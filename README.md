# Web Sistemak · Bezerotik zerbitzarira

Klaseko adibideen biltegia: localStorage, Node.js, npm, modulu integratuak (`os`, `path`, `fs`) eta asinkronia (callbackak, promesak eta `async/await`).

## Nola hasi

**GitHub Codespaces (gomendatua).** Sakatu **Code → Codespaces → Create codespace on main**. Node.js eta npm instalatuta datoz; ez da ezer instalatu behar.

**Zure ordenagailuan.** Node.js 22 behar duzu (adibidez, `nvm install 22` eginda). Gero:

```bash
git clone https://github.com/ialdabe/ws-backend-sarrera.git
cd ws-backend-sarrera
node -v
npm -v
```

## Urratsak (adarrak)

Klaseko urrats bakoitzak bere adarra du, eta adar bakoitzak aurrekoaren edukia du gehi urrats berria. `main` adarra abiapuntua da: proba-fitxategiak bakarrik ditu.

| Adarra | Edukia | Diapositibak |
|---|---|---|
| `main` | Abiapuntua: `datuak.txt`, `a.txt`, `b.txt` | — |
| `01-kaixo-mundua` | `zerbitzaria.js`: HTTP zerbitzari sinplea | 27–28 |
| `02-serve` | `package.json`, `serve`, `public/index.html` (localStorage demoa), scriptak eta `.gitignore` | 29–33 |
| `03-moduluak` | `demo-os.js`, `demo-path.js` | 35–43 |
| `04-fs` | `irakurri-sync.js`, `irakurri-async.js`, `callback-hell.js` | 44–51 |
| `05-promesak` | `irakurri-promesak.js` eta erronka: `irakurri-biak.js` | 52–53 |
| `06-async-await` | Promesen erronkaren ebazpena, `irakurri-async-await.js` eta erronka: `irakurri-biak-await.js` | 54–56 |
| `07-ariketa` | async/await erronkaren ebazpena eta ariketaren abiapuntua: `inbentarioa.js` | 57–60 |
| `08-ariketa-ebazpena` | `inbentarioa.js` osatuta | 61 |
| `09-http-bideak` | `zerbitzaria-bideak.js`: bi bide `http` moduluarekin soilik | 62–65 |

Adar batera aldatzeko:

```bash
git switch 03-moduluak
```

Aldaketa propioak badituzu eta adarrez aldatu nahi baduzu, egin commit bat lehenago edo gorde `git stash` bidez.

## Komandoak urratsez urrats

```bash
# 01 · Kaixo mundua → ireki http://localhost:8000
node zerbitzaria.js

# 02 · serve
npm install          # node_modules sortzeko (package.json dagoenean)
npm start            # public karpeta → http://localhost:3000
npm run dev          # gauza bera, 3500 portuan

# 03 · Moduluak
node demo-os.js
node demo-path.js

# 04-06 · Fitxategiak eta asinkronia
node irakurri-sync.js
node irakurri-async.js
node irakurri-promesak.js
node irakurri-async-await.js

# 07-08 · Ariketa (datuak/inbentarioa.json sortzen du)
node inbentarioa.js

# 09 · Bi bide → / eta /inbentarioa (aurretik exekutatu inbentarioa.js)
node zerbitzaria-bideak.js
```

Zerbitzari bat gelditzeko: **Ctrl + C** terminalean.

Codespacesen, zerbitzari bat martxan jartzean **Ports** fitxan agertzen da portua; sakatu esteka nabigatzailean irekitzeko.
