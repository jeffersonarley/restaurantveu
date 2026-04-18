<script setup>
import { ref } from 'vue'

// 1. VECTOR DE 40 PRODUCTOS
const productos = ref([
  { id: 1, nombre: "Hamburguesa Sencilla", precio: 15000, imagen: "https://images.unsplash.com/photo-1571091718767-18b5b1457add?w=300" },
  { id: 2, nombre: "Hamburguesa Doble Queso", precio: 19000, imagen: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=300" },
  { id: 3, nombre: "Hamburguesa Triple Carne", precio: 25000, imagen: "https://images.unsplash.com/photo-1550317138-10000687ad32?w=300" },
  { id: 4, nombre: "Perro Caliente Clásico", precio: 12000, imagen: "https://images.unsplash.com/photo-1541214113241-21578d2d9b62?w=300" },
  { id: 5, nombre: "Perro Especial con Tocineta", precio: 17000, imagen: "https://images.unsplash.com/photo-1627023411197-6851b69422d1?w=300" },
  { id: 6, nombre: "Perro Suizo", precio: 18500, imagen: "https://images.unsplash.com/photo-1599129900704-f3674b304c6c?w=300" },
  { id: 7, nombre: "Pizza Pepperoni Mediana", precio: 25000, imagen: "https://images.unsplash.com/photo-1628840042765-356cda07504e?w=300" },
  { id: 8, nombre: "Pizza Hawaiana Mediana", precio: 24000, imagen: "https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=300" },
  { id: 9, nombre: "Pizza 4 Quesos", precio: 28000, imagen: "https://images.unsplash.com/photo-1513104890138-7c749659a591?w=300" },
  { id: 10, nombre: "Pizza Vegetariana", precio: 22000, imagen: "https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?w=300" },
  { id: 11, nombre: "Pizza Carnes Frías", precio: 30000, imagen: "https://images.unsplash.com/photo-1574071318508-1cdbad80ad50?w=300" },
  { id: 12, nombre: "Bandeja Paisa Completa", precio: 32000, imagen: "https://images.unsplash.com/photo-1626700051175-656a42eaa5e3?w=300" },
  { id: 13, nombre: "Mote de Queso Grande", precio: 18000, imagen: "https://images.unsplash.com/photo-1547592166-23ac45744acd?w=300" },
  { id: 14, nombre: "Arroz Atollado", precio: 22000, imagen: "https://images.unsplash.com/photo-1512058564366-18510be2db19?w=300" },
  { id: 15, nombre: "Ajiaco Santafereño", precio: 20000, imagen: "https://images.unsplash.com/photo-1547592166-23ac45744acd?w=300" },
  { id: 16, nombre: "Pechuga a la Plancha", precio: 19000, imagen: "https://images.unsplash.com/photo-1532550907401-a500c9a57435?w=300" },
  { id: 17, nombre: "Costillas BBQ (500g)", precio: 38000, imagen: "https://images.unsplash.com/photo-1544025162-d76694265947?w=300" },
  { id: 18, nombre: "Sobrebarriga al Horno", precio: 26000, imagen: "https://images.unsplash.com/photo-1603048588665-791ca8aea617?w=300" },
  { id: 19, nombre: "Salchipapa Clásica", precio: 14000, imagen: "https://images.unsplash.com/photo-1585109649139-366815a0d713?w=300" },
  { id: 20, nombre: "Salchipapa Mega Ranchera", precio: 28000, imagen: "https://images.unsplash.com/photo-1619740455993-9e612b1af08a?w=300" },
  { id: 21, nombre: "Alitas BBQ x12", precio: 26000, imagen: "https://images.unsplash.com/photo-1527477396000-e27163b481c2?w=300" },
  { id: 22, nombre: "Nuggets de Pollo x10", precio: 12000, imagen: "https://images.unsplash.com/photo-1562967914-608f82629710?w=300" },
  { id: 23, nombre: "Papas Francesas Grandes", precio: 8000, imagen: "https://images.unsplash.com/photo-1573080496219-bb080dd4f877?w=300" },
  { id: 24, nombre: "Empanadas de Carne (5)", precio: 10000, imagen: "https://images.unsplash.com/photo-1628191010210-a59de33e5941?w=300" },
  { id: 25, nombre: "Tacos de Res (3 unidades)", precio: 18000, imagen: "https://images.unsplash.com/photo-1552332386-f8dd00dc2f85?w=300" },
  { id: 26, nombre: "Burrito Mixto Gigante", precio: 21000, imagen: "https://images.unsplash.com/photo-1626700051175-656a42eaa5e3?w=300" },
  { id: 27, nombre: "Desayuno Americano", precio: 15000, imagen: "https://images.unsplash.com/photo-1533089860892-a7c6f0a88666?w=300" },
  { id: 28, nombre: "Calentado con Huevo", precio: 14000, imagen: "https://images.unsplash.com/photo-1525351484163-7529414344d8?w=300" },
  { id: 29, nombre: "Sándwich Cubano Pro", precio: 16000, imagen: "https://images.unsplash.com/photo-1525351326368-efbb5cb6814d?w=300" },
  { id: 30, nombre: "Bowl de Frutas Frescas", precio: 12000, imagen: "https://images.unsplash.com/photo-1512621776951-a57141f2eefd?w=300" },
  { id: 31, nombre: "Jugo Natural en Agua", precio: 5000, imagen: "https://images.unsplash.com/photo-1544054468-b7d2f415fa58?w=300" },
  { id: 32, nombre: "Jugo Natural en Leche", precio: 7000, imagen: "https://images.unsplash.com/photo-1556881286-fc6915169721?w=300" },
  { id: 33, nombre: "Limonada Cerezada", precio: 8500, imagen: "https://images.unsplash.com/photo-1513558161293-cdaf765ed2fd?w=300" },
  { id: 34, nombre: "Gaseosa Personal", precio: 4000, imagen: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?w=300" },
  { id: 35, nombre: "Té Frío de la Casa", precio: 6000, imagen: "https://images.unsplash.com/photo-1499638673689-79a0b5115d87?w=300" },
  { id: 36, nombre: "Cerveza Club Colombia", precio: 7000, imagen: "https://images.unsplash.com/photo-1503572326578-831005663749?w=300" },
  { id: 37, nombre: "Agua Mineral sin Gas", precio: 3500, imagen: "https://images.unsplash.com/photo-1548839140-29a749e1cf3d?w=300" },
  { id: 38, nombre: "Brownie con Helado", precio: 9500, imagen: "https://images.unsplash.com/photo-1564355808539-22fda35bcd7e?w=300" },
  { id: 39, nombre: "Flan de Caramelo", precio: 7000, imagen: "https://images.unsplash.com/photo-1528975604071-b4dc52a2d18c?w=300" },
  { id: 40, nombre: "Malteada de Chocolate", precio: 13000, imagen: "https://images.unsplash.com/photo-1572490122747-3968b75cc699?w=300" }
])

// 2. ESTADOS
const carrito = ref(JSON.parse(localStorage.getItem('carrito')) || [])
const totalDinero = ref(0)
const cargando = ref(false)
const mensajeExito = ref("")

// 3. LÓGICA MANUAL (SIN COMPUTED NI WATCH)
const calcularTotalFactura = () => {
  let acumulado = 0
  for (let i = 0; i < carrito.value.length; i++) {
    acumulado += carrito.value[i].precio
  }
  totalDinero.value = acumulado
}

// Ejecutar al inicio para cargar total del LocalStorage
calcularTotalFactura()

const agregarProducto = (p) => {
  cargando.value = true // Activa Spinner
  
  setTimeout(() => {
    carrito.value.push(p)
    localStorage.setItem('carrito', JSON.stringify(carrito.value))
    calcularTotalFactura() // Actualización manual
    
    cargando.value = false
    mensajeExito.value = `¡${p.nombre} agregado! ✅`
    
    setTimeout(() => { mensajeExito.value = "" }, 2000) // Notificación temporal
  }, 400)
}

const limpiarTodo = () => {
  if(confirm("¿Deseas vaciar tu pedido?")) {
    carrito.value = []
    localStorage.removeItem('carrito')
    totalDinero.value = 0
  }
}
</script>

<template>
  <div v-if="cargando" class="spinner-overlay">
    <div class="loader"></div>
  </div>

  <div v-if="mensajeExito" class="toast">
    {{ mensajeExito }}
  </div>

  <div class="app">
    <header class="header">
      <div class="brand">🍔 Sabor Real</div>
      <div class="cart-box">
        <span class="cart-icon">🛒</span>
        <span class="cart-count">{{ carrito.length }}</span>
        <span class="cart-total">$ {{ totalDinero }}</span>
      </div>
    </header>

    <main class="content">
      <section v-if="carrito.length > 0" class="factura-container">
        <div class="ticket">
          <h3>RECIBO DE PEDIDO</h3>
          <p>----------------------------</p>
          <div v-for="(item, index) in carrito" :key="index" class="ticket-item">
             {{ item.nombre }} <span>${{ item.precio }}</span>
          </div>
          <p>----------------------------</p>
          <div class="ticket-total">TOTAL A PAGAR: ${{ totalDinero }}</div>
          <button @click="limpiarTodo" class="btn-clear">Vaciar Carrito</button>
        </div>
      </section>

      <h2 class="menu-title">Nuestra Carta (40 opciones)</h2>
      <div class="grid">
        <div v-for="p in productos" :key="p.id" class="card">
          <div class="image-wrapper">
            <img :src="p.imagen" alt="">
            <div class="price-badge">${{ p.precio }}</div>
          </div>
          <div class="card-info">
            <h4>{{ p.nombre }}</h4>
            <button @click="agregarProducto(p)" class="btn-add">Agregar al Carrito</button>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
/* RESET & BASE */
.app { font-family: sans-serif; background: #f4f4f4; min-height: 100vh; padding-top: 80px; }

/* HEADER */
.header {
  position: fixed; top: 0; width: 100%; height: 70px;
  background: #2d3436; color: white;
  display: flex; justify-content: space-between; align-items: center;
  padding: 0 40px; box-shadow: 0 4px 10px rgba(0,0,0,0.3); z-index: 100;
}
.brand { font-size: 1.5rem; font-weight: bold; color: #fab1a0; }
.cart-box { background: #e17055; padding: 8px 15px; border-radius: 30px; display: flex; align-items: center; gap: 10px; }
.cart-count { background: white; color: #e17055; padding: 2px 8px; border-radius: 50%; font-weight: bold; }

/* SPINNER */
.spinner-overlay {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(255,255,255,0.7); display: flex; justify-content: center; align-items: center; z-index: 1000;
}
.loader { border: 5px solid #f3f3f3; border-top: 5px solid #e17055; border-radius: 50%; width: 50px; height: 50px; animation: spin 0.8s linear infinite; }
@keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

/* TOAST NOTIFICATION */
.toast {
  position: fixed; bottom: 20px; right: 20px; background: #00b894; color: white;
  padding: 15px 30px; border-radius: 10px; z-index: 1000; box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

/* FACTURA STYLE */
.ticket {
  background: #fffbe6; padding: 20px; border: 1px dashed #333;
  width: 100%; max-width: 350px; margin: 0 auto 30px; font-family: 'Courier New', Courier, monospace;
}
.ticket-item { display: flex; justify-content: space-between; font-size: 0.9rem; margin-bottom: 5px; }
.ticket-total { font-weight: bold; font-size: 1.1rem; border-top: 1px solid #333; margin-top: 10px; padding-top: 10px; }
.btn-clear { background: #d63031; color: white; border: none; padding: 10px; margin-top: 15px; width: 100%; cursor: pointer; }

/* GRID */
.grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; padding: 20px; }
.card { background: white; border-radius: 15px; overflow: hidden; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
.image-wrapper { position: relative; height: 160px; }
.image-wrapper img { width: 100%; height: 100%; object-fit: cover; }
.price-badge { position: absolute; top: 10px; right: 10px; background: rgba(0,0,0,0.7); color: white; padding: 4px 8px; border-radius: 5px; }
.card-info { padding: 15px; text-align: center; }
.btn-add { background: #0984e3; color: white; border: none; width: 100%; padding: 10px; border-radius: 8px; cursor: pointer; font-weight: bold; }
.btn-add:hover { background: #74b9ff; }
</style>