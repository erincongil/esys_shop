# Contexto del Proyecto: Esy´s Shop (esys_shop)

## 1. Visión General
- **Nombre de la Tienda:** Esy´s Shop (Identificador del proyecto: `esys_shop`).
- **Propósito:** Web e-commerce pequeña para la tienda de ropa Esy´s Shop.
- **Alcance:** Tienda pública (catálogo, carrito, checkout) + Panel de Administración privado para gestión de inventario e imágenes.
- **Despliegue:** Vercel (Plan Hobby).

## 2. Stack Tecnológico Acordado
- **Framework Full-Stack:** Next.js (App Router, TypeScript, Tailwind CSS).
- **ORM:** Prisma ORM.
- **Base de Datos Relacional:** PostgreSQL en la nube (Neon o Supabase) con Connection Pooling.
- **Hosting & Serverless:** Vercel.
- **Almacenamiento de Imágenes:** Cloudinary (vía Upload Widget en Admin + SDK para eliminación por `public_id`).
- **Autenticación:** NextAuth.js (Auth.js v5) con proveedor de Google OAuth y roles (`ADMIN` / `USER`).

## 3. Estado Actual del Proyecto
- Inicialización del repositorio `esys_shop` con `create-next-app` (App Router, src/, Tailwind, TS).
- Dependencias instaladas: `next-auth@beta`, `@prisma/client`, `prisma`.
- Prisma inicializado (`npx prisma init`).

## 4. Próximos Pasos Inmediatos
1. Configurar esquema de Prisma (`prisma/schema.prisma`) para `User`, `Account`, `Product`, `ProductImage`, `Order`.
2. Configurar NextAuth.js v5 con Google Provider en `src/auth.ts` y `src/app/api/auth/[...nextauth]/route.ts`.
3. Crear variables de entorno en `.env.local` (`AUTH_SECRET`, `AUTH_GOOGLE_ID`, `AUTH_GOOGLE_SECRET`, `DATABASE_URL`).
4. Construir la Landing Page inicial de **Esy´s Shop** en `src/app/page.tsx` con el botón de login de Google.