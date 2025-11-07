# Story 2.1: Criação do Componente de Feedback

**Epic:** Épico 2 - Implementação do Sistema de Feedback e Governança
**Priority:** High
**Estimated Effort:** 6 horas
**Dependencies:** Story 1.2 (shadcn components)

## User Story

Como um **profissional de saúde**, eu quero **avaliar e comentar sobre a utilidade dos documentos** para que **os gestores possam melhorar continuamente o conteúdo**.

## Acceptance Criteria

- [ ] Design da interface de feedback criado com shadcn components
- [ ] Componente `Feedback.astro` criado e funcional
- [ ] Estados visuais implementados (idle, loading, success, error)
- [ ] Botões 👍/👎 funcionais
- [ ] Campo de comentário aparece após seleção
- [ ] Toast de confirmação após envio
- [ ] Componente integrado no footer das páginas de documentos
- [ ] Separador visual antes do componente

## Technical Tasks

- [ ] **2.1.1: Design da Interface de Feedback com shadcn:**
  - Desenhar a UI usando componentes shadcn: `Card`, `Button`, `Textarea`, `Toast`.
  - Definir os estados visuais (idle, loading, success, error).
  - Layout: Card container com título "Este documento foi útil?", botões 👍/👎, textarea condicional, botão de envio.

- [ ] **2.1.2: Criar Componente Astro para Feedback:**
  - Criar o arquivo `src/components/Feedback.astro`.
  - Estrutura usando `Card` do shadcn como container principal.
  - Botões de avaliação (👍/👎) usando `Button` com variants (outline para não selecionado, default para selecionado).
  - Campo de comentário usando `Textarea` do shadcn (exibido apenas após seleção de 👍 ou 👎).
  - Botão de envio usando `Button` com variant="default" e ícone `Send` do lucide-react.

- [ ] **2.1.3: Adicionar Interatividade (Client-Side):**
  - Adicionar `<script>` para gerenciar o estado dos botões e do campo de texto.
  - Usar `Toast` do shadcn para feedback visual após submissão (sucesso ou erro).
  - Implementar estados de loading usando disabled state no `Button` durante envio.
  - Adicionar `Skeleton` (opcional) se houver carregamento assíncrono.

- [ ] **2.1.4: Integrar Componente na Página:**
  - Customizar o layout do Starlight (e.g., `Footer.astro`) para incluir o componente de feedback no final das páginas de documentos.
  - Adicionar `Separator` antes do componente de feedback para divisão visual.

- [ ] **2.1.5: Simular Submissão (Placeholder):**
  - Ao enviar, o componente deve exibir um `Toast` de agradecimento, sem enviar dados reais.
  - Toast deve ter ícone de sucesso (lucide-react `Check`) e mensagem "Obrigado pelo seu feedback!".

## Notes

- Esta história implementa apenas o UI - Story 2.2 adiciona backend
- Feedback anônimo por padrão (sem autenticação nesta fase)
- Toast de agradecimento melhora UX mesmo sem envio real
- Componente deve ser não-intrusivo mas facilmente visível

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 2.1](../PR.md#história-21-criação-do-componente-de-feedback)
- Architecture: [Component Strategy - Card, Button, Textarea, Toast](../Arquitetura.md#35-estratégia-de-componentização-com-shadcn-studio-pro)
- FR4 (Feedback Interface): Exibir seção de feedback com avaliação (👍/👎) e campo de comentário
