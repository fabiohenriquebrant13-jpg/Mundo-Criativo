# Contexto da Mundo Criativo

## Estado verificado em 07/11/2026

- Repositório: `fabiohenriquebrant13-jpg/Mundo-Criativo`, branch remota `main`.
- A versão recente fornecida pelo usuário está em `Mundo_Criativo_Versao_Celular_Corrigida.zip`.
- Na raiz não existem atualmente `index.html` nem `Mundo-Criativo-Site-Institucional.html`; ambos estão na raiz interna do ZIP.
- O pacote inclui `assets/mundo-identidade.css`, imagens de fachada e fontes locais com licenças. Há também `assets/` solto no repositório: não presuma que ele esteja sincronizado com o ZIP.
- Consulte o `README.txt` atual e o manual PDF. Atualize este contexto quando a organização mudar; não restaure arquivos apagados a partir do histórico sem pedido.

## Escolha da fonte e fluxo de trabalho

1. Verifique Git, arquivos locais e conteúdo do ZIP antes de editar. Preserve mudanças do usuário.
2. Se o trabalho exigir editar a aplicação empacotada, confira caminhos e integridade do ZIP e extraia para uma pasta nova de trabalho fora dos arquivos publicáveis. Não sobrescreva o `assets/` da raiz para preparar uma auditoria.
3. Execute o servidor HTTP na pasta que realmente contém o `index.html` atual. O projeto é estático; não exige npm install, framework ou build por padrão. Exemplo, nessa pasta: `python3 -m http.server 8000 --bind 127.0.0.1`. Teste internamente, sem prometer uma prévia pública desse endereço.
4. Ao editar o site, mantenha os dois HTML do pacote sincronizados quando forem cópias equivalentes. Referencie o CSS realmente carregado. Não continue adicionando correções em folhas antigas sem uso.
5. Recompacte o ZIP somente quando solicitado ou já incluído claramente no escopo. Inclua HTML, CSS, imagens, fontes/licenças e demais arquivos do pacote autorizado. Exclua `.git`, `.agents`, credenciais, ferramentas e relatórios internos.
6. Confira integridade, conteúdo extraído e funcionamento do pacote final. Diferencie fonte preparada, ZIP, commit remoto e publicação.
7. Use o checkout existente; cada tarefa de nuvem já é isolada. Não crie worktrees sem pedido.

## Marca e informações comerciais

O manual `Manual_de_Marca_Mundo_Criativo.pdf` é a referência visual. Preserve a
revisão aprovada descrita no README: cabeçalho preto, texto branco, WhatsApp verde,
fachada integral sem zoom, cartões e melhorias móveis. As referências externas
servem para o objetivo autorizado, não para substituir a identidade da loja.

Paleta: #1F1F1F, #FFFFFF, #FF5C5C, #FFAF40, #FFE14C, #66D37E, #40B3FF e #A56DFF.
Use duas ou três cores de realce por composição. League Spartan em títulos,
menus e CTAs; Poppins em textos; Clicker Script em marca e assinaturas grandes.
Preserve as fontes locais e licenças.

A loja atua em Santa Luzia/MG com papelaria, presentes, roupas, brinquedos,
eletrônicos e utilidades. Preserve os dados atuais do pacote; não invente
endereço, telefone, horários, preços ou avaliações. Confira destinos sem enviar
mensagens de WhatsApp, ligações ou formulários.

URL anteriormente usada: https://fabiohenriquebrant13-jpg.github.io/Mundo-Criativo/.
Isso não comprova publicação ou configuração atual: verifique antes de afirmar
que está online ou definir metadados absolutos para uma implantação diferente.

## Ferramentas, validação e avaliações

Os scripts SEO agora estão em seo-audit/ e seo-audit-full/, com requisitos e uso
documentados em [SEO.md](SEO.md). Não há suíte de navegador versionada confirmada. Descubra
Python, Node, Playwright, Chromium, axe-core e Lighthouse no ambiente antes de
prescrever comandos. Não presuma caminhos de outro projeto. Mantenha dependências
de auditoria fora do pacote do site quando não forem dependências da aplicação.

Para alterações na aplicação, teste 375, 768 e 1440 px (e limites relevantes),
menu móvel/teclado/Escape/aria-expanded, categorias, âncoras, FAQ, imagens e
movimento reduzido, conforme o trecho alterado. Auditorias adicionais só quando
solicitadas ou necessárias. Para instalar skills/documentação, valide estrutura,
metadados e links locais; isso não é uma auditoria do site nem autoriza redesenho.

Use notas apenas em avaliações solicitadas, com medição ou rubrica, cenário e
cobertura. Não invente pontuações nem declare conformidade WCAG com teste automático.
