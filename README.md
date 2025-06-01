Prueba3.html:
<html>
<head>
<title> Prueba 3 </title>
<hl> Hola Prueba 3
<p> Prueba 3 </p>
</html>
</head>
---------------------
prueba1.html:
<!DOCTYPE html>
<html>
<head>
    <title>Login Form</title>
    <style>
        h1 {
            color: red;
        }
        body {
            text-align: center;
            padding: 13%;
            background-color: #00FF00;
        }
        button {
            border: none;
            background-color: red;
            width: 100px;
            height: 40px;
            border-radius: 50px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Iniciar Sesión</h1>
    <form onsubmit="return validarLogin()">
        Nombre de Usuario:  
        <input type="text" id="username" required><br><br>
        
        Contraseña del Usuario:  
        <input type="password" id="password" required><br>
        
        <!-- Enlace corregido -->
        <a href="file:///C:/Users/59274339/Desktop/Prueba%202/olvide%20la%20contrase%C3%B1a.html">Olvidé mi contraseña</a><br><br>
        
        <button type="submit">Aceptar</button>
    </form>

    <script>
        function validarLogin() {
            const usuario = document.getElementById("username").value;
            const clave = document.getElementById("password").value;

            if (usuario === "Pablo11" && clave === "1234") {
                // Redirige a otra página si los datos son correctos
                window.location.href = "file:///C:/Users/59274339/Desktop/Pruebas/Prueba3.html";
                return false; // Evita que el formulario se envíe normalmente
            } else {
                alert("Usuario o contraseña incorrectos.");
                return false;
            }
        }
    </script>
</body>
</html>




Olvide mi contraseña.html:

<!DOCTYPE html>
<html>
<head>
    <title>Pregunta de Seguridad</title>
    <style>
        body {
            text-align: center;
            padding: 5%;
            background-color: #f0f8ff;
            font-family: Arial, sans-serif;
        }
        h1 {
            color: green;
        }
        input, button {
            margin: 10px;
            padding: 10px;
            width: 250px;
            font-size: 16px;
        }
        .resultado {
            font-weight: bold;
            margin-top: 20px;
            color: blue;
        }
    </style>
</head>
<body>
    <h1>Verificación de identidad</h1>
    <form onsubmit="return verificarRespuestas()">
        <div>
            ¿De qué año eres?<br>
            <input type="text" id="pregunta1" required>
        </div>
        <button type="submit">Verificar</button>
    </form>

    <div class="resultado" id="resultado"></div>

    <script>
        function verificarRespuestas() {
            const p1 = document.getElementById("pregunta1").value.trim().toLowerCase();
            const resultado = document.getElementById("resultado");

            if (p1 === "2011") {
                resultado.innerHTML = "✅ Usuario: <strong>Pablo11</strong><br>✅ Contraseña: <strong>1234</strong>";
            } else {
                resultado.innerHTML = "❌ Respuesta incorrecta. Intenta de nuevo.";
            }

            return false; // Previene recarga de la página
        }
    </script>
</body>
</html>






