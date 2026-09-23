# Prompts de Motion

**Uma skill de Felipe Borges para o Claude Code que escreve prompts de vídeo de motion design de 15 segundos, prontos para o MiniMax H3 e modelos parecidos de texto para vídeo.**

Cada prompt sai com uma ideia central única, paleta travada com códigos hex, roteiro com os tempos de cada momento, lista exata dos textos da tela, proteção contra marcas reais e um Plano B para o elemento mais arriscado. A skill escreve o prompt; a geração do vídeo acontece na ferramenta que você usar.

## Conteúdo

- `skills/prompts-de-motion/SKILL.md`: a skill.
- `ALUNOS-prompts-de-motion.md`: guia para os alunos, com a skill pronta para copiar e colar.

## Instalar no Claude Code

```bash
mkdir -p ~/.claude/skills && cp -R skills/prompts-de-motion ~/.claude/skills/
```

Abra uma sessão nova do Claude Code. A skill aparece como `/prompts-de-motion` e também entra sozinha em pedidos de vídeo de lançamento ou de motion.
