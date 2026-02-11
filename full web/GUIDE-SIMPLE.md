# Guide de Mise à Jour - Site al moubadara (Version Simplifiée)

## 📋 Système de Données Intégrées

Les données (événements et actualités) sont **intégrées directement dans les fichiers HTML**.
Pas besoin de serveur web - ça fonctionne directement en ouvrant les fichiers !

---

## 🎯 Comment Ajouter un Nouvel Événement

### Étape 1 : Ouvrir le fichier
Ouvrez le fichier `evenementm7rez-dynamic.html` avec un éditeur de texte

### Étape 2 : Trouver la section des données
Cherchez cette ligne dans le code :
```javascript
const eventsData = {
    "events": [
```

### Étape 3 : Ajouter votre événement
Ajoutez un nouvel événement AVANT le dernier `]` :

```javascript
,
{
    "id": 4,
    "title": "Nom de votre événement",
    "date": "25 Juin 2026",
    "shortDescription": "Description courte",
    "fullDescription": "Description complète",
    "image": "nom-image.jpg",
    "location": "Lieu",
    "time": "10:00 - 16:00",
    "organizer": "Organisateur"
}
```

**Important :** N'oubliez pas la virgule `,` avant votre nouvel événement !

### Étape 4 : Mettre à jour aussi event-details.html
Vous devez ajouter le MÊME événement dans le fichier `event-details.html` à l'identique.

---

## 📰 Comment Ajouter une Actualité

### Fichiers à modifier (les 2 fichiers) :
1. `government-website.html` (page d'accueil)
2. `news-details.html` (page détails)

### Dans m7rez1.html :
Cherchez :
```javascript
const newsData = [
```

Ajoutez :
```javascript
,
{
    "id": 3,
    "title": "Titre actualité",
    "date": "11 Février 2026",
    "summary": "Résumé court",
    "content": "Contenu complet",
    "image": ""
}
```

### Dans news-details.html :
Faites LA MÊME chose - ajoutez la même actualité au même endroit.

---

## 🖼️ Comment Ajouter des Images

1. Placez votre image dans le même dossier que les fichiers HTML
2. Dans le code, utilisez juste le nom : `"image": "mon-image.jpg"`
3. Si pas d'image : `"image": ""`

---

## ✏️ Comment Modifier un Événement/Actualité

1. Trouvez l'événement par son ID dans le code
2. Modifiez le texte entre les guillemets
3. **Important :** Modifiez dans TOUS les fichiers concernés :
   - Pour événements : `evenementm7rez-dynamic.html` ET `event-details.html`
   - Pour actualités : `government-website.html` ET `news-details.html`

---

## 📁 Fichiers du Site

### Pages principales :
- `government-website.html` → Page d'accueil (avec actualités)
- `evenementm7rez-dynamic.html` → Liste des événements
- `event-details.html` → Détails d'un événement
- `news-details.html` → Détails d'une actualité
- `contactm7rez.html` → Page contact
- `plusm7rez.html` → Plus d'information

### Fichiers annexes :
- `icon.png` → Logo du site
- `m7rezimag.JPEG` → Image d'accueil (à ajouter)

---

## ⚠️ Règles TRÈS Importantes

### 1. Les IDs doivent être uniques
- Événement 1 → id: 1
- Événement 2 → id: 2
- NE PAS réutiliser le même ID !

### 2. Synchroniser les fichiers
Quand vous ajoutez/modifiez :
- **Événement** → Modifier `evenementm7rez-dynamic.html` ET `event-details.html`
- **Actualité** → Modifier `government-website.html` ET `news-details.html`

### 3. Ne pas oublier les virgules
```javascript
{ événement 1 },   ← virgule ici
{ événement 2 },   ← virgule ici
{ événement 3 }    ← PAS de virgule sur le dernier
```

### 4. Guillemets doubles obligatoires
✅ Bon : `"title": "Mon titre"`
❌ Mauvais : `'title': 'Mon titre'`

---

## 🔧 Que Faire Si Ça Ne Marche Pas

### Le site affiche "Chargement..." qui ne finit jamais
→ Erreur de syntaxe dans le code
→ Vérifiez les virgules et les guillemets

### Un événement n'apparaît pas
→ Vérifiez que vous l'avez ajouté dans les 2 fichiers
→ Vérifiez l'ID est unique

### Les liens ne fonctionnent pas
→ Vérifiez que tous les fichiers HTML sont dans le même dossier

---

## 📝 Exemple Complet d'Ajout

### Avant (dans evenementm7rez-dynamic.html) :
```javascript
const eventsData = {
    "events": [
        {
            "id": 1,
            "title": "Premier événement",
            ...
        },
        {
            "id": 2,
            "title": "Deuxième événement",
            ...
        }
    ]
};
```

### Après (ajout d'un 3ème événement) :
```javascript
const eventsData = {
    "events": [
        {
            "id": 1,
            "title": "Premier événement",
            ...
        },
        {
            "id": 2,
            "title": "Deuxième événement",
            ...
        },
        {
            "id": 3,
            "title": "Nouveau événement",
            "date": "30 Juin 2026",
            "shortDescription": "Courte description",
            "fullDescription": "Description longue",
            "image": "",
            "location": "Centre ville",
            "time": "14:00 - 18:00",
            "organizer": "Mairie"
        }
    ]
};
```

**N'oubliez pas de faire la même chose dans `event-details.html` !**

---

## ✅ Liste de Vérification

Avant de fermer les fichiers, vérifiez :
- [ ] L'ID est unique
- [ ] Toutes les virgules sont au bon endroit
- [ ] Les guillemets doubles sont utilisés
- [ ] Vous avez modifié TOUS les fichiers concernés
- [ ] Le site s'ouvre correctement dans le navigateur

---

## 💡 Astuce Pro

Faites une copie de sauvegarde de vos fichiers avant chaque modification !
Comme ça, si vous faites une erreur, vous pouvez revenir en arrière.

---

**Besoin d'aide ?** Contactez votre développeur web !
