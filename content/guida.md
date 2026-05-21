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
        color: #000 !important; 
        padding: 5px 15px; 
        text-transform: uppercase; 
        display: inline-block;
        margin-top: 25px;
    }
    .code-block {
        background-color: #000;
        border: 1px dashed #00FF00;
        padding: 15px;
        margin: 15px 0;
        font-size: 0.95em;
        white-space: pre-wrap;
        color: #00FF00;
    }
    .highlight { color: #fff; font-weight: bold; }
    .footer-cyber {
        text-align: center;
        border-top: 1px solid #00FF00;
        margin-top: 40px;
        padding-top: 20px;
        font-size: 0.9em;
    }
    ul { list-style-type: "-> "; }
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
# Installazione Git, Hugo Extended e VS Code
winget install Git.Git
winget install Hugo.Hugo.Extended
winget install Microsoft.VisualStudioCode</div>
    </div>

    <div class="step-content">
        <h2>2. CREAZIONE SITO E TEMA</h2>
        <p>Inizializzazione del progetto e collegamento del tema professionale:</p>
        <div class="code-block">
hugo new site miosito-hugo
cd miosito-hugo
git init
git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder</div>
    </div>

    <div class="step-content">
        <h2>3. CONFIGURAZIONE "CYBERSECURITY" (HUGO.TOML)</h2>
        <p>Sostituisci il contenuto di <span class="highlight">hugo.toml</span> con questo codice per attivare lo stile Terminale:</p>
        <div class="code-block">
baseURL = 'https://gennaropecorone-ai.github.io/miosito-hugo/'
languageCode = 'it-it'
title = 'G&G CYBER-LAB'
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
stickyHeader = true

[params.colors]
primary = "#00FF00"
background = "#000000"
text = "#00FF00"</div>
    </div>

    <div class="step-content">
        <h2>4. PROCEDURA DI PUBBLICAZIONE (IL RITUALE)</h2>
        <p>Da eseguire nel terminale di VS Code ogni volta che fai una modifica:</p>
        <div class="code-block">
# 1. Pulizia cartella di distribuzione
if (Test-Path docs) { Remove-Item -Recurse -Force docs }

# 2. Compilazione del sito
hugo

# 3. Invio a GitHub
git add .
git commit -m "Aggiornamento Cyber-Lab"
git push origin main</div>
    </div>

    <div class="step-content">
        <h2>5. MESSA ONLINE SU GITHUB PAGES</h2>
        <p>Configurazione finale nel browser:</p>
        <ul>
            <li>Vai su GitHub -> <span class="highlight">Settings</span> (Impostazioni).</li>
            <li>Seleziona <span class="highlight">Pages</span> nel menu a sinistra.</li>
            <li>Branch: <span class="highlight">main</span>.</li>
            <li>Cartella (Folder): Seleziona <span class="highlight">/docs</span>.</li>
            <li>Salva e attendi 60 secondi che il segnale si propaghi.</li>
        </ul>
    </div>

    <div class="footer-cyber">
        DOCUMENTO INTEGRALE GENERATO PER GENNARO PECORONE - G&G LAB - 2026
    </div>
</div>