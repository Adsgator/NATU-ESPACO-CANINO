> **Como usar:** Abra o Claude Code na raiz do projeto clonado e cole o prompt abaixo seguido do conteúdo deste arquivo.

**Prompt para o Claude Code:**

```
Você está implementando o site do cliente Julia Martins (segmento: Adestramento de cães).
Leia este documento do início ao fim antes de começar. Depois siga passo a passo:

1. Preencha `src/styles/tokens.css` com as cores da seção "Direção de Arte" (apenas os valores — os nomes são fixos)
2. Atualize o `<link>` de fonte serifada no `BaseLayout.astro` conforme a tipografia indicada
3. Preencha `src/pages/index.astro` com imports dos componentes e ordem das seções
4. Para cada seção, substitua os textos placeholder pela copy indicada neste documento
5. Preencha `.env` com WhatsApp, GTM e domínio — o template já lê essas variáveis
6. Preencha o `defaultSchema` no `BaseLayout.astro` com os dados do Schema.org
7. Preencha os TODOs em `politica-de-privacidade.astro` e `termos-de-uso.astro` com dados reais
8. Garanta: Hero com `id="hero-section"`, Footer com `id="footer"`, main com `id="main-content"`
9. Rode `npm run build` para validar — corrija qualquer erro antes de considerar pronto

Regras absolutas::
- NUNCA hardcode cor, fonte ou tamanho — sempre `var(--t-*)` ou classes utilitárias Tailwind
- `<Image />` do Astro, nunca `<img>` nativo
- Sem `any` no TypeScript, sem `!important` no CSS
- Tema padrão: claro (padrão)
```

---

# Documento do Projeto — Julia Martins

**Studio:** Astroteca Studio
**Gerado em:** 02/06/2026
**Segmento:** Adestramento de cães
**Tipo:** servico

---

## Briefing do Cliente

| Campo                 | Valor                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------ |
| Nome do cliente       | Julia Martins                                                                                          |
| Nome da marca         | Natu - Espaço Canino                                                                                   |
| Segmento              | Adestramento de cães                                                                                   |
| Tipo de negócio       | servico                                                                                                |
| Domínio               | https://natuespacocanino.com.br/                                                                       |
| WhatsApp              | 5512982668716                                                                                          |
| Horários              | Segunda-feira a sexta-feira, das 07:30 às 17:00.                                                       |
| Instagram             | https://www.instagram.com/natu_espacocanino/                                                           |
| Objetivo de conversão | Mensagem WhatsApp                                                                                      |
| Mensagem WhatsApp     | Olá! Gostaria de saber mais sobre a Natu e como funciona a avaliação comportamental para novos alunos. |
| GTM ID                | GTM-WNJZBRCD                                                                                           |
| Schema tipo           | LocalBusiness                                                                                          |
| Google nota           | 5                                                                                                      |
| Google avaliações     | 9                                                                                                      |

### FAQ

Meu cão pode frequentar a Natu?
Sim! Os cães são sempre bem-vindos. Nosso objetivo é promover equilíbrio, bem-estar e desenvolvimento emocional, respeitando a individualidade de cada animal. Para isso, cada aluno passa por uma avaliação prévia.

Pode cão reativo?
Depende da demanda do cão, pois nossa prioridade é a segurança. Cães com níveis mais altos de reatividade são direcionados para a Hospedagem em Modo Internado, onde o foco é o treino, manejo exclusivo e modificação de comportamento em ambiente controlado.

Como funciona o descanso dos cães?
Todos os cães descansam em caixas ou baias individuais, garantindo segurança, redução de estresse e sono de qualidade. O ambiente é monitorado 24h para total tranquilidade.

Aceitam filhotes?
Sim! Aceitamos filhotes com o protocolo vacinal completo. O ambiente da Natu é ideal para uma socialização correta desde cedo, respeitando a idade e a fase de desenvolvimento de cada um.

Existe separação por porte?
Sim. Os cães são separados por porte e também por temperamento. Isso garante interações saudáveis e um melhor aproveitamento da rotina. Na Natu, a qualidade vem sempre antes da quantidade.

---

## Estrutura da Página

### 1. Header

_Copy não preenchido — Claude Code deve criar com base no briefing._

### 2. Hero

_Copy não preenchido — Claude Code deve criar com base no briefing._

### 13. CTA Final

_Copy não preenchido — Claude Code deve criar com base no briefing._

### 14. Footer

_Copy não preenchido — Claude Code deve criar com base no briefing._

---

## Direção de Arte

### Tema Padrão

**Claro**

### Cores — `src/styles/tokens.css`

Preencha **apenas os valores** (os nomes são fixos entre projetos):

```css
:root {
  --t-primary: #285224;
  --t-primary-dark: #1f411c;
  --t-secondary: #f47a1f;
  --t-background: #fdfbf7;
  --t-surface: #ffffff;
  --t-surface-alt: #f8f8f8;
  --t-dark: #1a1a1a;
  --t-text-main: #222222;
  --t-text-soft: #555555;
  --t-text-muted: #888888;
  --t-border: #e6e6e6;
}

.dark {
  --t-background: #15130f;
  --t-surface: #26231c;
  --t-surface-alt: #383329;
  --t-text-main: #e6e6e6;
  --t-text-soft: #b3b3b3;
  --t-text-muted: #737373;
  --t-border: #333333;
}
```

### Tipografia

| Papel                  | Fonte   |
| ---------------------- | ------- |
| Heading (`font-serif`) | Gliker  |
| Body (`font-sans`)     | Poppins |

**Referências visuais:** https://natuespacocanino.com.br/

**Notas:** Esse site é da stack antiga que eu usa, era wordpress com elementor, quero trazer ele para a stack no que uso agora Astro 5 + Tailwind v4. Quero trazer o mesmo projeto com mesma copy e tudo já dentro do novo formato

---

## Regras de Copy — DNA do Negócio

## DNA: Prestador de Serviço

**Tom:** Confiante, direto, focado em resultado tangível.
**Perspectiva:** "Eu resolvo seu problema" — não "eu ofereço um serviço".
**Foco:** Transformação antes/depois. O visitante deve sentir que o problema dele tem solução aqui.

**Copy que funciona:**

- Hero: atacar a dor principal no título. Subheadline com o resultado esperado.
- CTA: verbos de ação imediata — "Agende agora", "Fale comigo hoje", "Quero resolver isso".
- Sobre: credenciais rapidamente, depois voltar ao cliente — não fazer monólogo sobre si.
- Depoimentos: resultado específico + prazo + nome real. Ex: "Resolvi em 3 dias o que levava semanas".

**Evitar:** Jargão técnico, parágrafos longos, muito sobre o processo e pouco sobre o resultado.

---

## Checklist Final

- [ ] `npm run build` sem erros de TypeScript/Astro
- [ ] `src/styles/tokens.css` preenchido com cores reais do cliente
- [ ] Fontes carregadas: `<link>` no `BaseLayout.astro` + import `@fontsource` no `global.css`
- [ ] `.env` preenchido: `PUBLIC_WA_NUMBER`, `PUBLIC_WA_MESSAGE`, `PUBLIC_GTM_ID`, `PUBLIC_SITE_URL`
- [ ] `BaseLayout.astro`: title, description, OG, canonical, Schema.org JSON-LD
- [ ] Hero com `id="hero-section"`; Footer com `id="footer"`; main com `id="main-content"`
- [ ] Header: esconde ao rolar para baixo; link ativo por IntersectionObserver
- [ ] WhatsApp flutuante: some quando Hero ou Footer estão visíveis; número real no `.env`
- [ ] Dark mode: toggle no Footer; persiste localStorage; sem flash na primeira carga
- [ ] Todas as seções com copy real (sem placeholder genérico)
- [ ] Responsivo em mobile (375px): texto ≥ 20px, botões ≥ 44px, padding lateral ≥ 20px
- [ ] `politica-de-privacidade.astro` e `termos-de-uso.astro`: TODOs preenchidos
- [ ] Schema tipo: `LocalBusiness`
- [ ] GTM configurado (ID: GTM-WNJZBRCD)
- [ ] WhatsApp (número: 5512982668716)
