# Git-logg

Klistra in utskrifter och svara på frågorna. Det här är din dokumentation av dagens arbete.

## 1. Utgångsläget

Skriv ut `git log --oneline --graph --all` direkt efter att du klonat. Klistra in här:
5a5841d (HEAD -> main, origin/main, origin/HEAD) Modul 5 i TypeScript med Vite

- 3804533 Add files via upload
- f7a13a4 Add files via upload
- c9a0075 Initial commit
  PS C:\ec\lexicon\monika-m5-dag09-git-grenar> git branch -a
- main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
  PS C:\ec\lexicon\monika-m5-dag09-git-grenar> git status
  On branch main
  Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\ec\lexicon\monika-m5-dag09-git-grenar>

```
(klistra in)
```

## 2. Merge utan konflikt

Klistra in `git log --oneline --graph --all` efter merge:

:\ec\lexicon\monika-m5-dag09-git-grenar> git log --oneline --graph --all

- 3853e53 (HEAD -> main) Merge branch 'meny-nyheter'
  |\
  | \* df30c71 (meny-nyheter) Lägg till kanelbulle på menyn
- | 0d7fa90 Lägg till telefonnummer
- | a28bf73 (origin/main, origin/HEAD) Add comment where to start tomorrow in read me
- | 93a3b94 Create branch meny-nyheter
  |/
- eabfd99 Run git log --oneline --graph --all, git branch -a git status
- 5a5841d Modul 5 i TypeScript med Vite
- 3804533 Add files via upload
- f7a13a4 Add files via upload
- c9a0075 Initial commit

Fråga: Vad är skillnaden mellan en _fast-forward_-merge och en merge som skapar en egen merge-commit? Svara med egna ord:
fast_forward lägger sig ändringarna på rad, merge-commit så blir det en förgrening/puckel och samlas ihop på slutet

## 3. Konflikten

Klistra in filen med konfliktmarkörerna, precis som den såg ut innan du löste den:

```
(klistra in)
Vardagar: 07–18
<<<<<<< HEAD
Helger: 10–17
=======
Helger: 09–18
>>>>>>> oppettider-sommar
Röda dagar: stängt
```

Fråga: Vad betyder `<<<<<<< HEAD`, `=======` och `>>>>>>> grennamn`?
nuvarande ändring
inkommit en nyare ändring, nu finns två ändringar på samma gång
Hur löste du den, och varför blev det så?

Tog bort markörerna och valde Helger 10-18

## 4. Ångra

Vad är skillnaden mellan `git restore`, `git revert` och `git reset`? Vilken är säkrast när ändringen redan är pushad?

git restore Återställer osparade ändringar i filer (working directory / staging).
git revert Skapar en ny commit som upphäver en specifik gammal commit.
git reset Flyttar bakåt i historiken och raderar/återställer tidigare commits.

skapa en ny commit

## 5. Pull request

Länk till din pull request (på ditt eget repo):

## 6. Reflektion

Vad är det värsta som kan hända om man kör `git push --force` på en gren som andra använder?

Man skriver över andras uppladdade kod med sin egen version
