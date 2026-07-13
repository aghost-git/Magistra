# MagistrAgape - ENM Madagascar

Application PWA de preparation au concours de la magistrature a Madagascar.

## Deploiement sur GitHub Pages

1. Uploadez tout le contenu de ce dossier a la racine de votre repo GitHub
2. Settings -> Pages -> Source = branche main, dossier / (root)
3. Votre app sera disponible a https://VOTRE-USERNAME.github.io/NOM-DU-REPO/

## Configuration de l'IA (2 options)

### Option A - GRATUITE : Google Gemini (recommandee)
1. aistudio.google.com/apikey -> Create API Key (aucune carte bancaire)
2. Dans l'app : Profil -> "Cle API Google Gemini" -> collez et enregistrez
3. Utilise "gemini-flash-latest" avec thinking desactive (reponses directes en JSON)

### Option B - PAYANTE : Anthropic Claude
1. console.anthropic.com/settings/keys -> Create Key, ajoutez des credits
2. Dans l'app : Profil -> "Cle API Anthropic" -> collez et enregistrez

IMPORTANT : si une cle Anthropic est presente (meme sans credit), elle est
utilisee EN PRIORITE sur Gemini. Pour utiliser Gemini, laissez le champ
Anthropic completement vide et enregistrez-le vide.

## IMPORTANT: Tester dans l'apercu Claude.ai vs site deploye

- Dans l'apercu artefact Claude.ai : proxy gratuit integre, aucune cle requise.
- Sur le site deploye (GitHub Pages) : utilise VOTRE cle API configuree.

## En cas d'erreur IA

- "credit balance is too low" = ajoutez des credits Anthropic, ou passez a Gemini
- "no longer available" = le modele Google a change, signalez pour mise a jour
- "is not valid JSON" = reponse IA malformee, reessayez (corrige normalement
  par la desactivation du mode "thinking" de Gemini)
- "HTTP 401" / "API key not valid" = cle invalide, revérifiez dans Profil
- "HTTP 429" / quota = trop de requetes, attendez quelques minutes
