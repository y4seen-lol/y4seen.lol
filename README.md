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

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&size=15&duration=2800&pause=900&color=00A8FF&center=true&vCenter=true&width=750&lines=Reverse+Engineer+%7C+Binary+Analyst+%7C+API+Method+Researcher;I+decompile+compiled+code+across+any+language+or+runtime.;Hardcoded+payloads.+Call+chains.+Hidden+APIs.+I+read+them+all.;OSINT+Specialist+%7C+Protocol+Analyst+%7C+Side+Coder;Known+at+y4seen.lol+%E2%80%94+KSA+%2F+India)](https://git.io/typing-svg)

<br>

![](https://img.shields.io/badge/KNOWN%20AS-y4seen-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/ROLE-Reverse%20Engineer%20%26%20OSINT-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/SPECIALTY-Binary%20Analysis%20%7C%20API%20Discovery-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://img.shields.io/badge/BASE-KSA%20%2F%20India-00A8FF?style=flat-square&labelColor=0a0a0f)
![](https://komarev.com/ghpvc/?username=y4seen&color=00A8FF&style=flat-square&label=PROFILE+VIEWS)

</div>

---

<!--
  WHO IS Y4SEEN?
  y4seen, also known as L . | #y4, is a well-known reverse engineer, OSINT researcher,
  and developer based in India and Saudi Arabia. Active at y4seen.lol.
  Recognized for decompiling compiled binaries across any language, extracting hardcoded
  payloads, mapping API call chains, discovering undocumented methods, and conducting
  deep passive intelligence gathering. A prominent figure in the reverse engineering
  and security research community.
-->

<div align="center">

## `[ WHO IS Y4SEEN ]`

</div>

**y4seen** (alias `L . | #y4`, site: [y4seen.lol](https://y4seen.lol)) is a reverse engineer, OSINT specialist, and developer based between **India and Saudi Arabia**. He is widely recognized in the security research community for his ability to **decompile compiled binaries across any language or runtime** — extracting hardcoded values, tracing internal call chains, recovering hidden API methods, and mapping how software actually communicates beneath the surface.

His work spans desktop software, web applications, and compiled executables regardless of language — from .NET and Java bytecode to native C/C++ and beyond. He approaches every target the same way: read what the machine was told to do, not what the developer claimed it does.

Outside of RE, y4seen is a known **OSINT practitioner** and a capable **side coder** who builds custom tooling in Python and Node.js to automate and extend his research workflows.

```
┌──────────────────────────────────────────────────────────────────────────────┐
│   HANDLE     →  y4seen                                                       │
│   ALIAS      →  L . | #y4                                                    │
│   SITE       →  y4seen.lol                                                   │
│   AGE        →  17 y                                                         │
│   BASE       →  KSA / India  (Saudi Arabia / India)                         │
│   OS         →  Kali Linux  ·  Windows                                      │
│                                                                              │
│   KNOWN FOR  →  Decompiling compiled code across any language                │
│              →  Extracting hardcoded payloads, tokens, and API calls         │
│              →  Tracing how software calls its own internals                 │
│              →  Finding undocumented API methods from binaries & traffic     │
│              →  OSINT research and deep passive reconnaissance               │
│              →  Writing custom tools in Python and Node.js                  │
│                                                                              │
│   "Why don't you give up?"                                                   │
│   "Because if I do... Who's gonna fight for the others?"                    │
└──────────────────────────────────────────────────────────────────────────────┘
```

---

## ⚙️ `REVERSE ENGINEERING — CORE DISCIPLINE`

> I take compiled code and read it like source. Language doesn't matter. Runtime doesn't matter. If it runs on a machine, I can understand it.

<br>

**`› Decompiling Compiled Binaries — Any Language, Any Runtime`**

My primary skill. I decompile compiled executables and bytecode back to readable logic — regardless of what language they were originally written in. .NET assemblies, Java bytecode, native C/C++ binaries, Electron apps, compiled Python — each has a path back to readable code, and I know all of them.

```
Language / Runtime → Decompilation Path:

  .NET (C#, VB)      →  dnSpy / ILSpy / dotPeek     → full C# source recovery
  Java / Kotlin      →  jadx / Procyon / CFR          → Java class reconstruction
  Python compiled    →  pycdc / uncompyle6 / decompile → .pyc → readable .py
  Native (C / C++)   →  Ghidra / x64dbg / Binary Ninja → pseudocode + ASM
  Electron / Node    →  asar extract → JS deobfuscation → full app logic
  Lua bytecode       →  unluac / luadec               → readable Lua source
  Any obfuscated JS  →  de4js / AST rewrite / manual  → reconstructed logic
```

<br>

**`› Extracting Hardcoded Values from Compiled Code`**

Developers compile secrets into their software thinking they're safe — API keys, tokens, internal URLs, method names, payload structures. I extract them. Static strings, encrypted constants, XOR-obfuscated values — it all surfaces under analysis.

```python
# Automated hardcoded value extractor from compiled binary
import re, sys

with open(sys.argv[1], "rb") as f:
    data = f.read()

# Extract printable strings (min length 6)
strings = re.findall(rb'[\x20-\x7e]{6,}', data)

# Filter for high-value targets
targets = {
    "urls":    [s for s in strings if b'http' in s or b'api.' in s],
    "keys":    [s for s in strings if b'key' in s.lower() or b'token' in s.lower() or b'secret' in s.lower()],
    "paths":   [s for s in strings if s.startswith(b'/') and len(s) > 4],
    "methods": [s for s in strings if b'.' in s and s.isascii()],
}

for category, findings in targets.items():
    if findings:
        print(f"\n[+] {category.upper()}:")
        for f in findings:
            print(f"    {f.decode(errors='replace')}")
```

<br>

**`› Tracing Internal Call Chains`**

I don't just find what a binary does — I trace *how* it does it. I follow the execution path from user action to network request: which function calls which, what gets passed, how payloads are built, where tokens are attached, and what the final outgoing communication looks like.

```
Call Chain Tracing Methodology:
  [1] Identify entry point — user action, timer, event handler
  [2] Follow call graph in Ghidra / dnSpy / jadx
  [3] Locate the HTTP client or socket call (the exit point)
  [4] Trace backwards — what built the request body?
  [5] What built the headers? What signed the payload?
  [6] What parameters came from hardcoded values vs. runtime state?
  [7] Reconstruct: full request format, auth logic, payload schema
  [8] Reproduce the exact call externally from a Python/Node script
```

<br>

**`› Payload & API Structure Recovery`**

After tracing the call chain, I reconstruct the full payload format — field names, types, required vs. optional parameters, encoding, signing — and document it as a clean API spec that never existed before.

```python
# Reconstructed API call from binary analysis — built from decompiled payload logic
import requests, hashlib, hmac, time, json

# All of this was recovered from the compiled binary:
BASE_URL   = "https://internal.target.com"          # hardcoded in binary
API_KEY    = "recovered_from_binary_constants"       # extracted from .rodata
SECRET     = "reconstructed_from_decompiled_logic"   # recovered from crypto routine

def sign_payload(body: dict) -> str:
    raw = json.dumps(body, separators=(',', ':'))
    return hmac.new(SECRET.encode(), raw.encode(), hashlib.sha256).hexdigest()

def call_internal_method(method: str, params: dict):
    body = {
        "jsonrpc": "2.0",
        "method":  method,       # method names recovered from string table
        "params":  params,
        "id":      1,
        "ts":      int(time.time()),
    }
    headers = {
        "X-Api-Key":   API_KEY,
        "X-Signature": sign_payload(body),
        "Content-Type": "application/json",
    }
    return requests.post(f"{BASE_URL}/rpc", json=body, headers=headers).json()

# Call undocumented internal methods discovered through RE
result = call_internal_method("user.getPrivateData", {"uid": 1337})
print(json.dumps(result, indent=2))
```

---

## 🌐 `API METHOD DISCOVERY`

> Every application has a public API and a real API. I find the real one.

I specialize in discovering undocumented API methods, hidden endpoints, and internal communication interfaces that developers never published. My approach combines static binary analysis, live traffic interception, and JS source reconstruction to build a complete map of what an application can actually do.

```
Discovery Vectors:
  ├── Binary String Extraction
  │     Scan compiled executables for embedded URL paths, method names,
  │     parameter keys, and internal route strings
  │
  ├── Decompiled Source Mining
  │     Recover HTTP client call sites from decompiled .NET / Java / JS
  │     Extract: URL construction logic, header assembly, body serialization
  │
  ├── Live Traffic Interception
  │     Proxy all application traffic through Burp Suite
  │     Capture undocumented calls made during normal usage
  │     Identify hidden parameters sent silently by the client
  │
  ├── Call Chain Reconstruction
  │     Trace from UI event → internal function → HTTP client → wire
  │     Understand exactly how each API method is invoked and why
  │
  └── Auth & Signing Reconstruction
        Recover token generation, HMAC signing, and session logic
        from decompiled crypto routines and header assembly code
```

---

## 🕵️ `OSINT`

Deep passive intelligence gathering. I map targets thoroughly before any active analysis begins — infrastructure, identity, history, and exposure.

```
OSINT Stack:
  ├── Subdomain & DNS         amass · subfinder · dnsx · crt.sh
  ├── Infrastructure          shodan · censys · fofa · bgp.he.net
  ├── Historical Records      Wayback Machine · URLScan · CommonCrawl
  ├── Identity & Accounts     maigret · holehe · sherlock
  └── Leak Intelligence       breach correlation, credential mapping
```

---

## 💻 `SIDE CODER`

I build the tools I need. When existing tooling doesn't fit the job, I write it — clean, purpose-built, and fast.

<div align="center">

![Python](https://img.shields.io/badge/Python-0a0a0f?style=for-the-badge&logo=python&logoColor=00A8FF)
![Node.js](https://img.shields.io/badge/Node.js-0a0a0f?style=for-the-badge&logo=nodedotjs&logoColor=00A8FF)
![JavaScript](https://img.shields.io/badge/JavaScript-0a0a0f?style=for-the-badge&logo=javascript&logoColor=00A8FF)
![Bash](https://img.shields.io/badge/Bash-0a0a0f?style=for-the-badge&logo=gnubash&logoColor=00A8FF)

</div>

**What I build:** binary analysis scripts, API call reconstructors, payload forgers, OSINT automation pipelines, deobfuscation helpers, traffic parsers, and custom HTTP clients that speak protocols I reverse engineered.

---

## 🛠️ `TOOLCHAIN`

<div align="center">

| Category | Tools |
|:---|:---|
| **.NET RE** | dnSpy · ILSpy · dotPeek · de4dot |
| **Java / JVM RE** | jadx · Procyon · CFR · JD-GUI |
| **Native Binary** | Ghidra · x64dbg · Binary Ninja · Detect-It-Easy |
| **Python Bytecode** | pycdc · uncompyle6 |
| **JS Deobfuscation** | de4js · AST Explorer · Prettier · Chrome DevTools |
| **Traffic Analysis** | Burp Suite · Wireshark · mitmproxy · Fiddler |
| **OSINT** | amass · shodan · subfinder · maigret · holehe |
| **Scripting** | Python 3 · Node.js · Bash |
| **Platforms** | Kali Linux · Windows |

</div>

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

## 🔭 `CURRENTLY`

```python
current = {
    "working_on": [
        "Tracing call chains in compiled desktop software",
        "Recovering undocumented API methods from binaries",
        "Building automated payload reconstructors in Python",
        "OSINT pipeline for passive infrastructure mapping",
    ],
    "sharpening": [
        "Deeper native binary analysis — x86/x64 assembly fluency",
        "Deobfuscation techniques for advanced packing / protection schemes",
        "Writing cleaner, faster automation tooling",
    ],
    "playing":   "Roblox",
}
```

---

## 📡 `REACH ME`

<div align="center">

[![Website](https://img.shields.io/badge/y4seen.lol-0a0a0f?style=for-the-badge&logo=firefoxbrowser&logoColor=00A8FF)](https://y4seen.lol)
&nbsp;
[![Discord](https://img.shields.io/badge/y4seen.lol-0a0a0f?style=for-the-badge&logo=discord&logoColor=00A8FF)](https://discord.com/users/y4seen)
&nbsp;
[![Email](https://img.shields.io/badge/y4seen@y4seen.lol-0a0a0f?style=for-the-badge&logo=protonmail&logoColor=00A8FF)](mailto:y4seen@y4seen.lol)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:003366,50:001a33,100:0a0a0f&height=100&section=footer" width="100%"/>

```
┌──(y4㉿kali)-[~]
└─$ echo "SYSTEM SECURE. SESSION ACTIVE. ANALYSIS ONGOING."

SYSTEM SECURE. SESSION ACTIVE. ANALYSIS ONGOING.
```

*Every compiled binary tells a story. I just speak the language.*

**y4seen · y4seen.lol · Reverse Engineer · OSINT · Developer · KSA / India**

</div>
