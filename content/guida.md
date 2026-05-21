+++
title = 'Guida Operativa'
date = 2026-05-21
draft = false
+++

{{< cyber >}}
<div class="cyber-header">
    <h1>G&G CYBER-LAB</h1>
    <p>MANUALE INTEGRALE DI INSTALLAZIONE E CONFIGURAZIONE</p>
</div>

<div class="step-content">
    <h2>1. PREPARAZIONE AMBIENTE</h2>
    <p>Eseguire nel Terminale (Amministratore):</p>
    <div class="code-block">
winget install Git.Git
winget install Hugo.Hugo.Extended
winget install Microsoft.VisualStudioCode</div>
</div>

<div class="step-content">
    <h2>2. CREAZIONE SITO</h2>
    <div class="code-block">
hugo new site miosito-hugo
cd miosito-hugo
git init</div>
</div>

<div class="step-content">
    <h2>3. IL RITUALE DI PUBBLICAZIONE</h2>
    <div class="code-block">
hugo
git add .
git commit -m "Update"
git push origin main</div>
</div>

<div style="text-align: center; border-top: 1px solid #0f0; margin-top: 20px; padding-top: 10px;">
    DOCUMENTO INTEGRALE GENERATO PER GENNARO PECORONE - G&G LAB - 2026
</div>
{{< /cyber >}}