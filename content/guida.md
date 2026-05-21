+++
title = 'Guida Operativa G&G Cyber-Lab'
date = 2026-05-21
draft = false
+++

<style>
    .cyber-body {
        background-color: #000;
        color: #0f0;
        font-family: 'Courier New', monospace;
        padding: 25px;
        border: 2px solid #0f0;
        border-radius: 10px;
        box-shadow: 0 0 20px #0f0;
        line-height: 1.6;
    }
    .cyber-header {
        text-align: center;
        border-bottom: 3px double #0f0;
        margin-bottom: 30px;
        padding-bottom: 15px;
    }
    .cyber-step {
        margin-bottom: 30px;
        border-left: 3px solid #0f0;
        padding-left: 20px;
    }
    h1 { font-size: 2em; text-transform: uppercase; letter-spacing: 2px; }
    h2 { 
        color: #000 !important; 
        background-color: #0f0; 
        padding: 5px 15px; 
        display: inline-block; 
        text-transform: uppercase;
        font-size: 1.3em;
    }
    .command-box {
        background-color: #0a0a0a;
        border: 1px dashed #0f0;
        padding: 15px;
        color: #0f0;
        margin: 15px 0;
        font-size: 0.95em;
    }
    .highlight { color: #fff; font-weight: bold; }
    ul { list-style-type: "> "; }
</style>

<div class="cyber-body">
    <div class="cyber-header">
        <h1>G&G CYBER-LAB</h1>
        <p>MANUALE INTEGRALE DI INSTALLAZIONE E CONFIGURAZIONE</p>
    </div>

    <div class="cyber-step">
        <h2>1. PREPARAZIONE AMBIENTE</h2>
        <p>Eseguire nel Terminale (Amministratore) per installare i componenti core del sistema:</p>
        <div class="command-box">
# Installazione Git, Hugo Extended e VS Code<br>
winget install Git.Git<br>
winget install Hugo.Hugo.Extended<br>
winget install Microsoft.VisualStudioCode
        </div>
    </div>

    <div class="cyber-step">
        <h2>2. CREAZIONE SITO E TEMA</h2>
        <p>Inizializzazione del progetto locale e collegamento del tema professionale Hugo Coder:</p>
        <div class="command-box">
hugo new site miosito-hugo<br>
cd miosito-hugo<br>
git init<br>
git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder
        </div>
    </div>

    <div class="cyber-step">
        <h2>3. CONFIGURAZIONE "CYBERSECURITY"</h2>
        <p>Sostituire il contenuto del file <span class="highlight">hugo.toml</span> con i parametri di stile G&G per attivare l'interfaccia terminale, il colore neon e l'avatar da 350px.</p>
    </div>

    <div class="cyber-step">
        <h2>4. PROCEDURA DI PUBBLICAZIONE (IL RITUALE)</h2>
        <p>Eseguire questa sequenza nel terminale di VS Code per ogni aggiornamento dei dati:</p>
        <div class="command-box">
# 1. Pulizia cartella di distribuzione<br>
if (Test-Path docs) { Remove-Item -Recurse -Force docs }<br><br>
# 2. Compilazione del sito<br>
hugo<br><br>
# 3. Invio a GitHub<br>
git add .<br>
git commit -m "Aggiornamento Cyber-Lab"<br>
git push origin main
        </div>
    </div>

    <div class="cyber-step">
        <h2>5. MESSA ONLINE SU GITHUB PAGES</h2>
        <p>Configurazione finale lato server tramite browser:</p>
        <ul>
            <li>Accedere a GitHub -> <span class="highlight">Settings</span> -> <span class="highlight">Pages</span>.</li>
            <li>Impostare il Branch su <span class="highlight">main</span>.</li>
            <li>Nella selezione cartella (Folder), scegliere <span class="highlight">/docs</span>.</li>
            <li>Cliccare su Salva e attendere la propagazione del segnale (60 secondi).</li>
        </ul>
    </div>

    <p style="text-align: center; margin-top: 40px; font-size: 0.8em;">
        DOCUMENTO INTEGRALE GENERATO PER GENNARO PECORONE - G&G LAB - 2026
    </p>
</div>