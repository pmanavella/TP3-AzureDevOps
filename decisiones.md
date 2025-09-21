# TP3 – Introducción a Azure DevOps

## 1. Creación del proyecto
Se creó el proyecto **TP3-manavella** en Azure DevOps.  
Para el *Work item process* se eligió **Agile**, ya que permite trabajar con **Features, User Stories, Tasks y Bugs**, lo cual se ajusta mejor a los objetivos del TP.  

**Justificación:**  
- Más completo que Basic y más flexible que Scrum para un trabajo individual.  
- Permite trazabilidad desde funcionalidades grandes (Features) hasta tareas concretas (Tasks).  
- Es ampliamente utilizado en proyectos académicos y profesionales, lo que facilita la defensa oral.  

---

## 2. Configuración del Sprint y Work Items
- Se configuró un **Sprint inicial de 2 semanas** (19/09/2025 – 03/10/2025).  
- Dentro de este Sprint se organizaron:  
  - **Feature principal:** Gestión de Usuarios.  
  - **User Stories:**  
    1. Registrar usuario  
    2. Login de usuario  
    3. Editar perfil  
  - **Tasks:** (2 por cada User Story)  
    - Diseñar UI correspondiente.  
    - Implementar la API o lógica de backend.  
  - **Bugs de ejemplo:**  
    - Error al validar emails con caracteres especiales.  
    - Login falla con contraseñas que incluyen caracteres especiales.  

**Justificación:**  
Esta estructura permite descomponer funcionalidades grandes en entregables pequeños y medibles. Además, asegura que el Sprint tenga un objetivo claro y que se puedan detectar errores tempranamente.  

---

## 3. Control de versiones con Azure Repos – Intentos de importación
La idea inicial fue **importar un repositorio externo de GitHub** (`Cervellini2501/FINALarqsot_I`) hacia Azure Repos para centralizar el trabajo.  

- Se intentó el método de *Import repository* desde la interfaz de Azure, pero no estaba disponible al tener el repo inicializado.  
- Se probó clonar localmente y configurar remoto a Azure.  
- Surgieron problemas técnicos:  
  - Bloqueo de SSH (puerto 22).  
  - Error 404 con la URL HTTPS de Azure.  

**Decisión:**  
Se documentó el proceso y se decidió avanzar con un **repositorio vacío en Azure** como alternativa.  

---

## 4. Control de versiones con Azure Repos – Solución aplicada
- Se creó un repositorio vacío: **TP3-repo-vacio**.  
- Se configuró un **token personal (PAT)** para autenticar con Azure DevOps.  
- Se utilizó un sitio web generado con ayuda de IA como código base (HTML y CSS).  
- Se subieron los archivos iniciales en una rama `feature/initial-import`.  
- Se configuraron políticas en `main`: Pull Request obligatorio con al menos un reviewer.  
- Se creó un Pull Request desde `feature/initial-import` hacia `main`, se aprobó y se completó el merge.  

---

## 5. Documentación en GitHub
Se creó el repositorio [TP3-AzureDevOps](https://github.com/pmanavella/TP3-AzureDevOps)  
Allí se cargaron:  
- `README.md` con acceso a Azure DevOps, instrucciones de uso y estructura del proyecto.  
- `decisiones.md` con justificación de las decisiones tomadas y evidencias del trabajo.  
- Capturas de pantallas de Boards, Sprint, repositorio y Pull Request.  

---

## 6. Problemas encontrados y soluciones
- ❌ Error al importar repo de GitHub por SSH y HTTPS.  
  ✅ Se resolvió creando repo vacío en Azure y subiendo el código manualmente.  
- ❌ Rechazo de `git push` al conectar con GitHub.  
  ✅ Se resolvió usando `git push --force` porque el repo remoto solo tenía un README vacío.  

---

## 7. Conclusión
El TP permitió practicar con **Azure Boards, Sprints, Work Items, Repositorios y Pull Requests**, resolviendo problemas técnicos reales y documentando decisiones.  
Se cumplió con los objetivos planteados y se generó evidencia clara del proceso, tanto en Azure DevOps como en GitHub.
