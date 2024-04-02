# Jak zjistit, kolik máš volného místa na disku?

## V powershellu (Windows 7/8/10/11)
*Tento postup vyžaduje, aby na počítači běžel operační systém Windows 7 a novější. Předpokládá se, že operační systém používá českou lokalizaci.*

1) Zmáčkni klávesovou zkratku <code>Win</code>+<code>R</code>

    *Klávesa <code>Win</code> se klávesa zpravidla umístěná mezi klávesou <code>alt</code> a <code>ctrl</code> s logem operačního Windows*

2) Otevře se okno s názvem **Spustit**
3) Do okna s názvem Spustit zadejte "powershell"
4) Zmáčkněte klávesu ENTER 
5) Zadejte příkaz <code>Get-Volume</code>
6) Do okna powershellu se vypíše tabuľka s kolonkami "DriveLetter", "FriendlyName", "FileSystemType", "DriveType", "HealthStatus", "OperationalStatus", "SizeRemaining", "Size".
Pod "SizeRemaining" je vypísané koľko zostáva miesta na disku.


## Windows 10
*Tento postup vyžaduje, aby na počítači běžel operační systém Windows 7 a novější. Předpokládá se, že operační systém používá českou lokalizaci.*

**V případě, že jste přihlášen na účtě, který má administrátorská práva**:

1) Zmáčkni klávesovou zkratku <code>Win</code>+<code>R</code>

    *Klávesa <code>Win</code> se klávesa zpravidla umístěná mezi klávesou <code>alt</code> a <code>ctrl</code> s logem operačního Windows*

2) Otevře se okno s názvem **Spustit**
3) Do textového pole s názvem "Otevřít" zadejte <code>diskmgmt.msc</code>
4) Mělo by se otevřít okno s názvem *Správa disků*

**V případě, že jste na účtě bez administrátorských práv, postupujte takto**:

1) Zmáčkni klávesovou zkratku <code>Win</code>+<code>R</code>

    *Klávesa <code>Win</code> se klávesa zpravidla umístěná mezi klávesou <code>alt</code> a <code>ctrl</code> s logem operačního Windows*

2) Otevře se okno s názvem **Spustit**
3) Do textového pole s názvem "Otevřít" zadejte <code>%SystemRoot%\explorer.exe /e,::{20D04FE0-3AEA-1069-A2D8-08002B30309D}</code>
4) Mělo by se otevřít okno s názvem *Tento počítač*
5) V okně vidíte jednotlivé připojené disky a jejich kapacity

## Ubuntu 22.04 Matte
1. Uživatel je přihlášen do počítače
2. Otevření menu - Kliknutí na ikonu s nápisem "Menu" v levém horním rohu monitoru
3. Kliknutí na "Type to search…"
4. Vyhledání "MATE Disk Usage Analyzer"
5. Otevření programu "MATE Disk Usage Analyzer" (kliněte na výsledek vyhledávání, který se objeví v pravém sloupci Menu)
6. V otevřeném okně najděte slovo "available"
nachází se v závorce vedle Total filesystem capacity v horním boxu okna (nikoli v hlavním grafickém boxu)
