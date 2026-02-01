<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIP CLN | Invitaciones Digitales</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Lato', sans-serif; background-color: #fdf6f0; color: #2c1810; }
        .font-gold { color: #d4a574; }
        .bg-gold { background-color: #d4a574; }
        .font-display { font-family: 'Playfair Display', serif; }
        .card:hover { transform: translateY(-5px); transition: 0.3s; }
    </style>
</head>
<body>

    <header class="p-8 text-center bg-white shadow-sm border-b border-gray-100">
        <h1 class="font-display text-4xl mb-2 text-[#2c1810]">Invitaciones <span class="font-gold text-5xl">VIP</span> CLN</h1>
        <p class="italic text-gray-500 tracking-widest text-xs uppercase">Exclusividad en cada detalle</p>
    </header>

    <section class="p-6 max-w-6xl mx-auto">
        <div id="catalogo" class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-4">
            </div>
    </section>

    <section class="bg-white p-8 border-t-4 border-[#d4a574] mt-20 shadow-2xl">
        <div class="max-w-4xl mx-auto">
            <h3 class="font-display text-2xl mb-6 text-center">⚙️ Panel de Administración</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-8">
                <div class="flex flex-col gap-2">
                    <label class="text-xs font-bold uppercase">Nombre del Diseño</label>
                    <input type="text" id="nombre" placeholder="Ej. Boda Imperial" class="p-3 bg-gray-50 border rounded-lg focus:outline-none focus:border-[#d4a574]">
                </div>
                <div class="flex flex-col gap-2">
                    <label class="text-xs font-bold uppercase">Precio de Renta</label>
                    <input type="text" id="precio" placeholder="Ej. $450" class="p-3 bg-gray-50 border rounded-lg focus:outline-none focus:border-[#d4a574]">
                </div>
                <div class="flex flex-col gap-2 md:col-span-2">
                    <label class="text-xs font-bold uppercase">URL de la Imagen</label>
                    <input type="text" id="imgUrl" placeholder="Pega el link de la foto aquí" class="p-3 bg-gray-50 border rounded-lg focus:outline-none focus:border-[#d4a574]">
                </div>
                <button onclick="agregarInvitacion()" class="bg-black text-white p-4 rounded-lg font-bold mt-2 hover:bg-[#d4a574] transition-all">
                    PUBLICAR EN LA WEB
                </button>
            </div>
        </div>
    </section>

    <script>
        // Tu número de WhatsApp (Culiacán)
        const miWhatsApp = "526671234567"; // <-- CAMBIA ESTO POR TU NÚMERO REAL

        // Cargar datos guardados
        let misInvitaciones = JSON.parse(localStorage.getItem('datosVip')) || [
            {nombre: "Boda Elegance", precio: "$500", img: "https://images.unsplash.com/photo-1607190074257-dd4b7af0309f?w=400"},
            {nombre: "XV Glamour", precio: "$450", img: "https://images.unsplash.com/photo-1519741497674-611481863552?w=400"}
        ];

        function actualizarVista() {
            const contenedor = document.getElementById('catalogo');
            contenedor.innerHTML = '';
            
            misInvitaciones.forEach((inv, index) => {
                contenedor.innerHTML += `
                    <div class="card bg-white rounded-2xl shadow-xl overflow-hidden border border-gray-100 flex flex-col">
                        <img src="${inv.img}" class="w-full h-72 object-cover">
                        <div class="p-6 flex-grow">
                            <h3 class="font-display text-2xl mb-1 text-[#2c1810]">${inv.nombre}</h3>
                            <p class="font-gold font-bold text-lg mb-4">${inv.precio} MXN</p>
                            <a href="https://wa.me/${miWhatsApp}?text=¡Hola! Me interesa rentar el diseño: ${inv.nombre}" 
                               target="_blank" 
                               class="block text-center bg-[#d4a574] text-white py-4 rounded-xl hover:bg-black transition-all font-bold tracking-widest text-sm">
                               PEDIR POR WHATSAPP
                            </a>
                            <button onclick="eliminar(${index})" class="mt-6 w-full text-[10px] text-red-400 uppercase tracking-tighter opacity-50 hover:opacity-100">Eliminar diseño</button>
                        </div>
                    </div>
                `;
            });
            localStorage.setItem('datosVip', JSON.stringify(misInvitaciones));
        }

        function agregarInvitacion() {
            const nombre = document.getElementById('nombre').value;
            const precio = document.getElementById('precio').value;
            const img = document.getElementById('imgUrl').value;

            if(nombre && precio && img) {
                misInvitaciones.push({nombre, precio, img});
                actualizarVista();
                // Limpiar campos
                document.getElementById('nombre').value = '';
                document.getElementById('precio').value = '';
                document.getElementById('imgUrl').value = '';
                alert("✅ ¡Invitación agregada al catálogo!");
            } else {
                alert("❌ Llena todos los campos, plebe.");
            }
        }

        function eliminar(id) {
            if(confirm("¿Seguro que quieres borrar este diseño?")) {
                misInvitaciones.splice(id, 1);
                actualizarVista();
            }
        }

        actualizarVista();
    </script>
</body>
</html>

