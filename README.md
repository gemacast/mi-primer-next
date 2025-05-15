# Mi primer proyecto Next.js

## Descripción
Proyecto creado como práctica para aprender los conceptos básicos de Next.js.

## Pasos realizados

1. **Creación del proyecto:**
   - Comando usado:
     ```bash
     npx create-next-app@latest
     ```
   - Configuración seleccionada:
     - No TypeScript
     - Sí ESLint
     - No Tailwind CSS
     - Sí carpeta src/
     - Sí App Router
     - No alias personalizados

2. **Primer arranque del servidor de desarrollo:**
   - Comando usado:
     ```bash
     npm run dev
     ```
   - Resultado:
     - Proyecto visible en: [http://localhost:3000](http://localhost:3000)

3. **Creación de páginas:**
   - `/`: Home con el texto **"Bienvenido a la Home"**
   - `/about`: Página Sobre mí
   - `/contact`: Página Contacto

## Próximos pasos
- Crear un Header reutilizable con enlaces de navegación.
- Aplicar estilos generales y de componentes.

---
## Aplicación de Estilos

### Estilos Globales

- Archivo editado: `/src/app/globals.css`
- Se definieron estilos globales para:
  - Reset de márgenes y paddings.
  - Estilo general del body (fondo, color, fuente, padding).
  - Estilos para encabezados (`h1`, `h2`, `h3`).
  - Estilos para enlaces (`a` y `a:hover`).
  - Estilo de la navegación (`header` y `nav ul`).
  - Contenedor principal (`main`) con fondo blanco, bordes redondeados y sombra.

### Implementación del Contenedor Main

- Se aplicó un `<main>` en las páginas para aprovechar los estilos globales.
- Ejemplo en `/src/app/page.js`:

```jsx
export default function HomePage() {
  return (
    <main>
      <h1>Bienvenido a la Home</h1>
      <p>Esta es la página principal de mi primer proyecto en Next.js.</p>
    </main>
  );
}
```

### Componente Footer (opcional)

- Archivo creado: `/src/components/Footer.js`
- Contenido:

```jsx
export default function Footer() {
  return (
    <footer style={{ marginTop: '2rem', padding: '1rem 0', textAlign: 'center', borderTop: '1px solid #ddd' }}>
      <p>© {new Date().getFullYear()} Gemma Castells. Todos los derechos reservados.</p>
    </footer>
  );
}
```
Integración realizada en /src/app/layout.js después del {children} para que aparezca en todas las páginas:

```jsx
import Footer from '../components/Footer';

// dentro del <body>
<Header />
{children}
<Footer />
```


_Proyecto realizado por Gemma Castells como práctica de Daw._
