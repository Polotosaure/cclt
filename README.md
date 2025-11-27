# Site Web CCLT Espérance

Site web officiel du Centre de Continuité du lien thérapeutique (CCLT) de l'Espérance à Rennes.

## À propos

Le CCLT Espérance est un centre de soins thérapeutiques qui accueille des adultes en détresse psychologique depuis 2008. Ce site web présente les services et l'approche thérapeutique du centre.

## Structure du Site

Le site est composé de 4 pages principales :

- **Accueil** (`index.html`) - Page d'accueil avec présentation générale
- **Présentation** (`presentation.html`) - Histoire et philosophie du centre
- **Nos Services** (`services.html`) - Détails des services proposés
- **Contact** (`contact.html`) - Formulaire de contact et informations pratiques

## Fonctionnalités

- Design responsive adapté à tous les écrans (mobile, tablette, desktop)
- Menu de navigation interactif avec hamburger menu sur mobile
- Formulaire de contact avec validation
- Animations au défilement
- Design moderne et professionnel

## Technologies Utilisées

- HTML5
- CSS3 (avec variables CSS pour une personnalisation facile)
- JavaScript (Vanilla JS, sans dépendances)

## Installation et Utilisation

### Option 1 : Ouverture directe

Ouvrez simplement le fichier `index.html` dans votre navigateur web.

### Option 2 : Serveur local

Pour un meilleur développement, utilisez un serveur local :

#### Avec Python 3 :
```bash
python -m http.server 8000
```

#### Avec Node.js (http-server) :
```bash
npx http-server
```

#### Avec PHP :
```bash
php -S localhost:8000
```

Puis ouvrez votre navigateur à l'adresse : `http://localhost:8000`

## Personnalisation

### Couleurs

Les couleurs principales sont définies dans le fichier `styles.css` avec des variables CSS :

```css
:root {
    --primary-color: #2c5f8d;
    --secondary-color: #4a90c9;
    --accent-color: #7fb3d5;
    /* ... autres couleurs */
}
```

Modifiez ces valeurs pour changer le thème du site.

### Contenu

Pour modifier le contenu :

1. Ouvrez le fichier HTML concerné dans un éditeur de texte
2. Modifiez le texte entre les balises HTML
3. Sauvegardez et rechargez la page dans votre navigateur

## Formulaire de Contact

Le formulaire de contact est actuellement configuré pour fonctionner en mode démo (les données sont affichées dans la console du navigateur).

Pour le connecter à un serveur backend :

1. Ouvrez `script.js`
2. Localisez la fonction de soumission du formulaire (ligne ~37)
3. Remplacez le `console.log` par un appel AJAX vers votre serveur

Exemple avec Fetch API :
```javascript
fetch('votre-url-backend/contact', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(formData),
})
.then(response => response.json())
.then(data => {
    showFormMessage('Message envoyé avec succès !', 'success');
})
.catch(error => {
    showFormMessage('Erreur lors de l\'envoi du message.', 'error');
});
```

## Structure des Fichiers

```
cclt/
├── index.html          # Page d'accueil
├── presentation.html   # Page de présentation
├── services.html       # Page des services
├── contact.html        # Page de contact
├── styles.css          # Feuille de styles
├── script.js           # Scripts JavaScript
└── README.md          # Ce fichier
```

## Compatibilité Navigateurs

Le site est compatible avec :

- Chrome (dernières versions)
- Firefox (dernières versions)
- Safari (dernières versions)
- Edge (dernières versions)
- Opera (dernières versions)

## Déploiement

Pour déployer le site en production :

### GitHub Pages
1. Créez un dépôt GitHub
2. Poussez les fichiers
3. Activez GitHub Pages dans les paramètres

### Netlify
1. Glissez-déposez le dossier sur Netlify
2. Ou connectez votre dépôt Git

### Serveur traditionnel
1. Uploadez tous les fichiers via FTP
2. Assurez-vous que `index.html` est dans le répertoire racine

## Support et Contact

Pour toute question concernant le site web, veuillez contacter le CCLT Espérance via les coordonnées indiquées sur la page Contact.

## Licence

Ce site est la propriété du CCLT Espérance - Tous droits réservés.

---

Développé pour le Centre de Continuité du lien thérapeutique de l'Espérance, Rennes.
