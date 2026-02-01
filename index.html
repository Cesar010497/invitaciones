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
        /* Estilo para que el panel de admin se vea profesional */
        input::placeholder { color: #a0a0a0; }
    </style>
</head>
<body>

    <header class="p-8 text-center bg-white shadow-sm border-b border-gray-100">
        <h1 class="font-display text-4xl mb-2 text-[#2c1810]">Invitaciones <span class="font-gold text-5xl">VIP</span> CLN</h1>
        <p class="italic text-gray-400 tracking-widest text-xs uppercase font-bold">Exclusividad y Elegancia Digital</p>
    </header>

    <section class="p-6 max-w-6xl mx-auto min-h-[400px]">
        <h2 class="font-display text-center text-2xl mb-10 text-[#5a4a42]">Catálogo de Diseños Disponibles</h2>
        <div id="catalogo" class="grid grid-cols-1 md:grid-cols-3 gap-8">
            </div>
    </section>

    <section id="admin" class="bg-white p-8 border-t-4 border-[#d4a574] mt-20 shadow-2xl">
        <div class="max-w-4xl mx-auto">
            <h3 class="font-display text-2xl mb-2 text-center text-[#2c1810]">⚙️ Panel de Gestión</h3>
            <p class="text-center text-gray-500 text-sm mb-8">Agrega o elimina diseños de tu página en tiempo real.</p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 bg-[#f9f9f9] p-6 rounded-2xl border border-gray-200">
                <div class="flex flex-col gap-2">
                    <label class="text-xs font-bold uppercase text-[#d4a574]">Nombre del Diseño</label>
                    <input type="text" id="nombre" placeholder="Ej. XV Años Royal" class="p-3 border rounded-lg focus:ring-2 focus:ring-[#d4a574] outline-none">
                </div>
                <div class="flex flex-col gap-2">
                    <label class="text-xs font-bold uppercase text-[#d4a574]">Precio de Renta (MXN)</label>
                    <input type="text" id="precio" placeholder="Ej. $450" class="p-3 border rounded-lg focus:ring-2 focus:ring-[#d4a574] outline-none">
                </div>
                <div class="flex flex-col gap-2 md:col-span-2">
                    <label class="text-xs font-bold uppercase text-[#d4a574]">Link de la Foto (Canva/Google/Imgur)</label>
                    <input type="text" id="imgUrl" placeholder="Pega el enlace de la imagen aquí" class="p-3 border rounded-lg focus:ring-2 focus:ring-[#d4a574] outline-none">
                </div>
                <button onclick="agregarInvitacion()" class="bg-black text-white p-4 rounded-xl font-bold mt-4 hover:bg-[#d4a574] transition-all shadow-lg active:scale-95 md:col-span-2">
                    PUBLICAR AHORA
                </button>
            </div>
        </div>
    </section>

    <footer class="py-12 text-center text-gray-400 text-[10px] uppercase tracking-widest">
        Invitaciones VIP CLN &copy; 2026 | Hecho para los mejores eventos
    </footer>

    <script>
        // 1. CONFIGURA TU WHATSAPP AQUÍ (Solo números, con 52 al principio)
        const miWhatsApp = "526670000000"; // <-- PON TU NÚMERO AQUÍ

        // 2. Base de datos local (se guarda en tu navegador)
        let misInvitaciones = JSON.parse(localStorage.getItem('datosVip')) || [
            {nombre: "Boda Imperial Gold", precio: "$500", img: "https://images.unsplash.com/photo-1607190074257-dd4b7af0309f?w=500"},
            {nombre: "XV Jardín Secreto", precio: "$450", img: "https://images.unsplash.com/photo-1519741497674-611481863552?w=500"}
        ];

        // 3. Función para pintar las invitaciones en pantalla
        function actualizarVista() {
            const contenedor = document.getElementById('catalogo');
            contenedor.innerHTML = '';

            misInvitaciones.forEach((inv, index) => {
                contenedor.innerHTML += `
                    <div class="card bg-white rounded-3xl shadow-xl overflow-hidden border border-gray-100 flex flex-col">
                        <img src="${inv.img}" class="w-full h-80 object-cover" onerror="this.src='https://via.placeholder.com/400x600?text=Error+al+Cargar+Imagen'">
                        <div class="p-6">
                            <h3 class="font-display text-2xl mb-1 text-[#2c1810]">${inv.nombre}</h3>
                            <p class="font-gold font-bold text-xl mb-5">${inv.precio} MXN</p>
                            <a href="https://wa.me/${miWhatsApp}?text=¡Hola! Me interesa rentar el diseño: ${inv.nombre}" 
                               target="_blank" 
                               class="block text-center bg-[#d4a574] text-white py-4 rounded-2xl hover:bg-black transition-all font-bold tracking-widest text-sm shadow-md">
                               COTIZAR POR WHATSAPP
                            </a>
                            <button onclick="eliminar(${index})" class="mt-6 w-full text-[9px] text-gray-300 uppercase font-bold hover:text-red-500 transition-colors">Remover del catálogo</button>
                        </div>
                    </div>
                `;
            });
            localStorage.setItem('datosVip', JSON.stringify(misInvitaciones));
        }

        // 4. Función para agregar nuevas invitaciones
        function agregarInvitacion() {
            const nombre = document.getElementById('nombre').value;
            const precio = document.getElementById('precio').value;
            const img = document.getElementById('imgUrl').value;

            if(nombre && precio && img) {
                misInvitaciones.push({nombre, precio, img});
                actualizarVista();

                // Limpiar el formulario
                document.getElementById('nombre').value = '';
                document.getElementById('precio').value = '';
                document.getElementById('imgUrl').value = '';

                alert("✨ ¡Invitación publicada con éxito!");
            } else {
                alert("⚠️ Plebe, llena todos los campos para poder publicar.");
            }
        }

        // 5. Función para borrar
        function eliminar(id) {
            if(confirm("¿Seguro que quieres quitar este diseño de la vista pública?")) {
                misInvitaciones.splice(id, 1);
                actualizarVista();
            }
        }

        // Ejecutar al cargar la página
        actualizarVista();
    </script>
</body>
</html>