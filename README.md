<div align="center">
  <img width="256" height="256" alt="icon" src="https://github.com/user-attachments/assets/4b95e4bd-9979-4ef2-9793-70d7821d0f7f" />
  <p><h3>SOPA</h3></p>
  <p>Clube penguin para esquisitos.</p>
</div>

---

### Sobre

- SOPA surgiu de uma necessidade da [Soup Group](https://kiteline.itch.io/soup-rooms) de criar uma versão universal e de fácil acesso do jogo obscuro japonês [soup0.9](https://yh.16dimensional.com/soup/), um _walking sim_ inspirado no [LSD Dream Emulator](https://en.wikipedia.org/wiki/LSD:_Dream_Emulator).
- Nós juntamos essa necessidade com a vontade dos membros do COSMOS de criar um chatroom meio anos 2000 inspirado no [World.com](https://en.wikipedia.org/wiki/Worlds.com), [SAPARi](https://weedeater.neocities.org/sapari/) e no aclamado [Club Penguin](https://en.wikipedia.org/wiki/Club_Penguin).

### Arquitetura

- `backend`
  - Usa o FastAPI + PostgreSQL para dados persistentes junto com WebRTC para dados mais dinâmicos como chats e posições de usuários no mapa.
  - Autenticação de usuários usando Firebase ou algum outro serviço terceirizado (incerto, pesquisar mais sobre dps).
- `frontend`
  - Paginas renderizadas usando templates pelo próprio backend.
  - Partes mais dinâmicas da UI são montados usando [HTMX](https://htmx.org/) e [AlpineJS](https://alpinejs.dev/).
  - 3D renderizado usando ThreeJS.
- `devops`
  - Deploy do banco de dados, do storage e do backend feito usando o [Railway](https://railway.com/).
 
### Tarefas

- [ ] Prototipagem de chatroom basica usando WebRTC + FastAPI
- [ ] Montar arquitetura por trás das chatrooms, seus assets e dados
