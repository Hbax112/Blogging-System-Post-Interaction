# Blogging-System-Post-Interaction

A collaborative blogging system where two users manage different parts:

- **User 1**: Manages blog posts (create, edit, view, delete).
- **User 2**: Interacts with blog posts (add comments, like, love, dislike).

## Data Structure
- **Article**: 
  - `string title`
  - `string author`
  - `string content`
  - `int date`
  - `Comment[] comments`
  - `int like`, `int dislike`, `int love`
  
- **Comment**: 
  - `string text`
  - `string author`
  - `int date`
  - `int like`, `int dislike`, `int love`

## File Structure
- **articol.txt**: 
  - Stores details about posted articles:
    ```txt
    <numar_articole>
    <titlu_articol1><autor_articol1><continut_articol1><data_articol1><reactii_articol1>
    ...
    ```
    
- **comentarii.txt**: 
  - Stores comments and reactions for articles:
    ```txt
    <index_articol1/titlu_articol1><lista_comentarii_articol1>
    <nr_likeruri_comentariu1><nr_dislike_comentariu1><nr_love_comentariu1>
    ...
    ```

## Interaction with Executables

### App 1 (Post Management):
- View all posts: 
  `./app_1.exe vizualizare_articole`
- Add a post: 
  `./app_1.exe adaugare_articol <titlu> <autor> <continut> <data>`
- Edit a post: 
  `./app_1.exe editare_articol <titlu> <autor> <continut> <data>`
- Delete a post: 
  `./app_1.exe stergere_articol <titlu> <autor>`

### App 2 (Interaction):
- View comments:
  `./app_2.exe vizualizare_comentarii <titlu>`
- Add a comment:
  `./app_2.exe adaugare_comentariu <titlu> <text> <autor> <data>`
- Delete a comment:
  `./app_2.exe stergere_comentariu <titlu> <index_comentariu>`
- Like/Dislike/Love a post or comment:
  `./app_2.exe acordare_like/acordare_dislike/acordare_love <articol/comentariu> <titlu> <autor>`

