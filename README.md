# Tagdh O'Hare
## Repte: el nostre README de práctica
## Como subir un cambio a github
* Guardar el documento en local (ctrl + s)
* añadir el cambio al repositorio (add .)
* realizar el commit (commit -m "")
* hacer el push (push -u origin)
* comprobar cambios en GitHub web 
- [ ] Guardado en local
- [ ] Añadir cambio
- [ ] Realizar commit
- [ ] Realizar push
- [ ] Comprovar

El meu repositori:
[https://github.com/Taikohno/OperacioNordTec.git](https://) 

Comandas Utilizadas:
```
git --version
git init
git status
git add .
git commit -m ""
git branch
git remote add origin
git remote -v
git push -u origin
```
| Git Version | Git Init | Git push -u origin | Git branch    | Git commit -m "" |
| ----------- | -------- | ------------------ | --- | ---------------- |
| Shows git version       | Initializes Git    | sends the changes to the commit in the github repo               | shows your directory    | loads the changes for the following push                 |

Errores:
Los canvios no se ven en el repo de github despues de un commit

Solucion:
Asegurese de guardar el fitchero en local antes de nada, despues `git add .` para que se guarde en git, a continuación `git commit -m""` entre las comillas tienes que poner una descripción pequeña, y finalmente `git push -u origin` y recarga la pagina de github. 

:3