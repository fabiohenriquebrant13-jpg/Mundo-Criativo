---
name: mundo-criativo-frontend
description: Melhorar o frontend da Mundo Criativo, preservando sua identidade visual e adaptando aparência e navegação ao celular.
---

# Frontend da Mundo Criativo

## Quando usar
Use para alterações de layout, aparência, navegação e responsividade.

## Preparação
- Leia o [contexto atual do projeto](../PROJETO.md), incluindo o ZIP de origem e as regras de sincronização.
- Leia as instruções AGENTS.md aplicáveis.
- Use o checkout existente; não crie worktrees sem pedido.
- Localize index.html e assets/.
- Se o projeto estiver apenas em ZIP, prepare uma cópia de trabalho
  sem sobrescrever arquivos existentes.
- Não substitua ou recompacte o ZIP sem pedido.
- Informe quando as alterações estiverem fora dos arquivos versionados.

## Identidade e conteúdo
- Siga o Manual_de_Marca_Mundo_Criativo.pdf e preserve o visual aprovado.
- Paleta: preto #1F1F1F, branco #FFFFFF, vermelho #FF5C5C, laranja #FFAF40, amarelo #FFE14C, verde #66D37E, azul #40B3FF e roxo #A56DFF. Use no máximo duas ou três cores de realce por composição.
- Fontes locais: League Spartan para títulos, menus e CTAs; Poppins para textos; Clicker Script para a marca e assinaturas. Preserve logos e fotografias reais.
- Use português brasileiro.
- Mantenha o foco em papelaria, presentes, roupas, brinquedos, eletrônicos e utilidades,
  em Santa Luzia/MG e região.
- Preserve contatos, endereço e horários.
- Não invente preços, garantias, avaliações, certificações
  ou vínculos com fabricantes.

## Desenvolvimento
- Prefira HTML, CSS e JavaScript simples.
- Adicione dependências apenas quando necessárias ao pedido.
- Priorize textos legíveis e botões fáceis de tocar.
- Evite rolagem horizontal indesejada na página.
- Preserve a rolagem horizontal intencional da galeria móvel.
- Mantenha imagens proporcionais e caminhos válidos.
- Preserve foco visível e navegação por teclado.

## Validação
- Confira larguras de 375, 768 e 1440 pixels.
- Teste abertura e fechamento do menu móvel.
- Confira aria-expanded, fechamento ao navegar e com Escape.
- Verifique links internos, imagens e perguntas frequentes.
- Confira os destinos de WhatsApp, telefone e mapa,
  sem enviar mensagens ou realizar chamadas.
- Use Playwright quando disponível.
- Localize Playwright e os navegadores antes de executar. Não presuma /workspace/site-dev-tools nem smoke.cjs; esses caminhos não fazem parte do projeto.

## Entrega
Explique o que mudou, o que foi verificado e as limitações.
Não publique nem envie alterações ao GitHub sem autorização.
