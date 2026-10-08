---
marp: true
theme: uncover
paginate: true
style: |
  section { font-size: 28px; }
  section.small { font-size: 20px; }
  section.small table { font-size: 0.7em; }
  img[alt~="center"] { display: block; margin: 0 auto; }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Marp

## Créer des slides avec du Markdown

- Écrire en `.md`
- Prévisualiser dans VS Code
- Exporter en PDF, PPTX, HTML

---

# 1. Installation

- Installer **VS Code**

```text
Extension : marp-team.marp-vscode
```

---

# 2. Structure d'un fichier Marp

- **Front matter** : en haut, entre `---`
- **Slides** : séparées par `---`
- **Commentaires** : `<!-- ... -->`

```text
mon-projet/
├── presentation.md
└── images/
    └── logo.png
```

---

# 3. Directives globales / locales

- **Globale** : front matter → toutes les slides
- **Locale** : commentaire HTML → slides suivantes
- **Locale (une seule slide)** : préfixe `_`

```markdown
<!-- backgroundColor: #f0f0f0 -->
<!-- _class: lead -->
```

- `<!-- -->` = commentaire HTML
- Une directive y est écrite comme `clé: valeur`

---

<!-- _class: small -->

# 4. Syntaxes essentielles

| Syntaxe | Utilisation | Exemple |
|---|---|---|
| `#` | Titre principal | `# Titre` |
| `##` | Sous-titre | `## Sous-titre` |
| `###` | Titre niveau 3 | `### Détail` |
| `-` | Liste à puces | `- Point` |
| `1.` | Liste numérotée | `1. Étape` |
| `**texte**` | Gras | `**important**` |
| `*texte*` | Italique | `*note*` |
| `` `code` `` | Code en ligne | `` `npm install` `` |
| `[lien](url)` | Lien | `[Marp](https://marp.app)` |
| `![image](url)` | Image | `![logo](logo.png)` |
| `---` | Nouvelle slide | `---` |
| `>` | Citation | `> Une idée` |

---

<!-- _class: small -->

# 5. Syntaxes moins fréquentes

| Syntaxe | Utilisation | Exemple |
|---|---|---|
| Tableau Markdown | Afficher des données | `\| A \| B \|` |
| Bloc de code | Code sur plusieurs lignes | trois backticks + langage |
| `<!-- -->` | Commentaire / directive | `<!-- _class: lead -->` |
| `<!-- _clé: valeur -->` | Directive pour 1 slide | `<!-- _color: red -->` |
| `![w:300](url)` | Largeur d'image | `![w:300](logo.png)` |
| `![bg](url)` | Image de fond | `![bg](fond.jpg)` |
| `![bg right](url)` | Image à droite | `![bg right](photo.jpg)` |
| `~~texte~~` | Barré | `~~ancien~~` |
| `<!-- notes -->` | Notes de l'orateur | `<!-- Penser à la démo -->` |
| `<style>` | CSS personnalisé | `<style> h1 { color: red } </style>` |

---

# 6. Directives Marp

| Directive | Rôle | Exemple |
|---|---|---|
| `marp` | Activer Marp | `marp: true` |
| `theme` | Choisir le thème | `theme: default` |
| `paginate` | Numéros de page | `paginate: true` |
| `header` | En-tête | `header: "Cours"` |
| `footer` | Pied de page | `footer: "2026"` |
| `class` | Classe de slide | `class: lead` |
| `backgroundColor` | Fond | `backgroundColor: #fff` |
| `color` | Couleur du texte | `color: #333` |
| `size` | Format | `size: 4:3` |

---

# 7. Slide de titre

- Utiliser la classe `lead`
- Texte centré

```markdown
<!-- _class: lead -->

# Titre

## Sous-titre
```

---

# 8. Images

- Ajouter :

```markdown
![logo](images/logo.png)
```

- Taille :

```markdown
![w:300](images/logo.png)
```

- Centrer (avec le style du fichier) :

```markdown
![center w:300](images/logo.png)
```

- Fond :

```markdown
![bg](images/fond.jpg)
```

---

# 9. Apparence et thèmes

- Thèmes inclus : `default`, `gaia`, `uncover`
- Changer de thème :

```markdown
theme: gaia
```

- Changer une couleur :

```markdown
---
marp: true
backgroundColor: #1e1e2e
color: #ffffff
---
```

- Une seule slide :

```markdown
<!-- _backgroundColor: #ffeaa7 -->
<!-- _color: #2d3436 -->
```

---

# 10. Pagination, header, footer

- **Numéro de page** :

```markdown
paginate: true
```

- **Header / footer** :

```markdown
header: "Mon cours"
footer: "© 2026"
```

- Masquer sur une slide :

```markdown
<!-- _paginate: false -->
```

---

# 11. Export

**Dans VS Code**
- `Ctrl+Shift+P`
- **Marp: Export Slide Deck...**
- Choisir **PDF**, **PPTX** ou **HTML**

**En ligne de commande**

```bash
marp presentation.md --pdf
marp presentation.md --pptx
marp presentation.md --html
```

---

<!-- _class: lead -->

# 12. Checklist

- `marp: true` en haut
- Slides séparées par `---`
- Images dans `images/`
- Export PDF / PPTX / HTML