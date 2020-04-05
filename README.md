# codename
Codename game web app

## TODOLIST

### BACKEND

#### API routes
- POST /games \
  Create new game : generate slug and board

- GET /games/:slug \
  Fetch game details by slug

- POST /games/:slug/play \
  Update game with player choice

- POST /games/:slug/renew \
  Renew game : generate new board

#### Model / DB
- Game { slug: String, users: Array, board: Array[25] } \
with 
  - user { name: String, team: ‘red|blue’ }
  - board array of { word: String, played: Boolean, type: ‘blue|red|forbidden|neutral’ }

#### Socket
Send socket on each action 

### FRONTEND
- Home \
  Game creation form
  
- Game \
  Spy view \
  Detective view
 
 
## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```
