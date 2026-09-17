# Documentación de la rama feature

## 1. Creación de la rama

El trabajo se realizó a partir de la rama principal **master**.

Primero se verificó que el repositorio estuviera actualizado:

```bash
git status
```

El resultado indicó que la rama **master** estaba actualizada con respecto a **origin/master**.

Posteriormente, se creó y se cambió a la nueva rama mediante el siguiente comando:

```bash
git checkout -b feature
```

Con este comando se creó la rama **feature** de forma local y automáticamente se realizó el cambio hacia dicha rama.

Para verificar la rama actual se utilizó:

```bash
git branch
```

El resultado mostró:

```bash
MiRama
* feature
master
```

El símbolo **"*"** indica que actualmente se está trabajando en la rama feature.

## 2. Creación del archivo README.md

Estando ubicado en la rama **feature**, se creó el archivo **README.md**.

Este archivo tiene como finalidad documentar el proceso realizado durante el ejercicio de ramas y versionamiento con Git.

## 3. Publicación del archivo

Después de crear y documentar el archivo **README.md**, se agregó al área de preparación mediante:

```bash
git add README.md
```

Posteriormente, se realizó un commit para registrar los cambios:

```bash
git commit -m "docs: add feature branch documentation"
```

El commit permite registrar de manera local la creación y contenido del archivo **README.md**.

## 4. Sincronización con el repositorio remoto

Finalmente, se publicó la rama **feature** en el repositorio remoto de GitHub mediante:

```bash
git push -u origin feature
```

El parámetro **-u** establece la relación entre la rama local **feature** y la rama remota **origin/feature**.

A partir de este momento, los cambios posteriores realizados en esta rama podrán sincronizarse utilizando:

```bash
git push
```

## 5. Verificación

Para comprobar que la rama local y la rama remota existen, se puede utilizar:

```bash
git branch -a
```

El resultado esperado debe mostrar las ramas:

```bash
MiRama
master
* feature
remotes/origin/feature
remotes/origin/master
```

De esta manera se verifica que la rama **feature** fue creada localmente y publicada correctamente en GitHub.

## 6. Integración de las ramas

Después de crear y publicar las ramas **feature**, **bugfix** y **hotfix**, se procedió a trasladar sus cambios a la rama principal **master**.

Primero se realizó el cambio hacia la rama **master**:

```bash
git checkout master
```

Posteriormente, se integraron los cambios de cada rama mediante **git merge**.

### Integración de feature

```bash
git merge feature
```

Esta operación incorporó a **master** el archivo **README.md** creado en la rama **feature**.

### Integración de bugfix

```bash
git merge bugfix
```

Esta operación incorporó a **master** el archivo **DocumentacionSolucion.txt** creado en la rama **bugfix**.

### Integración de hotfix

```bash
git merge hotfix
```

Esta operación incorporó a **master** el archivo **DocumentacionSolucionhotfix.txt** creado en la rama **hotfix**.

Finalmente, los cambios de la rama **master** fueron sincronizados con el repositorio remoto mediante:

```bash
git push origin master
```

## 7. Verificación final

Se verificó que los cambios de las tres ramas estuvieran integrados correctamente en **master**.

La estructura final contiene los siguientes archivos:

- **README.md**
- **DocumentacionSolucion.txt**
- **DocumentacionSolucionhotfix.txt**

También se verificó el historial de commits y las ramas existentes mediante:

```bash
git log --oneline --graph --all
```

y:

```bash
git branch -a
```

De esta manera se comprobó el proceso de creación, publicación, integración y sincronización de las ramas utilizadas durante el ejercicio.