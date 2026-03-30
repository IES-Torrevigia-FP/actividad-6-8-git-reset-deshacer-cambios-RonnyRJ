git reset --soft mueve el commit, pero mantiene todo en staging y en el working directory.
git reset (mixed) mueve el commit, quita del staging, pero deja los cambios en el working directory.
git reset --hard mueve el commit y borra todo (staging + working directory).

¿Por qué reset vs revert?

git reset reescribe el historial puede romper ramas compartidas.
git revert crea un commit nuevo que deshace cambios → no rompe el historial, por eso es más seguro en equipo.

Situaciones reales:

--soft quieres rehacer el último commit (cambiar mensaje o añadir algo).
mixed hiciste add demasiado pronto y quieres reorganizar los archivos antes de commitear.
--hard quieres volver a un estado limpio descartando todo (por ejemplo, pruebas fallidas en local).
