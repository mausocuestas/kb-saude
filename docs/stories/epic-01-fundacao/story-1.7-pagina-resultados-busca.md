# Story 1.7 (UX): Design da Página de Resultados da Busca

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Priority:** Medium
**Estimated Effort:** 4 horas
**Dependencies:** Story 1.5, Story 1.6

## User Story

Como um **profissional de saúde**, eu quero **ver resultados de busca claros e bem formatados** para que **possa identificar rapidamente qual documento contém a informação que procuro**.

## Acceptance Criteria

- [ ] Página de resultados customizada com identidade visual do projeto
- [ ] Termos buscados destacados nos títulos e snippets
- [ ] Cada resultado mostra: título, snippet relevante, categoria
- [ ] Layout integrado com o design geral do site
- [ ] Resultados ordenados por relevância
- [ ] Interface responsiva

## Technical Tasks

- [ ] **1.7.1: Customizar a Página de Resultados da Busca:**
  - Seguir a documentação do Pagefind para customizar a UI de resultados, criando um layout que se integre à identidade visual do projeto.

- [ ] **1.7.2: Implementar Destaque de Termos:**
  - Garantir que os termos buscados sejam destacados nos títulos e snippets dos resultados.

- [ ] **1.7.3: Melhorar a Apresentação dos Snippets:**
  - Ajustar a UI para que cada resultado mostre o título da página, um trecho do conteúdo relevante e a categoria do documento.

## Notes

- Destaque de termos ajuda usuário a confirmar relevância rapidamente
- Snippets devem ter tamanho apropriado (não muito longos)
- Categoria ajuda a contextualizar o documento
- Considerar adicionar filtros por categoria/status em futuras iterações
- Manter consistência visual com homepage (Story 1.6)

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.7](../PR.md#história-17-ux-design-da-página-de-resultados-da-busca)
- Architecture: [Tech Stack - Pagefind](../Arquitetura.md#3-tech-stack-versão-20---revisada)
- FR3 (Search): Resultados relevantes e bem apresentados
