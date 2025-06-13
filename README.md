## 🧠 **Design Pattern in React Native (2025 Overview)**

React Native è un framework flessibile, orientato alla composizione. I pattern emergono dall’uso della libreria React + ecosistema JS (Redux, MobX, Zustand, ecc.). Ecco quelli più importanti:

---

### 🧱 **1. Component Pattern (Composite)**

> React Native si basa sulla **composizione di componenti**: il pattern fondamentale.

* Ogni UI è un albero di componenti annidati
* Favorisce il riuso, la chiarezza e la separazione di responsabilità

📌 *Esempio: `<Button />`, `<Card><CardBody /></Card>`*

---

### 🧠 **2. [MVI](<https://github.com/DavideNas/Architectural-Patterns/blob/main/Architetture%20SW/MVI.md>) / [MVVM](<https://github.com/DavideNas/Architectural-Patterns/blob/main/Architetture%20SW/MVVM.md>) Pattern**

> Architetture **reactive-oriented** per app complesse.

* **Model**: stato globale (Redux/Zustand/MobX)
* **View**: componenti React Native
* **Intent/ViewModel**: gestione azioni, side-effects, logica

📌 *Usato con Redux Toolkit, Zustand, o React Query + custom hooks*

---

### 🧩 **3. [Observer Pattern](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Observer/Observer.md>)**

> React (e librerie come MobX, Zustand) usano il pattern Observer:

* Il componente **"osserva"** lo stato e si ri-renderizza al cambiamento
* Perfetto per app responsive e reactive

📌 *Esempio: `useSelector()`, `zustand.subscribe()`*

---

### 🧰 **4. [Factory Pattern](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Factory%20Method.md>)**

> Usato per creare componenti o configurazioni dinamiche.

* Navigation routes dinamiche
* Componenti UI generati da schema
* API factory (es. Axios instances, RTK Query)

📌 *Esempio: `createStackNavigator()`, `createApi()` di Redux Toolkit*

---

### 🧼 **5. [Decorator](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Decorator.md>) / HOC Pattern**

> Pattern classico React: Higher-Order Components (HOC).

* Aggiungono comportamenti a componenti senza modificarli
* Alternativa moderna: custom hooks

📌 *Esempio: `withNavigation`, `connect()` (Redux), `withErrorBoundary()`*

---

### 🔄 **6. [Command](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Command.md>) / Intent Pattern**

> Le azioni (Intent) sono comandi che modificano lo stato:

* `dispatch({ type: 'ADD_TO_CART' })`
* I reducer/handlers eseguono il comando

📌 *Core in Redux, MVI, Flux*

---

### 🌐 **7. [Adapter Pattern](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Adapter.md>)**

> Serve ad **astrarre librerie native, API o bridge JS-Native**.

* Wrapper per moduli nativi (fotocamera, Bluetooth, biometria)
* Adapter per logiche di rete, persistenza

📌 *Esempio: `SecureStoreAdapter.saveToken()`, `CameraModule.capture()`*

---

### 📡 **8. Pub/Sub Pattern**

> Spesso usato con event emitter o global bus (es. per notifiche o comunicazione cross-component):

* `EventEmitter.emit('user-logged-in')`
* Ottimo in app con tab navigation o deep linking

📌 *Esempio: `DeviceEventEmitter`, `event-bus` custom*

---

### 🧪 **9. [Strategy Pattern](<https://github.com/DavideNas/Design-Patterns-and-Angular/blob/main/Patterns%20Example/Strategy/Strategy.md>)**

> Usato per astrarre comportamenti intercambiabili:

* Strategie di autenticazione
* Gestione di errori, retry policies

📌 *Esempio: `auth.login(strategy: 'google')`*

---

### 📚 **In sintesi:**

| Pattern           | Dove lo trovi in React Native            |
| ----------------- | ---------------------------------------- |
| **Composite**     | Struttura a componenti React             |
| **MVI / MVVM**    | Architetture reactive con Redux, Zustand |
| **Observer**      | Stato → UI reattiva                      |
| **Factory**       | Navigazione, API, istanze dinamiche      |
| **HOC/Decorator** | Connessioni e comportamenti estendibili  |
| **Command**       | Action/dispatch in Redux                 |
| **Adapter**       | Accesso a moduli nativi o API            |
| **Pub/Sub**       | Eventi cross-componenti                  |
| **Strategy**      | Varianti intercambiabili di logica       |

---
