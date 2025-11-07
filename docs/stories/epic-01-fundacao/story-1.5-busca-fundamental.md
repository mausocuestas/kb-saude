# Story 1.5: Implementação da Busca Fundamental

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Priority:** High
**Estimated Effort:** 3 horas
**Dependencies:** Story 1.3, Story 1.4

## User Story

Como um **profissional de saúde**, eu quero **buscar documentos por conteúdo e metadados** para que **possa encontrar rapidamente informações específicas sem navegar manualmente**.

## Acceptance Criteria

- [ ] Build de produção gera índice Pagefind sem erros
- [ ] Busca por conteúdo funcional e retorna resultados relevantes
- [ ] Busca por metadados (autor, status) funcional
- [ ] Resultados de busca são precisos e bem ordenados
- [ ] (Opcional) Ponderação de busca ajustada para priorizar títulos

## Technical Tasks

- [ ] **1.5.1: Validar Indexação da Busca:**
  - Executar um build de produção (`pnpm build`) para gerar o índice de busca do Pagefind.
  - Verificar se o processo de indexação ocorre sem erros.

- [ ] **1.5.2: Testar Busca por Conteúdo e Metadados (FR3):**
  - Iniciar o servidor de preview (`pnpm preview`).
  - Realizar buscas por termos do conteúdo e por valores dos metadados (e.g., autor, status).
  - Confirmar que os resultados são relevantes e corretos.

- [ ] **1.5.3: Ajustar Ponderação da Busca (Opcional):**
  - Caso a relevância da busca precise de melhorias, investigar o uso de `data-pagefind-weight` nos componentes customizados para dar mais peso a títulos e metadados.

## Notes

- Pagefind é built-in no Starlight, não requer configuração extra inicial
- Build-time indexing garante performance máxima (NFR1)
- Busca por metadados é essencial para workflow dos profissionais
- Ponderação pode ser ajustada em iterações futuras se necessário

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.5](../PR.md#história-15-implementação-da-busca-fundamental)
- Architecture: [Tech Stack - Pagefind (Starlight built-in)](../Arquitetura.md#3-tech-stack-versão-20---revisada)
- FR3 (Search): Indexar e buscar por conteúdo e metadados do frontmatter
- NFR1 (Performance): Build-time rendering
