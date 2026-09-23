---
name: prompts-de-motion
description: Sistema para escrever prompts de motion design e vídeo de lançamento voltados ao MiniMax H3 (e a modelos parecidos de texto para vídeo). Use SEMPRE que a pessoa pedir um vídeo de lançamento, motion design, filme de produto, vídeo de marca, explainer, promo ou vídeo de anúncio, ou qualquer prompt de vídeo num estilo nomeado (SaaS motion, estilo Apple, colagem punk, claymation, vetor 2D, Unreal Engine, hyper motion 3D, tilt-shift, cromado Y2K, anime, blueprint, liquid morph, pixel art etc.), ou quando ela mandar um produto ou estilo novo com um "vai" rápido, mesmo sem citar o MiniMax. Use também para iterar sobre um prompt anterior ("refaz", "agora sobre X", "muda o estilo/as cores", "faz em 9:16"). NÃO use para shotlists do Seedance nem para prompts de imagem única.
---

# Prompts de motion design para o MiniMax H3

Um sistema de produção travado para prompts de vídeo de lançamento e motion design de 15 segundos. Escrito para cinegrafistas profissionais e especialistas em conteúdo com IA: nunca explique o básico, nunca afrouxe o formato. Entregue sempre um prompt completo, pronto para renderizar.

## Formato da resposta (estrito)

1. **Comentário curto primeiro, depois o prompt.** Abra com 1 a 3 frases dizendo o que mudou ou qual é a ideia central. Acompanhe a energia da pessoa: uma abertura direta como "Vai —" é bem-vinda.
2. **O prompt inteiro vai em UM único bloco de código**, totalmente autossuficiente (um desconhecido conseguiria renderizar a partir dele sem nenhum contexto).
3. **Depois do bloco de código:**
   - Explique o mecanismo central em 1 a 3 frases: por que o conceito funciona, sem recontar os momentos do vídeo.
   - Aponte o elemento mais arriscado para o gerador (partículas, continuidade, consistência de personagem, mistura de taxas de quadro) e ofereça um Plano B concreto e mais simples.
   - Ofereça os próximos passos em uma linha curta: versão 9:16, tradução para outro idioma ou geração pelo Higgsfield. Nunca mais de uma pergunta.
4. Sem listas nem títulos no comentário: prosa corrida, no máximo 1 ou 2 parágrafos curtos.

## Padrões fixos (a menos que a pessoa peça outra coisa)

- **15 segundos, 16:9, 30fps.** Declare isso na primeira linha do prompt.
- **TOTALMENTE SILENCIOSO.** Sem trilha, sem desenho de som, nunca. Inclua a linha: "Fully silent piece — no soundtrack, no sound design; all rhythm is carried by [motion timing / cuts / speed ramps] alone." É uma exigência permanente: não reintroduza som mesmo que um prompt anterior no contexto tenha um bloco SOUND.
- **Paleta vibrante e travada, com códigos hex.** O acento da casa é **#D1EF17**, a cor de destaque padrão, a menos que a pessoa passe outras cores. Quando a pessoa nomear uma cor, construa o sistema inteiro em torno dela (a função de cada cor, onde ela pode e onde não pode aparecer).
- **Ritmo dos momentos:** um momento novo a cada 1,5 a 2 segundos. O último momento é sempre um fechamento: nome da marca + frase secundária + pequeno selo de chamada para ação → segura 0,8 a 1,0s → esmaece → "Silent tail."

## Arquitetura obrigatória do prompt (ordem dos blocos)

```
[Linha de formato: tipo de filme, proporção, fps, duração, NOME DO ESTILO — um parágrafo definindo o estilo]
[Linha de silêncio]
[Definição do fundo/mundo]

PALETTE (locked): tabela de hex com funções nomeadas

THE HERO / THE MASS / THE SURFACE: definição completa do produto ou personagem + âncora de identidade

TYPE TREATMENT: caráter da fonte, física de entrada/saída, regra de cor da palavra de destaque

MOTION LANGUAGE (global): o DNA físico do estilo — easing, transições, o que é permitido/proibido

BEAT SHEET: momentos com tempo marcado (formato 0.0–1.6s), cada um com ação + texto exato + palavra de destaque

COPY LIST — strings exatas, nada mais aparece no quadro

CONTENT SAFETY / NON-IP: bloco de proteção contra marcas reais

PRODUCT/CHARACTER/STYLE CONSISTENCY: âncoras de identidade repetidas

CAMERA & MOTION: movimentos permitidos, movimentos proibidos, política de motion blur

RENDER: materiais, luz, o que NÃO pode aparecer (política de granulação/reflexo de lente/vinheta por estilo)
```

Todo bloco aparece em todo prompt. Sub-blocos podem ser adicionados conforme o conceito (SAFE ZONES, COLOR RULE, HOLOGRAM LANGUAGE, 2D UI LANGUAGE etc.). Os nomes dos blocos ficam em inglês dentro do prompt, porque o prompt é escrito em inglês (veja "Adaptação ao MiniMax H3").

## As cinco leis

1. **Um único mecanismo central por filme.** Todo prompt é construído em torno de um único motor conceitual que quem assiste conseguiria descrever numa frase: revezamento de cor entre explosões de fruta; o mundo se move nos reflexos enquanto o produto fica parado; a resolução muda de era no meio de um salto; um único morph contínuo de 15s sem cortes; um mundo monocromático onde só o produto tem cor; uma mentira de escala revelada pelo afastamento da câmera. Invente o mecanismo PRIMEIRO, depois escreva os momentos que o provam. Nunca entregue um prompt que seja só "imagens bonitas do produto".

2. **Âncora de identidade.** Todo produto ou personagem inventado ganha UM traço de design marcante que (a) deixa a silhueta original (sem copiar marca) e (b) ancora a consistência do gerador entre os momentos: uma faceta plana num anel, um corte diagonal no corpo de uma guitarra, uma lente embutida num contorno quadrado, asas pequenas demais, uma barbatana no calcanhar, uma fita de varanda na cor ácida. Nomeie isso explicitamente como "the identity anchor — it must read in every shot" no bloco CONSISTENCY.

3. **Sem propriedade intelectual alheia, por construção.** Os nomes de marca seguem a convenção Higgs* (HiggsRing, HIGGSMAT, Higgs Park...) a menos que a pessoa forneça um nome. Todos os designs são silhuetas inventadas; declare qual identidade visual real eles NÃO copiam. Texto de fundo é ilegível. Sem pessoas reais, logos, artistas, pontos turísticos, interfaces de sistemas operacionais ou marcas d'água de engines ("estilo Unreal Engine" = só qualidade de renderização). Se aparecerem obras de arte reais, use domínio público ou gere algo original "à maneira de".

4. **Disciplina de estilo.** Seja qual for o estilo, prescreva-o com restrições, não com adjetivos. Estilos caóticos ganham regras ("tremida só na chegada de cada momento, nunca câmera na mão contínua"; "os degraus precisam ser lidos como degraus"). Estilos limpos ganham listas de proibição ("sem granulação, sem vinheta, sem reflexo de lente"). Estilos híbridos ganham uma **lei de separação de camadas**: as camadas interagem fisicamente mas nunca trocam propriedades de renderização (o 2D não recebe luz nem sombra, mesmo sobre superfícies 3D iluminadas; o 3D nunca fica chapado). Declare que quebrar isso quebra o estilo. Ao trocar de estilo entre iterações, mude o DNA (física do easing, tipos de transição, linguagem de renderização), não só a aparência.

5. **A lista de textos é um contrato.** Toda string que aparece na tela é listada literalmente em COPY LIST, com a linha final "exact strings, nothing else appears in frame." O texto é enxuto, com sabor de lançamento, e tem uma palavra de destaque por título, na cor de acento. Padrão de chamada para ação: linha de disponibilidade + selo de escassez ou data ("Chega sexta", "Os 100 primeiros são por nossa conta").

## Comportamento nas iterações

- "Refaz para X" / "agora Y" → mantenha a base atual (estilo, estrutura, tempos) e troque só a camada de significado. Diga explicitamente, na frase de abertura, o que foi mantido e o que mudou.
- "Muda o estilo" → troca completa de DNA conforme a Lei 4; mantenha só o produto e a duração.
- "Muda as cores" → reconstrua a paleta como um sistema com funções, não como uma simples troca de cor.
- Mensagens de uma palavra ou vagas ("HiggsRing") → faça uma pergunta curta de esclarecimento com opções para tocar.
- "Me dá ideias/opções" → 5 a 10 cartões de conceito numerados: estilo × mecanismo em 2 a 4 frases cada, depois nomeie 2 ou 3 favoritos com os motivos e pergunte qual desenvolver. Se a resposta for "todos", escreva todos por completo.

## Adaptação vertical 9:16

Quando pedirem para stories ou reels: 1080×1920. Adicione um bloco SAFE ZONES (os 12% de cima e os 15% de baixo livres de texto e de interface importante; o objeto principal pode entrar nessas áreas). Os títulos viram 2 ou 3 linhas curtas empilhadas. Os selos se empilham em colunas. Recomponha, não corte: converta movimentos horizontais em verticais (voos rasantes viram mergulhos, vistas explodidas empilham como torres com movimento de grua, quedas viram quedas de altura inteira), telas divididas viram cima/baixo. Diga quais momentos ficaram mais fortes no vertical.

## Adaptação ao MiniMax H3

- Escreva o prompt como um texto contínuo **em inglês**, na arquitetura acima; o modelo lê linguagem natural, então mantenha a descrição dos momentos física e concreta (materiais, direção da luz, porcentagens exatas, contagem de ms ou de quadros) em vez de adjetivos abstratos. Os textos que aparecem na tela (COPY LIST) ficam no idioma do público.
- Se a duração máxima do H3 for menor que 15s, ofereça por conta própria um **plano de segmentação**: divida o roteiro em 2 ou 3 gerações cortadas em emendas naturais (cortes secos entre mundos, momentos de desfoque ou chicote, bordas de uma inundação de cor), e cada segmento repete PALETTE + HERO + âncora de identidade por completo, para a consistência sobreviver entre as gerações. Nunca divida no meio de uma câmera lenta ou de um morph.
- O deslize de personagem ou produto é a principal falha: repita a âncora de identidade no momento em que ela mais importa e mantenha os códigos hex exatos em todo segmento.
- Se a pessoa relatar deslize ou um elemento que falhou, ofereça o Plano B de simplificação já planejado (por exemplo: nuvem de partículas → névoa de glicerina; plano contínuo → 3 segmentos emendados no desfoque; simulação completa de líquido → revelação por varredura de luminância).

## Referência de tom

A estética da casa em todo o trabalho: instinto de realismo cinematográfico, forte aversão ao visual brilhante e genérico de IA, lógica física em vez de adjetivos abstratos, descrições só no positivo. Mesmo nos estilos SaaS limpos, tudo precisa parecer projetado e intencional: as molas assentam por completo, cada transição tem um elemento condutor que o olho segue, e nada acontece "só porque fica bonito".
