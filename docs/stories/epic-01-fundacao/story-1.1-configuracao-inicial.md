# Story 1.1: Configuração Inicial do Projeto Astro Starlight

**Epic:** Épico 1 - Fundação da Plataforma e Renderização de Conteúdo
**Status:** ready-for-dev
**Priority:** High
**Estimated Effort:** 4 horas
**Dependencies:** Nenhuma (primeira história)

## User Story

Como um **desenvolvedor**, eu quero **configurar o ambiente inicial do projeto Astro Starlight** para que **possamos ter a base da plataforma pronta para desenvolvimento**.

## Acceptance Criteria

- [ ] Ambiente de desenvolvimento configurado com Node.js LTS e pnpm
- [ ] Projeto Astro inicializado com template Starlight
- [ ] Servidor de desenvolvimento rodando e acessível via localhost
- [ ] Controle de versão Git inicializado com commit inicial
- [ ] Conteúdo padrão do Starlight removido e título do site atualizado

## Technical Tasks

- [x] **1.1.1: Preparar Ambiente de Desenvolvimento:**
  - Verificar se o Node.js (versão LTS) está instalado.
  - Instalar `pnpm` globalmente (`npm install -g pnpm`).

- [x] **1.1.2: Inicializar o Projeto Astro com Starlight:**
  - Executar `pnpm create astro@latest`.
  - Seguir os prompts para selecionar o template "Starlight".

- [x] **1.1.3: Instalar Dependências e Validar:**
  - Executar `pnpm install`.
  - Iniciar o servidor de desenvolvimento com `pnpm dev`.
  - Acessar o `localhost` para confirmar que o site está no ar.

- [ ] **1.1.4: Configurar Controle de Versão:**
  - Executar `git init`.
  - Criar o commit inicial com a estrutura do projeto.

- [ ] **1.1.5: Limpeza do Conteúdo Padrão:**
  - Remover as páginas e documentação de exemplo do Starlight.
  - Atualizar o título do site em `astro.config.mjs`.

## Notes

- Esta é a história fundamental que estabelece toda a base do projeto
- Todos os desenvolvedores devem conseguir clonar e rodar o projeto após esta história
- Documentar o processo de setup no README se necessário

## Dev Agent Record

### Context Reference
- [story-1.1-configuracao-inicial.context.xml](story-1.1-configuracao-inicial.context.xml)

## References

- PRD Section: [4. Detalhamento dos Épicos e Histórias - História 1.1](../PR.md#história-11-configuração-inicial-do-projeto-astro-starlight)
- Architecture: [Tech Stack - Astro & Starlight](../Arquitetura.md#3-tech-stack-versão-20---revisada)
- Astro Docs: https://docs.astro.build
- Starlight Docs: https://starlight.astro.build
