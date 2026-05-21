+++
title = 'Guida Operativa G&G Cyber-Lab'
date = 2026-05-21
draft = false
+++

<style>
    .cyber-body {
        background-color: #000;
        color: #00FF00;
        font-family: 'Courier New', Courier, monospace;
        padding: 25px;
        border: 2px solid #00FF00;
        border-radius: 10px;
        box-shadow: 0 0 20px #00FF00;
        line-height: 1.6;
        max-width: 900px;
        margin: 20px auto;
    }
    .cyber-header {
        text-align: center;
        border: 3px double #00FF00;
        padding: 20px;
        margin-bottom: 30px;
        background-color: #1a1a1a;
    }
    h1 { font-size: 2.2em; text-transform: uppercase; margin: 0; letter-spacing: 3px; }
    h2 { 
        background-color: #00FF00; 
        color: #000000; 
        padding: 5px 15px; 
        margin-top: 30px; 
        text-transform: uppercase; 
        font-size: 1.4em;
        display: inline-block;
    }
    .code-block {
        background-color: #000000;
        border: 1px dashed #00FF00;
        padding: 15px;
        margin: 15px 0;
        white-space: pre-wrap;
        font-size: 10pt;
        color: #00FF00;
    }
    .step-content { 
        margin-bottom: 25px; 
        padding: 10px;
        border-left: 2px solid #00FF00;
    }
    .highlight { color: #ffffff; font-weight: bold; }
    .footer {
        text-align: center;
        margin-top: 40px;
        font-size: 9pt;
        border-top: 1px solid #00FF00;
        padding-top: 15px;
    }
</style>

<div class="cyber-body">
    <div class="cyber-header">
        <h1>G&G CYBER-LAB</h1>
        <p>MANUALE INTEGRALE DI INSTALLAZIONE E CONFIGURAZIONE [cite: 68, 69]</p>
    </div>

    <div class="step-content">
        <h2>1. PREPARAZIONE AMBIENTE [cite: 70]</h2>
        <p>Eseguire nel Terminale (Amministratore) per installare i componenti core[cite: 71]:</p>
        <div class="code-block">
# Installazione Git, Hugo Extended e VS Code [cite: 72]
winget install Git.Git [cite: 73]
winget install Hugo.Hugo.Extended [cite: 74]
winget install Microsoft.VisualStudioCode [cite: 75]
        </div>
    </div>

    <div class="step-content">
        <h2>2. CREAZIONE SITO E TEMA [cite: 76]</h2>
        <p>Inizializzazione del progetto e collegamento del tema professionale[cite: 77]:</p>
        <div class="code-block">
hugo new site miosito-hugo [cite: 78]
cd miosito-hugo [cite: 79]
git init [cite: 80]
git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder [cite: 81]
        </div>
    </div>

    <div class="step-content">
        <h2>3. CONFIGURAZIONE "CYBERSECURITY" (HUGO.TOML) [cite: 82]</h2>
        <p>Sostituisci il contenuto di <span class="highlight">hugo.toml</span> con questo codice per attivare lo stile Terminale[cite: 83]:</p>
        <div class="code-block">
baseURL = 'https://gennaropecorone-ai.github.io/miosito-hugo/' [cite: 84]
languageCode = 'it-it' [cite: 85]
title = 'G&G CYBER-LAB' [cite: 86]
theme = 'hugo-coder' [cite: 87]
publishDir = 'docs' [cite: 88]

[cite_start][params] [cite: 89]
[cite_start]author = "G&G" [cite: 90]
[cite_start]description = "SISTEMA OPERATIVO G&G - ACCESSO AUTORIZZATO" [cite: 91, 92]
[cite_start]info = "Analisi Dati | Cybersecurity | AI Research" [cite: 93]
[cite_start]avatarurl = "images/GG.jpg" [cite: 94]
[cite_start]colorScheme = "dark" [cite: 95]
[cite_start]avatarSize = "350px" [cite: 96]
[cite_start]layout = "circle" [cite: 97]
[cite_start]stickyHeader = true [cite: 98]

[cite_start][params.colors] [cite: 99]
[cite_start]primary = "#00FF00" [cite: 100]
[cite_start]background = "#000000" [cite: 100]
[cite_start]text = "#00FF00" [cite: 100]
        </div>
    </div>

    <div class="step-content">
        <h2>4. [cite_start]PROCEDURA DI PUBBLICAZIONE (IL RITUALE) [cite: 101]</h2>
        <p>Da eseguire nel terminale di VS Code ogni volta che fai una modifica[cite: 102]:</p>
        <div class="code-block">
# 1. Pulizia cartella di distribuzione [cite: 103]
if (Test-Path docs) { Remove-Item -Recurse -Force docs } [cite: 104]

# [cite_start]2. Compilazione del sito [cite: 105]
[cite_start]hugo [cite: 106]

# [cite_start]3. Invio a GitHub [cite: 107]
[cite_start]git add . [cite: 108]
[cite_start]git commit -m "Aggiornamento Cyber-Lab" [cite: 109]
[cite_start]git push origin main [cite: 110]
        </div>
    </div>

    <div class="step-content">
        <h2>5. MESSA ONLINE SU GITHUB PAGES [cite: 111]</h2>
        <p>Configurazione finale nel browser[cite: 112]:</p>
        <ul>
            <li>Vai su GitHub -> <span class="highlight">Settings</span> -> <span class="highlight">Pages</span>[cite: 113].</li>
            <li>Branch: <span class="highlight">main</span>[cite: 113].</li>
            <li>Cartella (Folder): Seleziona <span class="highlight">/docs</span>[cite: 114].</li>
            <li>Salva e attendi 60 secondi[cite: 115].</li>
        </ul>
    </div>+++
title = 'Guida Operativa'
date = 2026-05-21
draft = false
+++

<style>
    .cyber-body {
        background-color: #000;
        color: #00FF00;
        font-family: 'Courier New', Courier, monospace;
        padding: 25px;
        border: 2px solid #00FF00;
        border-radius: 10px;
        box-shadow: 0 0 20px #00FF00;
        line-height: 1.6;
    }
    .cyber-header {
        text-align: center;
        border: 3px double #00FF00;
        padding: 20px;
        margin-bottom: 30px;
        background-color: #1a1a1a;
    }
    .step-content h2 { 
        background-color: #00FF00; 
        color: #000; 
        padding: 5px 15px; 
        text-transform: uppercase; 
        display: inline-block;
    }
    .code-block {
        background-color: #000;
        border: 1px dashed #00FF00;
        padding: 15px;
        margin: 15px 0;
        font-size: 0.9em;
    }
    .highlight { color: #fff; font-weight: bold; }
</style>

<div class="cyber-body">
    <div class="cyber-header">
        <h1>G&G CYBER-LAB</h1>
        <p>MANUALE INTEGRALE DI INSTALLAZIONE E CONFIGURAZIONE</p>
    </div>

    <div class="step-content">
        <h2>1. PREPARAZIONE AMBIENTE</h2>
        <p>Eseguire nel Terminale (Amministratore) per installare i componenti core:</p>
        <div class="code-block">
            winget install Git.Git<br>
            winget install Hugo.Hugo.Extended<br>
            winget install Microsoft.VisualStudioCode
        </div>
    </div>

    <div class="step-content">
        <h2>2. CREAZIONE SITO E TEMA</h2>
        <p>Inizializzazione del progetto e collegamento del tema professionale:</p>
        <div class="code-block">
            hugo new site miosito-hugo<br>
            cd miosito-hugo<br>
            git init<br>
            git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder
        </div>
    </div>

    <div class="step-content">
        <h2>3. CONFIGURAZIONE "CYBERSECURITY" (HUGO.TOML)</h2>
        <p>Sostituisci il contenuto di <span class="highlight">hugo.toml</span> per attivare lo stile Terminale.</p>
    </div>

    <div class="step-content">
        <h2>4. PROCEDURA DI PUBBLICAZIONE (IL RITUALE)</h2>
        <p>Da eseguire nel terminale di VS Code ogni volta che fai una modifica:</p>
        <div class="code-block">
            # 1. Pulizia cartella docs<br>
            if (Test-Path docs) { Remove-Item -Recurse -Force docs }<br><br>
            # 2. Compilazione e Invio<br>
            hugo<br>
            git add .<br>
            git commit -m "Aggiornamento Cyber-Lab"<br>
            git push origin main
        </div>
    </div>

    <div class="step-content">
        <h2>5. MESSA ONLINE SU GITHUB PAGES</h2>
        <ul>
            <li>Vai su GitHub -> <span class="highlight">Settings</span> -> <span class="highlight">Pages</span></li>
            <li>Branch: <span class="highlight">main</span> | Cartella: <span class="highlight">/docs</span></li>
        </ul>
    </div>

    <div style="text-align: center; border-top: 1px solid #0f0; margin-top: 20px; padding-top: 10px;">
        DOCUMENTO INTEGRALE GENERATO PER GENNARO PECORONE - G&G LAB - 2026
    </div>
</div>

    <div class="footer">
        DOCUMENTO INTEGRALE GENERATO PER GENNARO PECORONE - G&G LAB - 2026 [cite: 116, 117]
    </div>
</div>