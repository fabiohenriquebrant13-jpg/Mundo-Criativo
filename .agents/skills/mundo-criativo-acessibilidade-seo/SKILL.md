---
name: mundo-criativo-acessibilidade-seo
description: Auditar e melhorar acessibilidade, SEO e desempenho do site Mundo Criativo usando Playwright, axe-core e Lighthouse quando disponíveis.
---

# Acessibilidade e SEO da Mundo Criativo

## Quando usar
Use para auditorias e melhorias de acessibilidade, SEO e desempenho.

## Preparação
- Leia o [contexto atual do projeto](../PROJETO.md), incluindo o ZIP de origem e as regras de sincronização.
- Leia as instruções AGENTS.md aplicáveis.
- Use o checkout existente; não crie worktrees sem pedido.
- Identifique os arquivos do site e as ferramentas disponíveis.
- Preserve alterações existentes e informações comerciais.

## Acessibilidade
- Mantenha lang="pt-BR".
- Confira hierarquia de títulos e estrutura semântica.
- Verifique navegação por teclado e foco visível.
- Confira nomes acessíveis dos botões e links.
- Teste aria-expanded, fechamento do menu e tecla Escape.
- Confira contraste e textos alternativos das imagens.
- Mantenha um título descritivo no iframe do mapa.
- Use axe-core para verificações automatizadas.
- Não declare conformidade WCAG apenas com testes automatizados.

## SEO
- Mantenha título e meta description descritivos.
- Preserve conteúdo coerente com Santa Luzia/MG e região.
- Confira informações de compartilhamento nas redes sociais.
- Confirme a URL pública antes de adicionar canonical
  ou alterar URLs de compartilhamento.
- Não invente avaliações, certificações ou dados comerciais.
- Adicione dados estruturados apenas com informações verificadas.

## Desempenho
- Verifique tamanho, formato e dimensões das imagens.
- Use carregamento tardio nas imagens secundárias quando adequado.
- Evite carregamento tardio da imagem principal se prejudicar o LCP.
- Evite dependências desnecessárias.

## Ferramentas e validação
- Use Playwright para testar comportamento e diferentes telas.
- Use axe-core para identificar problemas de acessibilidade.
- Use Lighthouse para desempenho, acessibilidade,
  boas práticas e SEO.
- Descubra as ferramentas disponíveis antes de escolher comandos. Não há suíte de auditoria confirmada neste repositório.
- Se criar um relatório axe-core, salve as evidências fora do pacote público.
- Playwright, axe-core e Lighthouse são opcionais conforme o escopo; esta skill não instala ferramentas.
- Confira erros de execução e avisos antes de reportar resultados.
- Diferencie problemas do site, das ferramentas e da rede.
- Auditorias locais não comprovam indexação, ranking
  ou funcionamento de serviços externos.

## Entrega

Nas avaliações, siga o [padrão de notas de 0 a 100](../melhorar-html/references/avaliacoes.md),
com origem da nota, cenário e limitações. Checklists exigem rubrica e cobertura;
itens não medidos ficam como “não avaliado”.
Apresente problemas encontrados, verificações executadas
e validações manuais pendentes.
Não envie mensagens de WhatsApp nem publique sem autorização.
