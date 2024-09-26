<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Documentación de APIs</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/4.12.0/swagger-ui.css">
</head>
<body>
  <h1>Seleccione la API</h1>
  <select id="api-selector" onchange="loadApi()">
    <option value="">Seleccione una API</option>
    <option value="https://raw.githubusercontent.com/rromerosa/rromerosa.github.io/refs/heads/main/swagger.yaml">API Usuarios</option>
    <option value="https://raw.githubusercontent.com/rromerosa/rromerosa.github.io/refs/heads/main/services/swagger.yaml">API Services</option>
  </select>
  
  <div id="swagger-ui"></div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/4.12.0/swagger-ui-bundle.js"></script>
  <script>
    function loadApi() {
      const apiUrl = document.getElementById('api-selector').value;
      if (apiUrl) {
        SwaggerUIBundle({
          url: apiUrl,
          dom_id: '#swagger-ui',
        });
      }
    }
  </script>
</body>
</html>

