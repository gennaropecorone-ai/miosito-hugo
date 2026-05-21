+++
title = 'Guida Operativa G&G Cyber-Lab'
date = 2026-05-21
draft = false
+++

<style>
    .cyber-container {
        background-color: #000;
        color: #0f0;
        font-family: 'Courier New', monospace;
        padding: 30px;
        border: 2px solid #0f0;
        border-radius: 8px;
        box-shadow: 0 0 20px #0f0;
        max-width: 900px;
        margin: 20px auto;
    }
    .cyber-header {
        text-align: center;
        border-bottom: 2px double #0f0;
        margin-bottom: 40px;
        padding-bottom: 20px;
    }
    h1 { font-size: 2.2em; text-transform: uppercase; margin: 0; }
    h2 { 
        color: #000 !important; 
        background-color: #0f0; 
        padding: 8px 15px; 
        display: inline-block; 
        text-transform: uppercase; 
        font-size: 1.2em;
        margin-top: 30px;
    }
    .cyber-section {
        border-left: 3px solid #0f0;
        padding-left: 20px;
        margin: 30px 0;
    }
    .cyber-code {
        background-color: #0a0a0a;
        border: 1px dashed #0f0;
        padding: 15px;
        color: #0f0;
        overflow-x: auto;
        font-size: 0.9em;
        line-height: 1.5;
        margin: 15px 0;
    }
    .highlight { color: #fff; font-weight: bold; }
    ul { list-style-type: square; }
</style>

<div class="cyber-container">
    <div class="cyber-header">
        <h1>G&G CYBER-LAB</h1>
        <p>MANUALE INTEGRALE DI INSTALLAZIONE E CONFIGURAZIONE</p>
    </div>

    <div class="cyber-section">
        <h2>1. Preparazione Ambiente</h2>
        <p>Eseguire nel Terminale (Amministratore) per installare i componenti core[cite: 70, 71]:</p>
        <pre class="cyber-code">
# Installazione Git, Hugo Extended e VS Code
winget install Git.Git
winget install Hugo.Hugo.Extended
winget install Microsoft.VisualStudioCode [cite: 72, 73, 74, 75]</pre>
    </div>

    <div class="cyber-section">
        <h2>2. Creazione Sito e Tema</h2>
        <p>Inizializzazione del progetto e collegamento del tema professionale[cite: 76, 77]:</p>
        <pre class="cyber-code">
hugo new site miosito-hugo
cd miosito-hugo
git init
git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder [cite: 78, 79, 80, 81]</pre>
    </div>

    <div class="cyber-section">
        <h2>3. Configurazione "Cybersecurity" (hugo.toml)</h2>
        <p>Sostituisci il contenuto di <span class="highlight">hugo.toml</span> con questo codice per attivare lo stile Terminale[cite: 82, 83]:</p>
        <pre class="cyber-code">
baseURL = 'https://gennaropecorone-ai.github.io/miosito-hugo/'
theme = 'hugo-coder'
publishDir = 'docs'

[params]
    author = "G&G"
    description = "SISTEMA OPERATIVO G&G - ACCESSO AUTORIZZATO"
    info = "Analisi Dati | Cybersecurity | AI Research"
    avatarurl = "images/GG.jpg"
    colorScheme = "dark"
    avatarSize = "350px"
    layout = "circle"
    [params.colors]
        primary = "#00FF00"
        background = "#000000"
        text = "#00FF00" [cite: 84, 87, 88, 89, 90, 94, 95, 96, 97, 100]</pre>
    </div>

    <div class="cyber-section">
        <h2>4. Procedura di Pubblicazione (Il Rituale)</h2>
        <p>Eseguire nel terminale di VS Code per ogni modifica[cite: 101, 102]:</p>
        <pre class="cyber-code">
# 1. Pulizia cartella di distribuzione
if (Test-Path docs) { Remove-Item -Recurse -Force docs }

# 2. Compilazione del sito
hugo

# 3. Invio a GitHub
git add .
git commit -m "Aggiornamento Cyber-Lab"
[cite_start]git push origin main [cite: 104, 106, 108, 109, 110]</pre>
    </div>

    <div class="cyber-section">
        <h2>5. Messa Online su GitHub Pages</h2>
        [cite_start]<p>Configurazione finale nel browser[cite: 111, 112]:</p>
        <ul>
            <li>Vai su GitHub -> <span class="highlight">Settings</span> -> <span class="highlight">Pages</span>[cite: 113].</li>
            <li>Branch: <span class="highlight">main</span>[cite: 113].</li>
            <li>Cartella (Folder): Seleziona <span class="highlight">/docs</span>[cite: 114].</li>
            <li>Salva e attendi 60 secondi[cite: 115].</li>
        </ul>
    </div>

    <p style="text-align: center; margin-top: 50px; font-size: 0.8em; border-top: 1px solid #0f0; padding-top: 15px;">
        -- DOCUMENTO INTEGRALE GENERATO PER G&G LAB --
    </p>
</div>