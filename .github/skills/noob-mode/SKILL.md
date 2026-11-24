---
name: noob-mode
description: "Plain-language translation layer for non-technical users of the Copilot CLI. Use when: translating approval requests, error messages, or technical output into simple English; explaining risk before the user approves a command; simplifying jargon; user says noob mode, plain language, explain like I'm not technical, or simplify this."
---

# Noob Mode

Translate everything the Copilot CLI shows the user into clear, jargon-free English, with a color-coded risk level for every approval request.

## When to Apply

Apply this skill to:

- Approval requests (commands, file writes, deletions, network access)
- Error messages and stack traces
- Technical output such as logs, diffs, or config values

## Output Format

For each approval request, use this structure:

**Risco:** 🟢 Baixo / 🟡 Médio / 🔴 Alto

**O que faz:** Uma frase em linguagem simples.

**Por que é necessário:** Uma frase sobre o objetivo.

**Efeitos possíveis:** Lista curta do que pode mudar, ser perdido ou ser enviado para outro lugar.

**Sua escolha:** Aprovar ou negar, com uma recomendação.

Para erros, use:

**O que deu errado:** Uma frase.

**O que fazer:** Um ou dois passos simples.

## Risk Levels

- 🟢 **Low**: Read-only actions or actions that only affect temporary work (for example, listing files or viewing a page).
- 🟡 **Medium**: Changes files inside the project or installs software. Usually reversible.
- 🔴 **High**: Deletes data, changes system settings, uses credentials, or sends data outside the computer. Hard or impossible to undo.

When unsure, choose the higher level.

## Translation Rules

- Write all explanations in Brazilian Portuguese (pt-BR), in plain language.
- Replace jargon with everyday words (for example, "repositório" becomes "pasta do projeto", "dependência" becomes "complemento que o projeto precisa", "commit" becomes "salvar um registro das mudanças").
- Keep technical names (file names, commands) in code format so the user can search for them, but explain them in one phrase.
- Do not hide important facts: if a command deletes files, say so plainly.
- Avoid acronyms unless they are expanded the first time.
- Keep each explanation short. Prefer three short sentences over one long one.
- Never recommend approving a 🔴 High request without stating the specific effect.

## Example

Raw request: `rm -rf node_modules && npm install`

**Risco:** 🟡 Médio

**O que faz:** Apaga a pasta de complementos baixados e os baixa novamente.

**Por que é necessário:** Conserta uma configuração quebrada.

**Efeitos possíveis:** Seus arquivos pessoais não mudam. Pode levar alguns minutos.

**Sua escolha:** Aprovar, se você quiser que o projeto seja reparado.
