📄 README — Gestione del fork di anotherjulien/MyHOME
📌 Scopo
Questo repository è il fork personale del progetto MyHOME di anotherjulien.
Serve per:

mantenere una copia aggiornata del progetto originale

applicare modifiche personali nel branch dedicato

integrare i file necessari nel progetto Home Assistant principale

📁 Struttura locale
Codice
Projects/
    forks/
        anotherjulien/
            myhome/   ← questo repository
🔗 Remotes configurati
origin → il mio fork su GitHub
https://github.com/giannicoderani/MyHOME

upstream → repository originale
https://github.com/anotherjulien/MyHOME

Verifica:

Codice
git remote -v
🌱 Branch principali
main → copia pulita del progetto originale

giangiacomo → modifiche personali

Non lavorare mai su main.

🚀 Come aggiornare il fork dal progetto originale
Quando anotherjulien rilascia nuove versioni:

1. Vai nella repo
Codice
cd C:\Users\giann\Development\Projects\forks\anotherjulien\myhome
2. Aggiorna main dal repository originale
Codice
git checkout main
git fetch upstream
git merge upstream/main
git push
3. Porta le novità nel branch personale
Codice
git checkout giangiacomo
git merge main
git push
Se ci sono conflitti, risolverli e poi:

Codice
git add .
git commit
git push
🛠️ Come lavorare sulle modifiche personali
Assicurati di essere sul branch personale:

Codice
git checkout giangiacomo
Modifica i file necessari

Committa:

Codice
git add .
git commit -m "Descrizione modifica"
git push
🔄 Come integrare questo fork nel progetto Home Assistant
Il progetto Home Assistant principale si trova in:

Codice
Projects/homeassistant/
Per integrare le modifiche:

Copia i file necessari da questo fork (es. custom_components/...)

Incollali nel repo principale

Committa su homeassistant/dev

Quando stabile:

Codice
dev → main → push → deploy automatico (Git Pull)
🧹 Note operative
Non modificare mai main

Aggiornare periodicamente da upstream

Tenere tutte le personalizzazioni in giangiacomo

Copiare solo i file necessari nel progetto Home Assistant principale

✔️ Fine README