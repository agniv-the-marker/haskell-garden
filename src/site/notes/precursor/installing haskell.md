---
{"dg-publish":true,"permalink":"/precursor/installing-haskell/"}
---


First you need to install [GHCu[fp_notes.pdf](https://drive.google.com/file/d/1O1Oq5g9DEug96MbidHu_iYOwaDCYYNa2/view?usp=sharing)(https://www.haskell.org/ghcup/#) by running:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force;[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; try { Invoke-Command -ScriptBlock ([ScriptBlock]::Create((Invoke-WebRequest https://www.haskell.org/ghcup/sh/bootstrap-haskell.ps1 -UseBasicParsing))) -ArgumentList $true } catch { Write-Error $_ }
```

The `haskell-language-server` seems mostly optional, especially if your IDE will install extension support as a plug-in (in my case vscode). For `stack`, it's an alternative to `cabal` but is sometimes needed. In my case I'll install it. Take the defaults for the rest unless you want to not have it on your desktop, and it should install.

Right after this, do

```powershell
cabal install hlint
```

This will let you do linting. All of this installation might take a while (and open up MinGW x64), so in the meantime look at [[ide suppor[fp_notes.pdf](https://drive.google.com/file/d/1O1Oq5g9DEug96MbidHu_iYOwaDCYYNa2/view?usp=sharing)].
