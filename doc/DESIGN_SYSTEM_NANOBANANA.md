# Design System - Supercurso Nano Banana

**Data:** 2025-12-26
**Baseado em:** FEP_STYLE_REFERENCE.md, CONTENT_STRUCTURE.md, LAYOUT_REFERENCE.md

---

## 1. Stack Tecnológico

```
Framework CSS:  Tailwind CSS 3.x (CDN)
JavaScript:     Vanilla JS
Fontes:         Google Fonts - Inter
Build:          HTML puro (sem build process)
Dark Mode:      Tailwind class-based (localStorage + system preference)
Hospedagem:     GitHub Pages
```

---

## 2. Identidade Visual por Trilha

| Trilha | Nome | Cor Primária | Emoji | Badge |
|--------|------|--------------|-------|-------|
| **Trilha 1** | Fundamentos | Emerald (#10B981) | 🎯 | FUNDAMENTOS |
| **Trilha 2** | Nano Banana Mastery | Blue (#3B82F6) | 📚 | NANO BANANA |
| **Trilha 3** | Filmmaking com IA | Purple (#8B5CF6) | 🎬 | FILMMAKING |

### Classes por Trilha

```css
/* Trilha 1 - Fundamentos */
Badge:      bg-emerald-500/20 text-emerald-400
Borda:      border-emerald-500/30
Gradiente:  from-emerald-900/30 to-dark-800
Texto:      text-emerald-400
Hover:      hover:border-emerald-400

/* Trilha 2 - Nano Banana */
Badge:      bg-blue-500/20 text-blue-400
Borda:      border-blue-500/30
Gradiente:  from-blue-900/30 to-dark-800
Texto:      text-blue-400
Hover:      hover:border-blue-400

/* Trilha 3 - Filmmaking */
Badge:      bg-purple-500/20 text-purple-400
Borda:      border-purple-500/30
Gradiente:  from-purple-900/30 to-dark-800
Texto:      text-purple-400
Hover:      hover:border-purple-400
```

---

## 3. Paleta de Cores

### Dark Mode (Padrão)
| Nome | Código | Uso |
|------|--------|-----|
| `dark-900` | `#111827` | Fundo principal da página |
| `dark-800` | `#1f2937` | Cards, containers |
| `dark-700` | `#374151` | Elementos internos, hover states |
| `dark-600` | `#4b5563` | Bordas, divisores |

### Light Mode
| Nome | Código | Uso |
|------|--------|-----|
| Background | `#f8fafc` | Fundo principal |
| Cards | `#ffffff` | Cards, containers |
| Elementos | `#f1f5f9` | Elementos internos |
| Bordas | `#e2e8f0` | Bordas, divisores |

### Cores Semânticas
| Cor | Uso |
|-----|-----|
| `emerald-400/500` | Sucesso, positivo, "fazer" |
| `red-400/500` | Erro, alerta, "não fazer" |
| `blue-400/500` | Informação, dados |
| `yellow-400/500` | Aviso, atenção |
| `cyan-400/500` | Tech, dicas técnicas |

---

## 4. Estrutura de Arquivos

```
/curso/
├── index.html                    # Página principal do curso
├── trilha1/
│   ├── index.html               # Página da Trilha 1
│   ├── modulo-1-1.html          # O que é Geração de Imagens com IA
│   ├── modulo-1-2.html          # Como os Modelos de IA "Veem"
│   ├── ...
│   └── modulo-1-10.html         # Projeto Prático
├── trilha2/
│   ├── index.html
│   └── ...
├── trilha3/
│   ├── index.html
│   └── ...
└── assets/
    └── (se necessário)
```

---

## 5. Estrutura de Módulo

```
1. HEADER
   └── Badge da trilha
   └── Título com emoji
   └── Descrição (1-2 linhas)

2. STATS BANNER
   └── 3-5 métricas-chave do módulo

3. CONCEITOS PRINCIPAIS (2-4 seções)
   └── Cada conceito em seção própria
   └── Ordem: mais importante primeiro

4. ELEMENTOS DE SUPORTE
   └── Exemplos práticos
   └── Comparações (fazer/não fazer)
   └── Dados e pesquisas

5. RESUMO/CHECKLIST
   └── Síntese dos pontos principais
   └── CTA para voltar ao curso
```

---

## 6. Tipos de Boxes

### Box de Conceito (Gradiente)
```html
<div class="bg-gradient-to-br from-[COR]-900/30 to-dark-800 rounded-2xl p-8 border border-[COR]-500/30">
```

### Box Simples (Card)
```html
<div class="bg-dark-800 rounded-2xl p-8 border border-dark-600">
```

### Box de Informação Interna
```html
<div class="bg-dark-700/50 rounded-xl p-6 mb-6">
```

### Box de Dica
```html
<div class="bg-[COR]-900/20 p-6 rounded-xl border border-[COR]-500/30">
  <h4 class="font-bold text-[COR]-400 mb-3">💡 Dica</h4>
  <p class="text-neutral-300">...</p>
</div>
```

### Grid de Comparação
```html
<div class="grid md:grid-cols-2 gap-6">
  <div class="bg-emerald-900/20 p-6 rounded-xl border border-emerald-500/30">
    <h4 class="font-bold text-emerald-400 mb-4">✓ FAZER</h4>
    ...
  </div>
  <div class="bg-red-900/20 p-6 rounded-xl border border-red-500/30">
    <h4 class="font-bold text-red-400 mb-4">✗ NÃO FAZER</h4>
    ...
  </div>
</div>
```

---

## 7. Tipografia

| Elemento | Classes |
|----------|---------|
| Título da página (h1) | `text-4xl sm:text-5xl font-bold` |
| Título de seção (h2) | `text-2xl font-bold` |
| Título de sub-seção (h3) | `text-xl font-bold` |
| Parágrafo normal | `text-neutral-300` |
| Texto secundário | `text-neutral-400` |
| Badge | `text-sm font-semibold` |

---

## 8. Espaçamento

| Classe | Uso |
|--------|-----|
| `mb-12` | Entre seções principais |
| `mb-6` | Entre sub-seções |
| `mb-4` | Entre elementos dentro de uma seção |
| `p-8` | Padding de cards principais |
| `p-6` | Padding de boxes internos |
| `gap-6` | Espaço entre itens de grid |

---

## 9. Container Principal

```html
<main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
  <!-- Conteúdo -->
</main>
```

---

## 10. Tom de Voz

- **Direto e prático:** Sem enrolação
- **Conversacional:** Como se falasse com um amigo
- **Confiante:** Afirmações claras, não "talvez" ou "pode ser"
- **Empolgante:** Usar destaques em **negrito** para pontos-chave
- **Parágrafos:** Máximo 3-4 linhas

---

## 11. Checklist de Enriquecimento por Conceito

- [ ] **Contexto:** Por que isso importa?
- [ ] **Explicação técnica:** Como funciona?
- [ ] **Visualização:** Diagrama, barra, timeline
- [ ] **Exemplos:** Casos reais, prompts prontos
- [ ] **Comparação:** Certo vs Errado
- [ ] **Dados:** Estatísticas com fonte
- [ ] **Aplicação:** Como usar na prática

---

## 12. Emojis por Contexto

| Categoria | Emojis |
|-----------|--------|
| Conceito | 💡 🧠 📖 |
| Técnica | ⚙️ 🔧 🛠️ |
| Exemplo | 📝 ✏️ |
| Dica | 💡 ✨ |
| Alerta | ⚠️ ❌ |
| Sucesso | ✅ ✓ 🎉 |
| Foto/Imagem | 📷 🖼️ 🎨 |
| Vídeo | 🎬 📹 🎥 |
| IA | 🤖 🧠 |
