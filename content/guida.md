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
        padding: 20px;
        border: 2px solid #0f0;
        border-radius: 5px;
        box-shadow: 0 0 15px #0f0;
    }
    .cyber-header {
        text-align: center;
        border-bottom: 2px double #0f0;
        margin-bottom: 30px;
        padding-bottom: 10px;
    }
    .cyber-section {
        border-left: 3px solid #0f0;
        padding-left: 15px;
        margin: 25px 0;
    }
    .cyber-code {
        background-color: #0a0a0a;
        border: 1px dashed #0f0;
        padding: 15px;
        color: #0f0;
        overflow-x: auto;
    }
    h2 { color: #000 !important; background-color: #0f0; padding: 5px 10px; display: inline-block; text-transform: uppercase; }
    strong { color: #fff; }
</style>

<div class="cyber-container">
    <div class="cyber-header">
        <h1>SISTEMA OPERATIVO G&G</h1>
        <p>RELAZIONE TECNICA DI CONFIGURAZIONE</p>
    </div>

    <div class="cyber-section">
        <h2>1. Installazione Core</h2>
        <p>Eseguire nel terminale Amministratore per preparare l'ambiente:</p>
        <pre class="cyber-code">
winget install Git.Git
winget install Hugo.Hugo.Extended
winget install Microsoft.VisualStudioCode</pre>
    </div>

    <div class="cyber-section">
        <h2>2. Configurazione hugo.toml</h2>
        <p>Parametri per il look <strong>Cyber-Hacker</strong>:</p>
        <pre class="cyber-code">
colorScheme = "dark"
avatarSize = "350px"
[params.colors]
    primary = "#00FF00"
    background = "#000000"
    text = "#00FF00"</pre>
    </div>

    <div class="cyber-section">
        <h2>3. Il Rituale di Pubblicazione</h2>
        <p>Sequenza obbligatoria per il caricamento online:</p>
        <pre class="cyber-code">
hugo
git add .
git commit -m "Cyber-Update"
git push origin main</pre>
    </div>

    <div class="cyber-section">
        <h2>4. GitHub Pages Settings</h2>
        <ul>
            <li>Branch: <strong>main</strong></li>
            <li>Folder: <strong>/docs</strong></li>
        </ul>
    </div>

    <p style="text-align:center; font-size: 0.8em; margin-top: 30px;">-- FINE TRASMISSIONE --</p>
</div>