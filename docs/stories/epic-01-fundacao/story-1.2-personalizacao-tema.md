# Story 1.2: Personalização da Identidade Visual (Tema)

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Priority:** High
**Estimated Effort:** 6 horas
**Dependencies:** Story 1.1

## User Story

Como um **gestor de conteúdo**, eu quero **que o site tenha a identidade visual da Secretaria de Saúde** para que **os usuários reconheçam imediatamente a origem oficial do conteúdo**.

## Acceptance Criteria

- [ ] Paleta de cores e tipografia da Secretaria aplicadas
- [ ] Shadcn studio pro instalado e configurado
- [ ] Componentes base shadcn instalados e testados
- [ ] CSS customizado aplicado com variáveis do Starlight
- [ ] Fontes customizadas configuradas
- [ ] Logo oficial substituído
- [ ] Tema consistente em todo o site

## Technical Tasks

- [ ] **1.2.1: Definir Paleta de Cores e Tipografia:**
  - Levantar as cores e fontes da identidade visual da Secretaria de Saúde.

- [ ] **1.2.2: Instalar e Configurar shadcn studio pro (Base de Componentes):**
  - Instalar shadcn CLI seguindo [documentação oficial](https://shadcnstudio.com/docs/getting-started/how-to-use-shadcn-cli).
  - Configurar o `shadcn.config.json` para integração com Astro e Tailwind.
  - Instalar componentes base necessários para o projeto:
    - `Button`: Botões de ação em toda aplicação
    - `Card`: Containers de conteúdo
    - `Badge`: Indicadores de status
    - `Alert`: Mensagens de sistema
    - `Input`: Campos de entrada
    - `Avatar`: Fotos de usuário (para fase de autenticação)
    - `DropdownMenu`: Menus dropdown (para fase de autenticação)
    - `Separator`: Divisores visuais
  - Configurar o shadcn studio MCP server para auxiliar no desenvolvimento (opcional, recomendado).
  - Testar renderização de componentes básicos em página de teste (`/test-components`).

- [ ] **1.2.3: Configurar CSS Customizado:**
  - Em `astro.config.mjs`, apontar a propriedade `customCss` para um novo arquivo (e.g., `src/assets/custom.css`).
  - No arquivo CSS, sobrescrever as variáveis de cor do Starlight (e.g., `--sl-color-accent`) com as cores do projeto usando o sistema de design do shadcn.

- [ ] **1.2.4: Configurar Fontes Customizadas:**
  - Se usar fontes externas (e.g., Google Fonts), importá-las no CSS.
  - Aplicar as fontes às variáveis de CSS do Starlight (e.g., `--sl-font-body`, `--sl-font-headings`).

- [ ] **1.2.5: Substituir Logo:**
  - Adicionar o logo oficial (preferencialmente SVG) à pasta `public/`.
  - Atualizar a propriedade `logo` em `astro.config.mjs` com o caminho para o novo logo.

- [ ] **1.2.6: Validar Alterações:**
  - Navegar pelo site para garantir que o novo tema foi aplicado de forma consistente.

## Notes

- A paleta de cores deve seguir WCAG 2.1 AA para contraste
- Shadcn studio pro é a biblioteca base para TODOS os componentes customizados
- Manter design tokens consistentes entre Starlight e shadcn
- Página de teste `/test-components` pode ser removida após validação

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.2](../PR.md#história-12-personalização-da-identidade-visual-tema)
- Architecture: [Estratégia de Componentização com shadcn studio pro](../Arquitetura.md#35-estratégia-de-componentização-com-shadcn-studio-pro)
- NFR3 (Design): Permitir personalização de cores e tipografia
- NFR7 (Componentização): shadcn studio pro como biblioteca base
