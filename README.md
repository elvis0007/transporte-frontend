# 🌳 Estructura de Ramas del Proyecto Frontend

Este repositorio sigue una estructura de ramas basada en **Git Flow**, con ramas principales y ramas de desarrollo y características.

---

## 🧩 Estructura de Ramas

- **main** → Contiene el código estable y listo para producción.  
- **develop** → Se utiliza para integrar nuevas características antes de pasarlas a `main`.  
- **feature/** → Ramas temporales para desarrollar nuevas funciones o módulos.  
  Ejemplo: `feature/login`, `feature/dashboard`, `feature/api-integration`

---

## 🧠 Diagrama de Flujo de Ramas (Mermaid)

Para visualizar el siguiente diagrama correctamente:

1. Abre este README en **VS Code**.  
2. Instala la extensión **Markdown Preview Mermaid Support**.  
3. O visita 👉 [https://mermaid.live/](https://mermaid.live/) y pega el código del diagrama.

```mermaid
gitGraph
    commit id:"Init"
    branch develop
    commit id:"Dev1"
    checkout main
    commit id:"Main1"
    merge develop id:"MergeDev"
    
    branch feature
    checkout feature
    commit id:"Feat1"
    commit id:"Feat2"
    checkout main
    merge feature id:"MergeFeat"
