# Story 1.4: Exibição de Documentos com Metadados de Governança

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Priority:** High
**Estimated Effort:** 6 horas
**Dependencies:** Story 1.2, Story 1.3

## User Story

Como um **profissional de saúde**, eu quero **ver informações de governança dos documentos (versão, status, autor)** para que **possa confiar na validade e atualidade da informação**.

## Acceptance Criteria

- [ ] Esquema de metadados definido em `src/content/config.ts`
- [ ] Campos obrigatórios: version, status, author, lastUpdated
- [ ] Metadados adicionados aos conteúdos de exemplo
- [ ] Componente `DocumentMetadata.astro` criado usando shadcn components
- [ ] Banner de status "Revogado" implementado com shadcn Alert
- [ ] Metadados renderizados corretamente em todas as páginas de documentos

## Technical Tasks

- [ ] **1.4.1: Definir Esquema de Metadados:**
  - Definir em `src/content/config.ts` o esquema para a coleção `docs`.
  - Adicionar os campos: `version` (string), `status` (enum: 'Rascunho', 'Publicado', 'Revisão', 'Revogado'), `author` (string), e `lastUpdated` (date).

- [ ] **1.4.2: Adicionar Metadados aos Conteúdos de Exemplo:**
  - Atualizar o frontmatter dos arquivos `.mdx` de exemplo com os novos campos.

- [ ] **1.4.3: Customizar a UI para Exibir Metadados (usando shadcn):**
  - "Ejetar" o componente `PageSidebar` ou `MarkdownContent` do Starlight para permitir customização.
  - Criar um componente Astro `DocumentMetadata.astro` usando componentes shadcn:
    - Usar `Card` do shadcn como container de metadados
    - Usar `Badge` para exibir version e status (cores diferentes por status)
    - Usar `Separator` para divisões visuais entre campos
  - Renderizar `version`, `status`, e `author` abaixo do título da página.

- [ ] **1.4.4: Implementar Banner de Status usando shadcn Alert (FR7):**
  - No componente customizado, usar o componente `Alert` do shadcn com `variant="destructive"`.
  - Adicionar lógica que exibe o Alert se o `status` do documento for 'Revogado'.
  - Incluir ícone de alerta (usando lucide-react) e mensagem clara sobre revogação.
  - Adicionar link para documento substituto (se aplicável).

## Notes

- Status "Revogado" deve ser muito visível para evitar uso de informação desatualizada
- Badge colors: Rascunho (cinza), Publicado (verde), Revisão (amarelo), Revogado (vermelho)
- Metadados são fundamentais para a confiabilidade do sistema
- Validar contraste de cores para WCAG 2.1 AA compliance

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.4](../PR.md#história-14-exibição-de-documentos-com-metadados-de-governança)
- Architecture: [Component Strategy - Badge, Card, Alert](../Arquitetura.md#35-estratégia-de-componentização-com-shadcn-studio-pro)
- FR7 (Status Banner): Exibir banner de alerta visual para documentos com status "Revogado"
- NFR7 (Componentização): WCAG 2.1 AA compliance
