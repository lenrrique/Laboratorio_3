# Laboratorio_3



En el codigo HTML encontramos

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web de tarjetas</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1>Tarjetas utilizando JSON
    <div id="tarjetas-container"></div>

    <script src="app.js"></script>
</body>
</html>

En el codigo CSS encontramos 

**.card {
    border: 1px solid #000045;
    border-radius: 8px;
    padding: 16px;
    margin-bottom: 16px;
    color: rgb(27, 58, 168);
}

.card h2 {
    font-size: 18px;
    margin-bottom: 8px;
}

.card p {
    font-size: 14px;
}**

en el codigo Javascript encontramos

fetch ('data.json')
.then(response => response.json())
.then(data => {
const tarjetasContainer=document.getElementById('tarjetas-container');

data.forEach(objeto=>{
const tarjeta = document.createElement('div');
tarjeta.classList.add('card');

const titulo = document.createElement('h2');
titulo.textContent = objeto.titulo;
        
const contenido = document.createElement('p');
contenido.textContent = objeto.contenido;

tarjeta.appendChild(titulo);
tarjeta.appendChild(contenido);

tarjetasContainer.appendChild(tarjeta);
});
})
.catch(error => console.error(error));

En el DataJonhson encontramos

[
    {
        "titulo": "Tarjeta 1",
        "contenido": "Contenido de la tarjeta 1"
    },
    {
        "titulo": "Tarjeta 2",
        "contenido": "Contenido de la tarjeta 2"
    },
    {
        "titulo": "Tarjeta 3",
        "contenido": "Contenido de la tarjeta 3"
    }

]


En la extension encontramos

{
    "recommendations": [
        "ritwickdey.liveserver"
    ]
}
