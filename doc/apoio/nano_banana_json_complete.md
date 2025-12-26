# Estrutura JSON Completa para Nano Banana

## Por Que Prompts JSON Funcionam Melhor

Prompts em texto simples são vagos. Prompts JSON são precisos. JSON faz diferença porque oferece saída mais limpa (Nano Banana processa dados estruturados de forma mais confiável), imagens mais nítidas (categorias claras resultam em menos artefatos estranhos), controle (define estilo, ambiente, composição e detalhes técnicos separadamente), e repetibilidade (uma vez que você tem um formato JSON que funciona, pode reutilizá-lo para resultados consistentes).

## Anatomia de um Prompt JSON

A estrutura básica de um prompt JSON para Nano Banana contém seis blocos principais:

```json
{
  "style": {},
  "technical": {},
  "materials": {},
  "environment": {},
  "composition": {},
  "quality": {}
}
```

Cada bloco comunica algo específico ao modelo: **style** define o visual e a sensação, **technical** especifica detalhes similares a configurações de câmera, **materials** descreve texturas, tecidos e superfícies, **environment** estabelece o cenário ou fundo, **composition** determina como os elementos são organizados no quadro, e **quality** define resolução e acabamento.

## Detalhamento dos Blocos

### Bloco Style (Estilo)
O estilo é o humor da imagem. Define se você quer drama cinematográfico, realismo documental ou uma pintura a óleo surreal.

```json
"style": {
  "primary": "photorealistic",
  "rendering_quality": "high-resolution",
  "lighting": "natural"
}
```

O campo **primary** define a base artística (photorealistic, cinematic, painterly, surreal), **rendering_quality** garante clareza, e **lighting** estabelece a atmosfera.

### Bloco Technical (Técnico)
Este bloco permite que você atue como fotógrafo, controlando profundidade de campo, abertura e exposição.

```json
"technical": {
  "aperture": "f/1.8",
  "depth_of_field": "shallow",
  "exposure": "balanced"
}
```

### Bloco Materials (Materiais)
Especifica os materiais quando você está gerando produtos, ambientes ou objetos.

```json
"materials": {
  "primary": "oak wood",
  "secondary": "glass",
  "texture": "smooth"
}
```

Este bloco é crucial para mockups de produtos ou visuais de design onde as superfícies importam.

### Bloco Environment (Ambiente)
O modelo precisa de contexto para entender onde a cena acontece.

```json
"environment": {
  "location": "modern office",
  "time_of_day": "sunset",
  "weather": "clear"
}
```

### Bloco Composition (Composição)
Controla como o sujeito é enquadrado na imagem.

```json
"composition": {
  "framing": "rule of thirds",
  "angle": "low-angle shot",
  "focus_subject": "center"
}
```

### Bloco Quality (Qualidade)
Fornece instruções de acabamento final.

```json
"quality": {
  "resolution": "4K",
  "sharpness": "ultra-sharp",
  "post_processing": "cinematic grading"
}
```

## Exemplo Completo de Prompt JSON

```json
{
  "style": {
    "primary": "photorealistic",
    "rendering_quality": "high-resolution",
    "lighting": "soft natural light"
  },
  "technical": {
    "aperture": "f/1.8",
    "depth_of_field": "shallow",
    "exposure": "balanced"
  },
  "materials": {
    "primary": "stainless steel",
    "secondary": "glass",
    "texture": "polished"
  },
  "environment": {
    "location": "urban café",
    "time_of_day": "morning",
    "weather": "clear"
  },
  "composition": {
    "framing": "rule of thirds",
    "angle": "eye-level",
    "focus_subject": "coffee cup on table"
  },
  "quality": {
    "resolution": "4K",
    "sharpness": "crisp",
    "post_processing": "cinematic color grading"
  }
}
```

## Erros Comuns a Evitar

Os iniciantes frequentemente cometem três erros principais. Primeiro, misturar texto simples com JSON, quando o prompt deve ser puramente JSON. Segundo, esquecer chaves ou colchetes, pois um único caractere faltando invalida todo o prompt. Terceiro, sobrecarregar detalhes contraditórios, como especificar "low-light" junto com "bright exposure", o que confunde o modelo.

## Dicas Profissionais

Comece sempre pelo estilo e depois adicione camadas. Mantenha prompts modulares, permitindo trocar blocos de "environment" para reutilização. Use sempre o Thinking Mode no Gemini para raciocínio mais inteligente passo a passo. Teste pequenas alterações, pois uma mudança na abertura ou iluminação pode transformar completamente o resultado.

## JSON vs Texto Simples

Use JSON quando precisar de precisão, repetibilidade ou imagens polidas. Use texto simples quando estiver fazendo brainstorming, experimentando ou explorando ideias. O fluxo de trabalho profissional recomendado é começar em texto simples para testar ideias e depois mudar para JSON para os resultados finais.

## Casos de Uso Práticos

Empreendedores e criadores podem usar prompts JSON para mockups de fotografia de produtos (sem sessões fotográficas caras), visuais de marketing (campanhas publicitárias, posts em redes sociais), ativos de design de marca (logos, gráficos com estilo consistente), e storytelling (personagens consistentes em múltiplas imagens).
