


poniższe polecenia wpisywane są w konsole Zsh + Oh My Zsh/git bash
konsola jest na mac os lub linuksie

git --version sprawdza wersje gita
git bash here otwiera konsole gita z okna folderu
git init tworzy repozytorium
ls  	wyswietla foldery
ls -a 	wyswietla takze pliki i foldery ukryte
cd git-kurs 	przechodzi do folderu git-kurs

git status 	pokazuje status naszego gita

touch 1.txt 	tworzy plik 1.txt, plik znajduje sie w working area
code . 	otwiera visual studio code w  aktualnym katalog

Git ma trzy obszary pracy 
1.  working area
2. staging area
3. repozytorium
konfigurujemy dostęp do repozytorium
 git config --global user.name "GrzegorzBuczynski"
 git config --global user.email "grzegorzbuczynski93@gmail.com"

git add 1.txt 	dodaje plik 1.txt do śledzenia, plik przechodzi z working area do staging area
git commit -m"Dodajemy pierwszy plik 1.txt" 
m znaczy że załączamy massage

git log 	sprawdzamy historie commitów
wciskamy q by wyjść z okna histori comitów (w konsoli na macu przy wiekszej ilości wpisów na windows też)

git add -A	dodaje wszystkie nie śledzone pliki do śledzenia
git commit -m"Drugi commit - dodajemy trzy nowe pliki"

po zmodyfikowaniu pliku 1.txt musimy znowu dodać plik do stagingu
git add 1.txt	dodajemy 1.txt do zakomitowania
git commit -m"Trzeci commit -modyfikacja pliku 1.txt"

git commit -am"Czwarty commit dodajemy do stagingu i commitujemy"
modyfikator am znaczy add all, massage

git branch  wyswietla branche

git checkout -b"logowanie" tworzy nowy branch o nazwie logowanie/
git checkout master 	przełącza na branch master
git merge logowanie	łaczy branch logowanie do aktualnego brancha

git push wypychamy brancha do sieci/zewnętrznego repozytorium
git remote add <name> <url> dodaje/konfiguruje zdalne repozytorjum
git push -u origin master; do origina wysylamy brancha na branch master 
git pyta o nazwe użytkownika
git pyta o hasł, wklejamy token do githuba
, jeśli nie pyta startujemy agenta pytajacego o dane eval `ssh-agent -s`

mkdir kopia-repo	tworzy folder o nazwie kopia-repo
cd kopia-repo		przechodzi do kopia-repo
git clone <adres>	kopiuje innego brancha



https://www.toolsqa.com/git/branch-in-git/
Can I rename a branch after creation?

Yes, branches can be renamed by executing the command git -m <old_name> <new_name>. 
Although one should avoid this operation since the branch name can confuse the team members.
 



Quick setup — if you’ve done this kind of thing before
or	
https://github.com/GrzegorzBuczynski/buczynski.git
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

…or create a new repository on the command line
echo "# buczynski" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/GrzegorzBuczynski/buczynski.git
git push -u origin main
…or push an existing repository from the command line
git remote add origin https://github.com/GrzegorzBuczynski/buczynski.git
git branch -M main
git push -u origin main
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

