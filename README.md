<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0f,50:001a33,100:003366&height=120&section=header&animation=fadeIn" width="100%"/>
</div>

<div align="center">

```
██╗   ██╗ ██╗  ███████╗███████╗███████╗███╗   ██╗
╚██╗ ██╔╝██╔╝  ██╔════╝██╔════╝██╔════╝████╗  ██║
 ╚████╔╝██╔╝   ███████╗█████╗  █████╗  ██╔██╗ ██║
  ╚██╔╝ ██╔╝   ╚════██║██╔══╝  ██╔══╝  ██║╚██╗██║
   ██║  ██╔╝   ███████║███████╗███████╗██║ ╚████║
   ╚═╝  ╚═╝    ╚══════╝╚══════╝╚══════╝╚═╝  ╚═══╝
```

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&size=15&duration=2800&pause=900&color=00A8FF&center=true&vCenter=true&width=750&lines=Reverse+Engineer+%7C+API+Method+Researcher+%7C+Protocol+Analyst;I+find+endpoints+devs+never+meant+to+expose.;Desktop+RE+%E2%80%94+Web+App+Analysis+%E2%80%94+Traffic+Deconstruction;If+it+communicates%2C+I+can+map+it.+If+it+hides%2C+I+find+it.;%22Why+give+up%3F+Who+fights+for+the+others%3F%22)](https://git.io/typing-svg)

<br>

![](https://img.shields.io/badge/ROLE-Reverse%20Engineer-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/FOCUS-API%20Method%20Discovery-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/TARGET-Desktop%20%7C%20Web%20%7C%20Protocols-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/BASE-KSA%20%2F%20India-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://komarev.com/ghpvc/?username=y4seen&color=00A8FF&style=flat-square&label=PROFILE+VIEWS)

</div>

---

<div align="center">

## `[ OPERATOR PROFILE ]`

</div>

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│   ALIAS      →  L . | #y4                                                   │
│   HANDLE     →  y4seen                                                      │
│   SITE       →  y4seen.lol                                                  │
│   AGE        →  17 y                                                        │
│   LOCATION   →  KSA / India                                                 │
│   OS         →  Kali Linux  ·  Windows                                      │
│                                                                              │
│   WHAT I DO  →  I reverse engineer desktop software and web applications.   │
│              →  I find APIs, methods, and endpoints devs never documented.   │
│              →  I read network traffic until the protocol has no secrets.    │
│              →  I map how software talks — then I speak its language.        │
│                                                                              │
│   "Why don't you give up?"                                                   │
│   "Because if I do... Who's gonna fight for the others?"                    │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘
```

---

## ⚙️ `REVERSE ENGINEERING`

> My primary discipline. I take software apart at the seams to understand what it actually does — not what the docs say it does.

<br>

**`› Desktop Application Analysis`**

I analyze compiled desktop software statically and dynamically — tracing execution flow, identifying obfuscation layers, locating hardcoded logic, and reconstructing intent from disassembly. My goal is always a complete functional map: what the software does, what it hides, and how it communicates.

```
Static Analysis Pipeline:
  [1] Load binary into Ghidra / x64dbg
  [2] Identify entry points, key functions, crypto routines
  [3] Rename symbols, annotate logic, rebuild data structures
  [4] Trace API call chains to understand external communication
  [5] Locate: hardcoded strings, keys, URLs, internal method names
  [6] Document findings as a clean functional spec
```

<br>

**`› Web Application & JavaScript Reverse Engineering`**

Modern web apps hide enormous amounts of logic in minified, obfuscated JS bundles. I deobfuscate, reconstruct, and analyze client-side code to expose internal API contracts, auth logic, hidden parameters, and methods the frontend uses but never publicizes.

```javascript
// Deobfuscation approach — reconstruct readable logic from minified bundles
// Step 1: beautify
// prettier --write bundle.min.js

// Step 2: identify and rename mangled symbols by behavior
// Before:
const a = b(c, d, 0x1f4);
// After tracing: 
const token = generateHmac(secret, payload, 500);

// Step 3: extract all internal API calls
// grep -oP '(?<=fetch\(")[^"]+' bundle.js
// grep -oP '(?<=axios\.(get|post|put)\(")[^"]+' bundle.js

// Step 4: map auth header construction — find how tokens are built
// look for: headers["Authorization"], X-Api-Key, X-Request-Signature
```

<br>

**`› Protocol & Network Traffic Analysis`**

I intercept and dissect network communication to understand how software actually talks — including encrypted traffic, custom binary protocols, and undocumented message formats. Wireshark and Burp are my primary lenses, scripting handles the rest.

```
Traffic Analysis Process:
  [1] Capture  →  Wireshark full PCAP / Burp Suite proxy intercept
  [2] Decrypt  →  HTTPS via custom CA, MITM for thick clients
  [3] Identify →  Message framing: REST, WebSocket, binary, custom
  [4] Parse    →  Decode payloads: JSON, protobuf, custom serialization
  [5] Map      →  Build complete request/response schema per endpoint
  [6] Replay   →  Forge raw requests to confirm understanding
  [7] Script   →  Automate via Python or Node.js client
```

```python
# Automated request replayer — forge and test captured API calls
import requests, json

session = requests.Session()
session.headers.update({
    "Authorization": "Bearer <extracted_token>",
    "X-Request-ID":  "<reconstructed_value>",
    "Content-Type":  "application/json",
})

# Replay a captured internal method call
payload = {
    "method": "internal.getAccountData",   # undocumented method
    "params": { "userId": 1337 },
    "id":     1
}

r = session.post("https://target.com/api/rpc", json=payload)
print(json.dumps(r.json(), indent=2))
```

---

## 🌐 `API METHOD DISCOVERY`

> APIs always have more surface than they expose. My job is finding the rest.

This is my signature discipline. I locate and map undocumented API methods, hidden endpoints, and internal communication patterns that developers never intended to be public-facing.

<br>

**`› How I Find What's Not Documented`**

```
Multi-Vector Discovery:
  ├── JS Bundle Mining
  │     Deobfuscate frontend bundles → extract all fetch/axios/XHR calls
  │     Grep for route strings, method names, param keys, header names
  │
  ├── Traffic Capture
  │     Proxy the live application through Burp Suite
  │     Record every request made during normal usage flows
  │     Identify undocumented parameters sent silently by the client
  │
  ├── Desktop Binary Analysis
  │     Strings scan on executables → harvest embedded URL paths
  │     Trace HTTP client calls in disassembly → map all call sites
  │     Identify internal RPC method tables and enum values
  │
  ├── Version Diffing
  │     Compare old vs. new client builds → find removed/added routes
  │     Dead routes on servers often still respond with weaker auth
  │
  └── Swagger / OpenAPI Hunting
        /api-docs  /swagger.json  /openapi.yaml  /v2/api-docs
        Internal docs exposed on staging, CDN, or misconfigured routes
```

<br>

**`› API Authentication Reverse Engineering`**

I reconstruct exactly how authentication works — token generation, signing algorithms, session mechanics, and authorization chains — by reading the code and traffic rather than the docs.

```python
# Reconstruct a custom HMAC request signature from JS source
import hmac, hashlib, time, json

# Recovered from deobfuscated bundle:
# signature = HMAC-SHA256(secret_key, method + ":" + timestamp + ":" + body_hash)

def build_signature(secret: str, method: str, body: dict) -> dict:
    ts        = str(int(time.time()))
    body_str  = json.dumps(body, separators=(',', ':'))
    body_hash = hashlib.sha256(body_str.encode()).hexdigest()
    
    message   = f"{method}:{ts}:{body_hash}"
    sig       = hmac.new(secret.encode(), message.encode(), hashlib.sha256).hexdigest()
    
    return {
        "X-Timestamp":  ts,
        "X-Signature":  sig,
        "Content-Type": "application/json",
    }

# Now we can call the undocumented endpoint directly
headers = build_signature(RECOVERED_SECRET, "POST", payload)
```

<br>

**`› WebSocket & RPC Method Discovery`**

Many modern apps use WebSocket connections with internal RPC-style method dispatch. I intercept these streams, enumerate method names, and map the full call surface.

```
WS Analysis:
  → Intercept WebSocket frames in Burp Suite
  → Identify message envelope structure (JSON-RPC, custom, protobuf)
  → Enumerate method names from JS source and live traffic
  → Test undocumented methods directly via ws client
  → Map parameter types per method by fuzzing and observing errors
```

```javascript
// WebSocket method enumerator (Node.js)
const WebSocket = require('ws');

const METHODS = [
  'user.getProfile', 'user.getPrivate', 'admin.listUsers',
  'internal.getConfig', 'system.status', 'account.getBalance'
  // harvested from deobfuscated JS bundle
];

const ws = new WebSocket('wss://target.com/ws', {
  headers: { 'Authorization': `Bearer ${TOKEN}` }
});

ws.on('open', () => {
  METHODS.forEach((method, i) => {
    ws.send(JSON.stringify({ id: i, method, params: {} }));
  });
});

ws.on('message', (data) => {
  const res = JSON.parse(data);
  if (!res.error) console.log(`[FOUND] ${METHODS[res.id]} -> `, res.result);
});
```

---

## 🕵️ `OSINT`

Passive intelligence gathering to map targets before active analysis begins.

```
My OSINT Stack:
  ├── Subdomain Enumeration    amass · subfinder · dnsx · crt.sh
  ├── Infrastructure Mapping   shodan · censys · fofa
  ├── Historical Data          Wayback Machine · URLScan · CommonCrawl
  ├── Identity Research        maigret · holehe · sherlock
  └── Leak Intelligence        credential and source correlation
```

---

## 🛠️ `TOOLCHAIN`

<div align="center">

| Category | Tools |
|:---|:---|
| **Disassembly / RE** | Ghidra · x64dbg · dnSpy · Detect-It-Easy |
| **Traffic Analysis** | Burp Suite · Wireshark · mitmproxy · Fiddler |
| **JS Analysis** | Prettier · AST Explorer · Chrome DevTools · de4js |
| **OSINT** | amass · shodan · subfinder · maigret · holehe |
| **Scripting** | Python 3 · Node.js · Bash |
| **API Testing** | Burp Repeater · Postman · curl · custom scripts |
| **Platforms** | Kali Linux · Windows |

</div>

---

## 💻 `STACK`

<div align="center">

![Python](https://img.shields.io/badge/Python-0a0a0f?style=for-the-badge&logo=python&logoColor=00A8FF)
![Node.js](https://img.shields.io/badge/Node.js-0a0a0f?style=for-the-badge&logo=nodedotjs&logoColor=00A8FF)
![JavaScript](https://img.shields.io/badge/JavaScript-0a0a0f?style=for-the-badge&logo=javascript&logoColor=00A8FF)
![Bash](https://img.shields.io/badge/Bash-0a0a0f?style=for-the-badge&logo=gnubash&logoColor=00A8FF)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-0a0a0f?style=for-the-badge&logo=burpsuite&logoColor=00A8FF)
![Wireshark](https://img.shields.io/badge/Wireshark-0a0a0f?style=for-the-badge&logo=wireshark&logoColor=00A8FF)

</div>

Python and Node.js for scripting and automation. Burp Suite for intercepting and replaying traffic. Wireshark for raw protocol analysis. Ghidra and x64dbg for binary work. Custom tooling when nothing off-the-shelf fits the job.

---

## 📊 `STATS`

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=y4seen&show_icons=true&theme=dark&hide_border=true&title_color=00A8FF&icon_color=00A8FF&text_color=c9d1d9&bg_color=0a0a0f&ring_color=00A8FF&count_private=true" height="165"/>
&nbsp;&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=y4seen&layout=compact&theme=dark&hide_border=true&title_color=00A8FF&text_color=c9d1d9&bg_color=0a0a0f&langs_count=6" height="165"/>

<br><br>

<img src="https://github-readme-streak-stats.herokuapp.com?user=y4seen&theme=dark&hide_border=true&background=0a0a0f&ring=00A8FF&fire=00A8FF&currStreakLabel=00A8FF&sideLabels=00A8FF&dates=555555" height="165"/>

</div>

---

## 🔭 `CURRENT FOCUS`

```python
current_work = [
    "Desktop binary analysis — mapping undocumented internal method tables",
    "JS deobfuscation tooling — automated bundle analysis pipeline",
    "Protocol reconstruction — decoding custom binary message formats",
    "API method enumeration — building systematic discovery methodology",
]

learning = [
    "Advanced traffic analysis — encrypted protocol reconstruction",
    "Assembly reading — faster static analysis without decompiler crutch",
    "Automation — chaining RE steps into repeatable pipelines",
]
```

---

## 📡 `CONTACT`

<div align="center">

[![Website](https://img.shields.io/badge/y4seen.lol-0a0a0f?style=for-the-badge&logo=firefoxbrowser&logoColor=00A8FF)](https://y4seen.lol)
&nbsp;
[![Discord](https://img.shields.io/badge/Discord-0a0a0f?style=for-the-badge&logo=discord&logoColor=00A8FF)](https://discord.com)
&nbsp;
[![Email](https://img.shields.io/badge/Email-0a0a0f?style=for-the-badge&logo=protonmail&logoColor=00A8FF)](mailto:contact@y4seen.lol)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:003366,50:001a33,100:0a0a0f&height=100&section=footer" width="100%"/>

```
┌──(y4㉿kali)-[~]
└─$ echo "SYSTEM SECURE. SESSION ACTIVE. ANALYSIS ONGOING."

SYSTEM SECURE. SESSION ACTIVE. ANALYSIS ONGOING.
```

*Every API has hidden methods. Every binary has secrets. I find both.*

</div>
