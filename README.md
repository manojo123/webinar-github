# WEBINAR - GITHUB

## Procedimientos
1. Programador1 desarrolla utilizando su ambiente local, dentro de un nuevo branch de su proyecto. El nuevo branch debe tener el nombre dev-NOMBRE
2. Una vez listo, programador1 envia su codigo a github, desde el branch dev-NOMBRE.
3. Programador1 se encarga en conectar el servidor de pré produccion ```ssh USUARIO@url``` hace checkout en el branch correcto y realiza el pull de los archivos en el branch correcto. Caso multiplos programadores esten trabajando en el mismo proyecto, no va haber conflicto de codigos porque cada uno tiene su branch apenas tener cuidado en no manipular data en el branch de otra persona.
4. La persona encargada en solicitar el desarrollo en conjunto a un otro programador evalua los cambios y en caso no apruebe loop paso 1. En caso apruebe, break;
5. Una vez aprobado, Programador1 desde el servidor de pre-produccion hace el merge de dev para master
6. En caso haya conflictos de merge, una vez solucionados otro programador deberá evaluar que el codigo está funcionando.
7. En caso todo esté bien, se sube a produccion en el master branch por @Manuel Llaguno o @Jorge Moura

## INIT project in github
```
echo "# webinar-merge" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/{namespace}/{project}.git
git push -u origin main
```

## Create branch
```
git checkout -b dev-hello
```

## Create File
```
echo "Welcome to dev branch" >> hello.txt
```

## Push Branch and settings to git 
```
git add hello.txt
git commit -m "Add new file hello"
```

## Merge Branch to main
```
git checkout main
```

```
git merge dev-hello //Merges
git branch -d dev-hello //delete branch
git push origin :dev-hello //delete branch in github
```

```
git checkout -b dev-conflict
```
## modify hello.txt
push

## Links
https://github.com/manojo123/webinar-github
https://drive.google.com/file/d/1HiL6SnUc0ocmKsyvoHUCOm9X3uWdLV0o/view?usp=sharing

> Gracias Andrei
https://www.notion.so/Comandos-745d6849ffdb42ce871b6012f2d08384#c434262da17d4c6db255ad74f650c972
