---
cssclasses:
  - wide-page
campagne: dnd-ravnica
---
> [!multi-column]
> > [!blank-container]
> > # Personnages joueurs
> > ```dataview
> > TABLE joueur, nom, string("![" + image + "]()") as "Image"
> > FROM #pj 
> > WHERE campagne = this.campagne
> > ```
> 
> > [!blank-container]
> > # Sessions
> > 
> > ```dataview
> > TABLE 
> > FROM #session
> > WHERE campagne = this.campagne
> > ```
> > 
> > ```meta-bind-button
> > id: "create-session"
> > style: primary
> > label: "Créer une Session"
> > action:
> >   type: createNote
> >   folderPath: "2. Sessions"
> >   fileName: "Nouvelle Session"
> >   openNote: true
> > ```
