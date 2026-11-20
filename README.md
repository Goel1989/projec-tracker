# Project Tracker / Suivi de projet

A project-tracking tool that runs as a **single HTML file**, with your data kept in a **CSV file**.
No server, no installation, no admin rights: double-click the file and it opens in your browser.

*Outil de suivi de projet en un seul fichier HTML, qui garde vos données dans un fichier CSV. Sans serveur, sans installation, sans droits administrateur. [Description en français plus bas.](#français)*

---

## Files

| File | Description |
|---|---|
| `project-tracker.html` | English version |
| `suivi-projet-blanc.html` | French version (*version française*) |
| `exemple-suivi-projet-100-actions.csv` | Example data: 100 fictitious actions from a car development project, 12 work packages |

## Features

- **Overview**: an automatic project status (all good / to watch / alert) and overall progress. It also lists the actions that need attention and the deadlines in the next 14 days, and gives a status for each work package.
- **Actions table**: all columns, with filters by work package, status, priority and owner, plus search and sorting.
- **Dated follow-ups**: lines such as `dd/mm/yy : text` in the follow-up column are split by date when imported. You can add or edit each one separately.
- **Status rule**: an action turns red only when its due date (or rescheduled date) has passed and it is not finished.
- **Follow-up report**: shows how actions changed over a chosen period, ready to paste into a weekly email.
- **Gantt planning**:
  - opens in a separate window;
  - 16:9 pages with several work packages per page, never split across two pages;
  - full action names, and one date zoom shared by all pages.
- **Exports**:
  - PowerPoint (`.pptx`) and JPEG of the Gantt pages;
  - a dated CSV copy (`…-YYYY-MM-DD_HHhMMmSS.csv`).
- **Clear all**: resets the tool so you can load another file.

## How to use

1. Download `project-tracker.html` (or the French version) and open it in **Chrome** or **Edge**.
2. Open your CSV, using one of these two methods:
   - **Drag the CSV file** from File Explorer into the window, then click **Turn on automatic saving**. Every change (new action, new follow-up, progress update) is then written straight to the file, and a green badge shows the time of the last save.
   - Or click **Open a CSV file**. If your browser does not allow writing to files opened from disk, changes are kept in the browser and a banner reminds you to use **Download a copy**. **Data that has not been downloaded may be lost.**
3. To try the tool, open `exemple-suivi-projet-100-actions.csv`.

### CSV format

- Separator `;`, UTF-8 encoding. Opens directly in Excel.
- Columns (French or English headers are accepted):
  `N°Action; Chantier; Actions; Responsable; Version de structure; Délai; Priorité; Date reprogrammée; Finalisé; Suivi; Date de début; Avancement`
- Dates are written `dd/mm/yyyy`.
- In the **Suivi** (follow-up) column, put one line per follow-up, starting with its date: `dd/mm/yy : text`.

### Limitations

- Automatic saving to the file uses the browser's *File System Access API*, which works in Chrome and Edge only. Some company policies block it; in that case use **Download a copy**.
- Data that is not linked to a file is kept in the browser's local storage, which is cleared if browser data is erased.

## Privacy

Everything runs locally in your browser. No data is sent anywhere.

## License

[MIT](LICENSE): free to use, modify and share.

---

## Français

Outil de suivi de projet en **un seul fichier HTML**, qui garde vos données dans un **fichier CSV**. Sans serveur, sans installation, sans droits administrateur.

### Fonctions

- **Vue globale** : un verdict automatique (tout va bien / à surveiller / alerte) et l'avancement global. La vue liste aussi les actions qui demandent votre attention et les échéances à 14 jours, et donne un état par chantier.
- **Tableau des actions** : toutes les colonnes, avec des filtres par chantier, voyant, priorité et responsable, une recherche et un tri.
- **Suivis datés** : les lignes `jj/mm/aa : texte` de la colonne Suivi sont séparées par date à l'ouverture. Chaque suivi s'ajoute et se modifie séparément.
- **Règle du voyant** : rouge seulement si l'échéance (ou la date reprogrammée) est dépassée et que l'action n'est pas finalisée.
- **Rapport de suivi** : l'évolution des actions sur une période choisie, prête à coller dans un mail.
- **Planning Gantt** :
  - dans une fenêtre séparée ;
  - pages 16:9 avec plusieurs chantiers par page, jamais coupés ;
  - noms d'actions complets et zoom de dates commun à toutes les pages.
- **Exports** :
  - PowerPoint (`.pptx`) et JPEG du Gantt ;
  - copie CSV datée.
- **Tout effacer** : remet l'outil à zéro pour charger un nouveau fichier.

### Utilisation

1. Ouvrez `suivi-projet-blanc.html` dans **Chrome** ou **Edge**.
2. Ouvrez votre CSV, avec l'une de ces deux méthodes :
   - **Glissez votre fichier CSV** depuis l'Explorateur dans la fenêtre, puis cliquez sur **Activer l'enregistrement automatique**. Chaque modification est alors enregistrée dans le fichier, et une pastille verte indique l'heure du dernier enregistrement.
   - Ou cliquez sur **Ouvrir un fichier CSV**. Si le navigateur n'autorise pas l'écriture dans le fichier, les modifications sont gardées dans le navigateur : utilisez **Télécharger une copie** pour les sauvegarder. **Sans téléchargement, les données peuvent être perdues.**
3. Pour essayer l'outil, ouvrez `exemple-suivi-projet-100-actions.csv`.

### Confidentialité

Tout fonctionne en local dans votre navigateur ; aucune donnée n'est envoyée.

### Licence

[MIT](LICENSE) : libre d'utilisation, de modification et de diffusion.
