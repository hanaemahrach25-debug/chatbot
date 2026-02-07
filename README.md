# Trinity_AI_Assistant 

Un chatbot intelligent et élégant avec une interface utilisateur moderne, construit avec HTML, CSS et JavaScript vanilla.

![Trinity AI Chatbot](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

##  Démo en ligne

Essayez le chatbot : [https://hanaemahrach25-debug.github.io/chatbot/](https://hanaemahrach25-debug.github.io/chatbot/)

##  Caractéristiques

### Interface Utilisateur
- **Design moderne** avec effet glassmorphisme et animations fluides
- **Palette de couleurs professionnelle** : tons de bleus profonds et sophistiqués
- **Typographie distinctive** : Playfair Display pour les titres, Source Sans 3 pour le contenu
- **Responsive design** : s'adapte parfaitement aux écrans mobiles et desktop
- **Animations CSS** : transitions douces et micro-interactions raffinées

### Fonctionnalités
-  Système de messages avec horodatage
-  Indicateur de saisie animé (typing indicator)
-  Redimensionnement automatique du champ de texte
-  Suggestions de questions prédéfinies
-  Réponses contextuelles intelligentes basées sur des mots-clés
-  Support clavier : Enter pour envoyer, Shift+Enter pour nouvelle ligne
-  Indicateur de statut en ligne
-  Scroll automatique vers les nouveaux messages
-  Aucune dépendance externe requise

##  Installation et utilisation

### Méthode 1 : Utilisation directe
1. Téléchargez le fichier `chatbot.html`
2. Ouvrez-le dans votre navigateur web préféré
3. Commencez à discuter avec Trinity AI !

### Méthode 2 : Cloner le repository
```bash
# Cloner le repository
git clone https://github.com/hanaemahrach25-debug/chatbot.git

# Accéder au dossier
cd chatbot

# Ouvrir le fichier HTML dans votre navigateur
open chatbot.html  # macOS
start chatbot.html # Windows
xdg-open chatbot.html # Linux
```

### Méthode 3 : Serveur local
```bash
# Avec Python 3
python -m http.server 8000

# Avec Node.js (npx http-server)
npx http-server

# Puis ouvrir : http://localhost:8000/chatbot.html
```

##  Exemples de questions

Le chatbot peut répondre à différentes catégories de questions :

**Salutations**
- "Bonjour"
- "Salut"
- "Hello"

**Aide et capacités**
- "Quelles sont tes capacités ?"
- "Que peux-tu faire ?"
- "Aide-moi"

**Intelligence artificielle**
- "Comment fonctionne l'intelligence artificielle ?"
- "Qu'est-ce que le machine learning ?"
- "Parle-moi de l'IA"

**Organisation et productivité**
- "Aide-moi à organiser ma journée"
- "Comment être plus productif ?"
- "Conseils de planification"

##  Technologies utilisées

| Technologie | Description |
|------------|-------------|
| **HTML5** | Structure sémantique du chatbot |
| **CSS3** | Styles avancés avec gradients, animations, backdrop-filter |
| **JavaScript (Vanilla)** | Logique interactive sans framework |
| **Google Fonts** | Typographies Playfair Display et Source Sans 3 |

##  Structure du code

```
chatbot.html
├── <head>
│   ├── Métadonnées et configuration
│   └── Google Fonts (Playfair Display, Source Sans 3)
├── <style>
│   ├── Variables CSS personnalisées
│   ├── Styles de l'interface
│   ├── Animations et transitions
│   └── Media queries responsive
├── <body>
│   ├── Container principal
│   ├── Header avec titre et statut
│   ├── Zone de chat avec messages
│   └── Zone de saisie avec textarea et bouton
└── <script>
    ├── Gestion des messages
    ├── Système de réponses du bot
    ├── Animations et interactions
    └── Event listeners
```

##  Personnalisation

### Modifier les couleurs
Les couleurs sont définies dans les variables CSS au début du fichier :

```css
:root {
    --primary-dark: #0a1628;      /* Fond principal */
    --primary-blue: #1e3a5f;      /* Bleu principal */
    --accent-blue: #2c5f8d;       /* Bleu accent */
    --light-blue: #4a7ba7;        /* Bleu clair */
    --highlight: #64b5f6;         /* Surbrillance */
    --text-primary: #e8eef5;      /* Texte principal */
    --text-secondary: #b0c4de;    /* Texte secondaire */
}
```

### Ajouter de nouvelles réponses
Dans la section JavaScript, modifiez l'objet `botResponses` :

```javascript
const botResponses = {
    nouvelleCatégorie: [
        "Réponse 1 pour cette catégorie",
        "Réponse 2 pour cette catégorie"
    ]
};
```

Puis ajoutez la détection dans la fonction `getBotResponse()` :

```javascript
if (message.match(/mot-clé1|mot-clé2/)) {
    return botResponses.nouvelleCatégorie[Math.floor(Math.random() * botResponses.nouvelleCatégorie.length)];
}
```

### Modifier les polices
Changez les liens Google Fonts dans le `<head>` et les références dans le CSS :

```css
body {
    font-family: 'Votre-Police', sans-serif;
}
```

##  Fonctionnalités avancées possibles

Ce chatbot est conçu comme une base extensible. Voici quelques améliorations possibles :

- [ ] Intégration d'une vraie API d'IA (OpenAI, Anthropic, etc.)
- [ ] Sauvegarde de l'historique dans localStorage
- [ ] Mode clair/sombre avec switch
- [ ] Support des fichiers et images
- [ ] Export de conversation en PDF
- [ ] Traduction multilingue
- [ ] Synthèse vocale (Text-to-Speech)
- [ ] Reconnaissance vocale (Speech-to-Text)
- [ ] Boutons de réponses rapides
- [ ] Système de feedback utilisateur

##  Compatibilité

| Navigateur | Version minimale | Support |
|-----------|------------------|---------|
| Chrome | 88+ |  Complet |
| Firefox | 85+ |  Complet |
| Safari | 14+ |  Complet |
| Edge | 88+ |  Complet |
| Opera | 74+ |  Complet |

**Note** : Le chatbot utilise `backdrop-filter` qui nécessite un navigateur moderne.

##  Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le projet
2. Créez une **branche** pour votre fonctionnalité (`git checkout -b feature/NouvelleFonctionnalité`)
3. **Committez** vos changements (`git commit -m 'Ajout d'une nouvelle fonctionnalité'`)
4. **Push** vers la branche (`git push origin feature/NouvelleFonctionnalité`)
5. Ouvrez une **Pull Request**

##  Licence

Ce projet est sous licence MIT. Vous êtes libre de l'utiliser, le modifier et le distribuer.

```
MIT License

Copyright (c) 2025 Hanae Mahrach

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

##  Auteur

**Hanae Mahrach**
- GitHub: [@hanaemahrach25-debug](https://github.com/hanaemahrach25-debug)
- Projet: [Trinity AI Chatbot](https://hanaemahrach25-debug.github.io/chatbot/)

##  Remerciements

- Inspiration basée sur l'architecture **Trinity-Large-Preview** d'Arcee AI
- Design inspiré par les principes du **glassmorphisme** et du **design moderne**
- Typographies fournies par **Google Fonts**

##  Support

Si vous rencontrez des problèmes ou avez des questions :
- Ouvrez une [issue](https://github.com/hanaemahrach25-debug/chatbot/issues) sur GitHub
- Consultez la section des [discussions](https://github.com/hanaemahrach25-debug/chatbot/discussions)

---

 **Si ce projet vous plaît, n'hésitez pas à lui donner une étoile sur GitHub !**
