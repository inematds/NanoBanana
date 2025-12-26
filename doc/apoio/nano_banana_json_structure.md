# Estrutura JSON do Nano Banana Pro

## Anatomia de um Prompt JSON Perfeito

### 1. Core Identifiers (Identificadores Principais)
- **label**: Nome interno curto para o prompt (ex: "direct-flash-gamer-girl")
- **tags**: Palavras-chave de alto nível que funcionam como âncoras para a estética geral

### 2. Subject Block (Bloco do Sujeito)
- **Subject**: Lista descrevendo traços físicos (idade, pele, cabelo, expressão)
- **MadeOutOf**: Define materiais e texturas especificamente
- **Arrangement**: Pose e posicionamento físico

### 3. Environment (Ambiente)
- **Background**: Cenário geral
- **RoomObjects**: Itens específicos que povoam a cena
- **Accessories**: Pequenos detalhes que conectam o sujeito ao fundo

### 4. Technical Control (Controle Técnico)
- **Lighting**: Fonte de luz, direção e qualidade
- **ColorRestriction**: Limita a paleta de cores para coesão
- **Camera**: Objeto aninhado definindo o "equipamento virtual"
  - lens: Distância focal
  - aperture: Profundidade de campo
  - iso / grain: Controla textura

### 5. Output
- **OutputStyle**: Estilo final (photorealistic, oil painting, 3D render, anime)
- **Mood**: Atmosfera desejada

## Exemplo de Estrutura JSON Completa

```json
{
  "label": "direct-flash-gamer-girl",
  "tags": ["direct-flash", "90s-photography", "film-aesthetic"],
  "Style": ["direct-flash-photography-3", "documentary-candid-style-2"],
  "Subject": [
    "young woman, early 20s, fair skin",
    "long dark hair, loose braids",
    "eyes looking directly into camera"
  ],
  "MadeOutOf": [
    "white cotton camisole",
    "high-waisted shorts",
    "plastic gaming controller"
  ],
  "Arrangement": "subject sits cross-legged on couch, holding controller",
  "Background": "dimly lit retro room, crowded shelves",
  "ColorRestriction": [
    "warm tungsten tones",
    "white outfit for contrast",
    "red and black accents"
  ],
  "Lighting": "strong direct on-camera flash, hard shadows",
  "Camera": {
    "type": "digital rangefinder",
    "lens": "35mm",
    "aperture": "f/2.0",
    "flash": "high intensity direct"
  },
  "OutputStyle": "photorealistic snapshot, visible texture, film grain",
  "Mood": "intimate, nostalgic"
}
```

## Benefícios do JSON Prompting
1. **Separação de Conceitos**: Previne "concept bleeding" onde cores ou atributos vazam entre elementos
2. **Foco Ponderado**: O modelo presta atenção específica a detalhes definidos em chaves específicas
3. **Reprodutibilidade**: Permite trocar um único elemento sem quebrar a consistência
