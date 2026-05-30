# 🏴‍☠️ SPCP — Surubão pros Chapéus de Palha

> *"Viemos fazendo graça, fomos também fazendo graça"*

Memorial online da comunidade **SPCP** — um servidor dedicado a One Piece, animes, jogos e muita putaria. Tudo infelizmente tem seu fim, mas a memória fica.

---

## 📁 Estrutura do projeto

```
spcp-memorial/
├── index.html       # O site completo (HTML, CSS e JS em um único arquivo)
└── imagens/         # Fotos dos membros da tripulação
    ├── exemplo.jpg
    └── ...
```

---

## ✏️ Como editar o site

Abra o `index.html` em qualquer editor de texto. Todas as seções editáveis têm um comentário explicativo logo acima delas — procure pelos blocos `<!-- === ... === -->`.

### Tripulação

Cada membro é um bloco assim:

```html
<div class="tribute-member"
     data-ini="AB"
     data-name="Nome do Membro"
     data-role="Descrição · Papel na comunidade"
     data-img="imagens/nome.jpg">
</div>
```

| Atributo | O que é | Exemplo |
|---|---|---|
| `data-ini` | Iniciais exibidas quando não há foto | `"JV"` |
| `data-name` | Nome do membro | `"João Vitor"` |
| `data-role` | Descrição ou papel | `"Nosso Luffy · O fundador"` |
| `data-img` | Caminho da foto (deixe `""` para usar iniciais) | `"imagens/joao.jpg"` |

**Adicionar membro:** copie um bloco inteiro e cole antes do `</div>` que fecha `#crewWall`.  
**Remover membro:** apague o bloco inteiro do `<div class="tribute-member">` até o `</div>`.

---

### Momentos marcantes

Cada card de momento é um bloco assim:

```html
<div class="theory-card reveal">
  <span class="theory-tag serious">Séria</span>
  <h3 class="theory-title">Título do momento</h3>
  <p class="theory-body">Descrição do que aconteceu.</p>
</div>
```

A tag de categoria aceita três valores:

| Valor na classe | Cor | Quando usar |
|---|---|---|
| `serious` | Roxo | Momentos marcantes de verdade |
| `fun` | Azul | Momentos engraçados ou de brincadeira |
| `debate` | Vermelho | Debates, conflitos, polêmicas |

**Adicionar momento:** copie um bloco e cole dentro de `<div class="theory-grid">`.  
**Remover momento:** apague o bloco inteiro.

---

### Música de fundo

O player de áudio já está implementado no site. Para ativar:

1. Coloque o arquivo `.mp3` na pasta do projeto (ex: `musica.mp3`)
2. Abra o `index.html` e procure por esta linha:
   ```html
   <!-- <source src="SUA_MUSICA.mp3" type="audio/mpeg"> -->
   ```
3. Remova os `<!--` e `-->` e substitua `SUA_MUSICA.mp3` pelo nome do seu arquivo:
   ```html
   <source src="musica.mp3" type="audio/mpeg">
   ```

---

## 🖼️ Como adicionar fotos dos membros

1. Salve a foto com um nome simples, sem espaços ou acentos (ex: `joao.jpg`)
2. Faça upload para a pasta `imagens/` aqui no GitHub
3. No `index.html`, localize o membro e preencha o `data-img`:
   ```html
   data-img="imagens/joao.jpg"
   ```

> ⚠️ **Evite usar links do Discord** para as imagens — eles expiram com o tempo e a foto vai quebrar no site. Prefira sempre arquivos dentro da pasta `imagens/` do próprio repositório.

---

## 🚀 Como atualizar o site

Qualquer alteração feita nos arquivos aqui no GitHub é refletida automaticamente no site em poucos segundos. Basta:

1. Editar o arquivo (clique no lápis ✏️ no GitHub)
2. Fazer o commit das mudanças
3. Aguardar alguns segundos e recarregar o site

---

## 🛠️ Tecnologias usadas

- HTML5 + CSS3 + JavaScript puro — sem frameworks, sem dependências externas
- Fontes: [Google Fonts](https://fonts.google.com/) — Cinzel Decorative, IM Fell English, Crimson Pro
- Hospedagem: [GitHub Pages](https://pages.github.com/) — gratuito

---

*Nakama é para sempre.* 🕯️
