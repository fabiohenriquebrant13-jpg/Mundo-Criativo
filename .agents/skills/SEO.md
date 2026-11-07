# Auditorias SEO da Mundo Criativo

## Instalação e organização

Duas skills instaladas em `main`, adaptadas dos arquivos enviados pelo usuário
em 07/11/2026:

- [seo-audit](seo-audit/SKILL.md): auditoria básica de uma página.
- [seo-audit-full](seo-audit-full/SKILL.md): análise avançada, com módulos sociais,
  dados estruturados e PageSpeed quando configurado.

Cada pasta mantém seus próprios scripts, referência, template e licença MIT
(Copyright 2026 Jeff). Origem indicada nos anexos:
https://github.com/JeffLi1993/seo-audit-skill.
Os scripts, templates e licenças foram preservados como enviados. As instruções
e o guia da skill completa receberam adaptações locais. Os dois README enviados
são duplicados e foram consolidados neste guia; suas alegações sobre outro
repositório, branch, ambiente preparado e auditorias antigas não se aplicam aqui.
O arquivo [ORIGEM-SEO.json](ORIGEM-SEO.json) registra hashes dos anexos e destinos.

Leia [PROJETO.md](PROJETO.md) antes de escolher o alvo. O site recente está no ZIP;
instalar estas ferramentas não extrai nem modifica a aplicação e não comprova
que o site esteja publicado. Não inclua `.agents/`, ambiente virtual ou relatórios
no ZIP da hospedagem. Não recompacte o site como consequência da instalação.

## Dependências reproduzíveis

Requisitos consolidados dos dois anexos idênticos:
[requirements-seo-audit.txt](requirements-seo-audit.txt).

Na raiz de um checkout, com Python 3.10 ou posterior:

```bash
python3 -m venv /workspace/seo-audit-tools/venv
/workspace/seo-audit-tools/venv/bin/python -m pip install -r .agents/skills/requirements-seo-audit.txt
/workspace/seo-audit-tools/venv/bin/python -m pip check
```

O caminho é uma convenção para o ambiente de nuvem, não parte da aplicação.
Em outro computador, escolha um caminho de sua propriedade fora dos arquivos
publicáveis. Preserve proxy, certificados e TLS; não use verify=False.

## Utilização

Abra uma nova tarefa no projeto e peça, por exemplo:

- “Use $seo-audit para avaliar o SEO da URL que vou informar, sem alterar o site.”
- “Use $seo-audit-full para uma auditoria técnica da URL confirmada, com resultados em português.”
- “Use $seo-audit para revisar o HTML do ZIP atual; marque verificações da hospedagem como não avaliadas.”

O catálogo automático depende do cliente/sessão. É possível apontar diretamente
para o SKILL.md se necessário. Não execute uma auditoria só porque a skill foi instalada.

Os comandos do SKILL.md são relativos à pasta da skill, e o Python deve ser o do
ambiente virtual. Da raiz, um exemplo de verificação **local**, após extrair o
HTML atual para uma pasta de trabalho, é:

```bash
/workspace/seo-audit-tools/venv/bin/python .agents/skills/seo-audit/scripts/check-schema.py --file /tmp/mundo-auditoria/index.html
```

Esse caminho é um exemplo e precisa existir. Não analise o ZIP sem extrair o
arquivo correto, nem restaure HTML removido. O retorno 1 de um validador pode
significar um achado SEO ou erro de acesso: leia o JSON e diferencie os casos.
Os status e contagens são evidências, não pontuações oficiais de ranking.

Salve resultados fora do checkout, por exemplo
`/workspace/seo-audit-results/<execucao>/`, com data, versão, cenário e limites.
Os templates contêm achados demonstrativos: substitua/remova exemplos e
placeholders antes de entregar. Não coloque relatórios na página pública.
Siga [avaliacoes.md](melhorar-html/references/avaliacoes.md) para notas fundamentadas.

## Cuidados com o escopo e a interpretação

- Confirme domínio e subcaminho antes de requisições. A URL usada anteriormente
  foi `https://fabiohenriquebrant13-jpg.github.io/Mundo-Criativo/`; isso não verifica
  a hospedagem atual. Em GitHub Pages, robots e sitemap podem pertencer à raiz
  do host; não trate sua ausência no subcaminho como defeito automático.
- `check-site.py` normaliza hosts e pode examinar rotas/subdomínios fora do caminho
  principal. Leia os destinos antes de executá-lo. Não sonde test.github.io ou
  subdomínios de uma plataforma de terceiros como se fossem ambientes da loja.
  Em hospedagem compartilhada, prefira análise local e verificações manuais dos
  destinos autorizados; documente os módulos não executados.
- Seções “A loja” e contato podem ser válidas na mesma página. Não imponha páginas
  /about ou /contact sem necessidade. Não gere termos legais nem informações
  comerciais fictícias para satisfazer heurísticas.
- Scripts usam HTTP estático; não executam JavaScript de página. Quando necessário,
  compare com navegador. Semântica, contraste e qualidade editorial exigem revisão.
- Verificações locais não comprovam indexação, desempenho real, experiência em
  campo, autorização para publicar ou conformidade WCAG completa.

## PageSpeed e segredos

O script de PageSpeed lê `PAGESPEED_API_KEY` ou `GOOGLE_PAGESPEED_API_KEY`.
Confira bindings e presença das variáveis antes de solicitar configuração; nunca
peça o valor em chat nem grave chaves em comandos, relatórios ou commits.
Não solicite chave para instalação, --help ou validadores locais.

PageSpeed requer acesso a `www.googleapis.com` e credencial utilizável na rota
configurada. Sem esse pré-requisito, não execute o módulo; conclua as análises
independentes e identifique a auditoria como parcial. Um erro de chave, quota,
rede ou timeout não é nota zero de desempenho. API key não fornece acesso a GSC,
Analytics, logs ou dados privados do negócio.

## Verificação desta instalação

- Dependências dos anexos instaladas em ambiente virtual externo ao repositório.
- Dez scripts responderam a --help; sintaxe Python analisada.
- pip check não encontrou dependências incompatíveis.
- Casos locais controlados verificam leitura de JSON-LD e metadados sociais.
- Não foi executada auditoria pública da Mundo Criativo, chamada PageSpeed ou
  verificação de indexação. Nenhuma chave é necessária para os testes locais.

## Limitação verificada dos validadores

No caso controlado de JSON-LD sintaticamente inválido, o validador básico retorna
`warn` e exit 0; o completo retorna `fail` e exit 1. Não interprete exit 0 como
“SEO aprovado”: leia status, detail e schemas. Para validação sintática rigorosa,
use também o validador completo (modo --file não exige chave PageSpeed) ou o parser
JSON e registre a evidência adicional. Os scripts originais não foram alterados.
