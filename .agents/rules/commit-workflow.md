# Flujo previo a cada commit

No crees commits salvo que el desarrollador lo solicite explícitamente. Cuando solicite un commit, completa estos pasos en orden antes de cada commit:

1. **Confirmar el alcance:** verifica que la tarea y sus criterios de aceptación estén claros. Si no lo están, solicita aclaración antes de continuar.
2. **Revisar el estado inicial:** ejecuta `git status` e identifica cambios preexistentes. Consérvalos y no los incluyas sin autorización.
3. **Validar los cambios:** ejecuta las pruebas, comprobaciones de tipos o lint pertinentes a las rutas modificadas. Si no existe una comprobación aplicable, indícalo; si falla, informa antes de crear el commit.
4. **Revisar el diff:** inspecciona todos los cambios previstos y ejecuta `git diff --check`. Comprueba que no haya secretos, archivos generados ni cambios ajenos al alcance.
5. **Preparar el commit:** añade únicamente las rutas autorizadas, revisa `git diff --cached` y crea el commit solo si coincide con el alcance solicitado.

No uses `git add .` para preparar cambios. No enmiendes, reescribas ni publiques commits existentes salvo que el desarrollador lo pida expresamente.
