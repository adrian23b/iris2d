# Iris2D

Iris2D es un juego de ciudad virtual 2D donde los jugadores construyen, comercian e interactúan en un mundo compartido impulsado por tokens y activos digitales sobre Stellar.

## 🎮 Concepto

Cada jugador comienza con una cantidad inicial de tokens y construye progresivamente su propia ciudad dentro de un mundo compartido.

El jugador podrá:

* Explorar el mundo 2D.
* Obtener recursos.
* Construir estructuras.
* Gestionar su inventario.
* Interactuar con otros jugadores.
* Comerciar recursos.
* Utilizar tokens.
* Conectar una wallet Stellar.
* Realizar transacciones sobre Stellar.
* En futuras versiones, poseer e intercambiar activos digitales del juego.

---

## 🛠️ Stack

* **React**
* **TypeScript**
* **Vite**
* **Stellar Wallets Kit**
* **Stellar Testnet**
* **Supabase / Neon**
* **Vercel**

---

## 🏗️ Arquitectura

El proyecto está organizado en módulos independientes para mantener desacoplados el gameplay, la persistencia y la integración blockchain.

```text
src/
├── app/                    # Aplicación principal
│
├── components/             # Componentes React reutilizables
│
├── game/                   # Núcleo del juego
│   ├── state/              # Estado global del juego
│   ├── world/              # Mundo y mapa 2D
│   ├── player/             # Jugador y movimiento
│   ├── entities/           # Entidades del mundo
│   └── economy/            # Economía del juego
│
├── blockchain/             # Integración con Stellar
│
├── database/               # Persistencia de datos
│
├── services/               # Servicios y comunicación externa
│
├── types/                  # Tipos TypeScript compartidos
│
├── assets/                 # Recursos gráficos
│
└── main.tsx                # Punto de entrada
```

---

## 🔗 Arquitectura de alto nivel

```text
                         IRIS2D
                           │
             ┌─────────────┴─────────────┐
             │                           │
          GAME CORE                 BLOCKCHAIN
             │                           │
      ┌──────┼──────┐             ┌──────┼──────┐
      │      │      │             │      │      │
    World  Player Economy       Wallet  Token  Transactions
      │      │      │             │      │      │
      └──────┼──────┘             └──────┼──────┘
             │                           │
             └─────────────┬─────────────┘
                           │
                     SERVICE LAYER
                           │
                 ┌─────────┴─────────┐
                 │                   │
              Database            Stellar
           Supabase / Neon       Horizon / API
                 │                   │
                 └─────────┬─────────┘
                           │
                         Vercel
```

La lógica del juego se mantiene desacoplada de Stellar mediante una capa de servicios.

Esto permite desarrollar inicialmente el gameplay sin depender de la blockchain y posteriormente conectar las funcionalidades que realmente necesitan operaciones on-chain.

---

# 🚀 Roadmap

## Nivel 1 — Base de aplicación

* [x] Estructura inicial del proyecto
* [ ] App Shell
* [ ] Game State
* [ ] Game UI / HUD

## Nivel 2 — Mundo 2D

* [ ] World Map
* [ ] Player Controller
* [ ] World Entities
* [ ] Interaction System

## Nivel 3 — Economía

* [ ] Player Inventory
* [ ] Resource System
* [ ] Building System
* [ ] Economy System

## Nivel 4 — Persistencia

* [ ] Player Profile
* [ ] Database Layer
* [ ] Game Persistence
* [ ] World Persistence

## Nivel 5 — Integración Stellar

* [ ] Wallet Connection
* [ ] Stellar Account
* [ ] Stellar Service Layer
* [ ] Blockchain Transactions

## Nivel 6 — Economía On-Chain

* [ ] Iris Token
* [ ] Token Rewards
* [ ] Token Transfer
* [ ] Transaction History

## Nivel 7 — Multiplayer

* [ ] Player Presence
* [ ] Player Interaction
* [ ] Trading System
* [ ] Multiplayer Sync

## Nivel 8 — Activos digitales

* [ ] Asset Registry
* [ ] Digital Asset Minting
* [ ] Asset Ownership
* [ ] Asset Marketplace

---

# 🎯 MVP

El objetivo inicial es construir una versión mínima pero funcional de Iris2D.

El flujo principal será:

```text
Jugador
   │
   ▼
Ciudad 2D
   │
   ▼
Movimiento
   │
   ▼
Interacción
   │
   ▼
Obtención de recursos
   │
   ▼
Inventario
   │
   ▼
Construcción
   │
   ▼
Progreso persistente
   │
   ▼
Wallet Stellar
   │
   ▼
Tokens
   │
   ▼
Transacción Stellar
```

---

# 🌐 Stellar

La integración blockchain se desarrollará inicialmente utilizando **Stellar Testnet**.

Stellar será utilizado como capa blockchain para:

* Gestionar la wallet del jugador.
* Consultar cuentas.
* Gestionar tokens.
* Realizar transferencias.
* Registrar transacciones.
* En futuras versiones, gestionar activos digitales del juego.

La lógica del juego no deberá depender directamente de Horizon ni del SDK de Stellar.

La comunicación seguirá conceptualmente esta arquitectura:

```text
Game Module
     │
     ▼
Stellar Service
     │
     ▼
Stellar SDK / Horizon
     │
     ▼
Stellar Testnet
```

---

# 💾 Persistencia

La información del juego que no necesita estar directamente en blockchain será almacenada mediante una base de datos.

Datos candidatos:

* Perfil del jugador.
* Posición.
* Inventario.
* Recursos.
* Edificios.
* Estado del mundo.
* Historial de acciones.
* Información de marketplace.

La aplicación utilizará una capa de abstracción para evitar que los módulos del juego dependan directamente del proveedor de base de datos.

```text
Game
 │
 ▼
Database Service
 │
 ├── Supabase
 │
 └── Neon
```

---

# 📁 Organización por responsabilidades

### `game/`

Contiene la lógica principal del juego.

### `blockchain/`

Contiene todo lo relacionado con Stellar y las wallets.

### `database/`

Contiene la persistencia y acceso a datos.

### `services/`

Contiene servicios externos y APIs.

### `components/`

Contiene componentes visuales reutilizables.

### `types/`

Contiene los tipos compartidos de TypeScript.

### `assets/`

Contiene sprites, imágenes, sonidos y otros recursos del juego.

---

# 💻 Desarrollo

## Requisitos

* Node.js
* npm
* Git

## Instalación

Clonar el repositorio:

```bash
git clone <repository-url>
cd iris2d
```

Instalar dependencias:

```bash
npm install
```

Iniciar el servidor de desarrollo:

```bash
npm run dev
```

La aplicación estará disponible en la URL mostrada por Vite.

---

# 🧪 Desarrollo con Stellar Testnet

Durante el desarrollo se utilizará Stellar Testnet para evitar utilizar activos reales.

La integración blockchain se incorporará progresivamente después de completar la base del juego.

```text
Local Development
       │
       ▼
   Iris2D
       │
       ▼
Stellar Testnet
```

---

# ☁️ Deployment

El frontend será desplegado utilizando **Vercel**.

```text
GitHub
   │
   ▼
 Vercel
   │
   ▼
 Iris2D
```

Los servicios externos y las variables de entorno deberán configurarse independientemente para cada entorno.

---

# 📌 Estado del proyecto

**Estado:** En desarrollo

**Versión:** MVP

**Objetivo actual:** Construir una ciudad virtual 2D funcional e integrar progresivamente una economía basada en Stellar.

---

# 📜 License

Este proyecto se encuentra actualmente en desarrollo.

