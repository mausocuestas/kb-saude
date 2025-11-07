# Story 1.6 (UX): Criação da Página Inicial Customizada

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Priority:** Medium
**Estimated Effort:** 5 horas
**Dependencies:** Story 1.2, Story 1.3, Story 1.5

## User Story

Como um **visitante do site**, eu quero **uma página inicial acolhedora com busca central e acesso rápido** para que **possa começar minha jornada facilmente sem precisar navegar pelo menu**.

## Acceptance Criteria

- [ ] Layout customizado criado sem sidebar Starlight padrão
- [ ] Barra de busca central implementada com shadcn Input
- [ ] Autocomplete/sugestões implementadas (opcional)
- [ ] Cards de acesso rápido criados com shadcn Card
- [ ] 3-4 links para categorias/documentos importantes
- [ ] Design responsivo (3 colunas desktop, 1-2 mobile)
- [ ] Hover effects e transições suaves

## Technical Tasks

- [ ] **1.6.1: Criar Layout Customizado para a Homepage:**
  - Criar um novo arquivo de layout em Astro que não utilize a sidebar e o layout padrão do Starlight.
  - Aplicar este layout apenas à rota `/`.

- [ ] **1.6.2: Implementar Barra de Busca Central (usando shadcn Input):**
  - Criar componente `SearchBar.astro` usando o `Input` do shadcn com tamanho grande (lg).
  - Adicionar ícone de busca à esquerda (usando lucide-react `Search` icon).
  - Estilizar para destaque central na página com sombra e animação de foco.
  - Implementar autocomplete/sugestões (opcional).
  - Ao submeter a busca, redirecionar o usuário para a página de resultados customizada.

- [ ] **1.6.3: Criar Componente de "Cards de Acesso Rápido" (usando shadcn Card):**
  - Desenvolver componente `QuickAccessCard.astro` baseado no `Card` do shadcn.
  - Estrutura: título, descrição curta, ícone (lucide-react) e link.
  - Incluir hover effects (elevação, transição suave) e cursor pointer.
  - Layout responsivo com grid de cards (3 colunas desktop, 1-2 mobile).

- [ ] **1.6.4: Popular os Cards:**
  - Definir uma lista estática de 3-4 links para as categorias ou documentos mais importantes.
  - Renderizar os cards usando o componente `QuickAccessCard`.

## Notes

- Homepage é o primeiro ponto de contato - deve ser simples e acolhedora
- Busca central é o principal CTA (Call to Action)
- Cards de acesso rápido para categorias mais acessadas
- Manter design consistente com identidade visual (Story 1.2)
- Performance é crítica - página deve carregar rapidamente

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.6](../PR.md#história-16-ux-criação-da-página-inicial-customizada)
- Architecture: [Component Strategy - Card, Input](../Arquitetura.md#35-estratégia-de-componentização-com-shadcn-studio-pro)
- FR3 (Search): Busca deve estar facilmente acessível
- NFR7 (Componentização): Usar shadcn components
