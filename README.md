# Actividad: Gemini vs Vertex AI

## Contexto
En este trabajo, se toma un caso hipotético de una startup educativa pequeña con presupuesto limitado y sin requisitos regulatorios especiales. Se comparan dos opciones de Google para trabajar con modelos de IA generativa:
- **API de Gemini**: más accesible, flexible, ideal para startups y MVPs
- **Vertex AI**: más robusta, segura, orientada a empresas grandes con requisitos de compliance

## Instalación

### 1. Crear entorno virtual

```bash
python -m venv venv
source venv/Scripts/activate  # Windows bash/PowerShell
# o
venv\Scripts\activate  # Windows cmd
```

### 2. Instalar dependencias

```bash
pip install google-genai python-dotenv jupyter
```

### 3. Configurar credenciales

1. Copia `.env.example` a `.env`:
   ```bash
   cp .env.example .env
   ```

2. Edita `.env` y añade tu API key de Google:
   ```
   GOOGLE_API_KEY=tu_clave_aqui
   ```

   Para obtener la clave:
   - Visita [Google AI Studio](https://aistudio.google.com/)
   - Ve a "Get API key" → "Create new secret key"

### 4. Ejecutar el notebook

```bash
jupyter notebook SDK_actividad.ipynb
```

## Estructura del notebook

| Descripción | Requiere API |
|-------|-------------|--------------|
| Análisis de escenario | ✗ |
| Configuración y verificación | ✗ |
| `generate_content` básico | ✓ |
| `generate_content_stream` | ✓ |
|  Multimodal (imagen) | ✓ |


## Resolución de problemas

### Error: `ModuleNotFoundError: No module named 'google.genai'`
→ Instala: `pip install google-genai`

### Error: `GOOGLE_API_KEY no encontrada`
→ Verifica que `.env` existe y tiene el formato correcto

### Respuesta vacía en multimodal
→ Verifica que la ruta de la imagen es correcta y el formato MIME coincide

## Notas

- Los modelos cambian; verifica la [documentación oficial](https://ai.google.dev/)

