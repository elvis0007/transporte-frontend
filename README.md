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
    commit id:"Dev2"
    checkout main
    commit id:"Main1"
    merge develop id:"MergeDev"

    branch feature/login
    checkout feature/login
    commit id:"Login1"
    commit id:"Login2"
    checkout develop
    merge feature/login id:"MergeLogin"

    branch feature/venta-boletos
    checkout feature/venta-boletos
    commit id:"Venta1"
    commit id:"Venta2"
    checkout develop
    merge feature/venta-boletos id:"MergeVenta"

    checkout main
    merge develop id:"Release-v1.0"
