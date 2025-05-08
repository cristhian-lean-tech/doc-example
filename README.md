# 📘 OpenAPI Documentation Template using Swagger UI + GitHub Pages

This repository serves as a **template** to quickly publish and share your OpenAPI documentation (in JSON or YAML format) using **Swagger UI**, hosted for free via

eg. https://cristhian-lean-tech.github.io/doc-example/

**GitHub Pages**.

---

## 🔧 How to Use

Follow these steps to publish your own API documentation:

---

### 1. 🍴 Fork or Clone this Repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. 📄 Replace the API Definition

Replace the file openapi.json with your own OpenAPI file:

- You can rename your file as openapi.json or openapi.yaml
- If you change the file name, update it in index.html accordingly (see step 3)

### 3. 📝 Update the swagger-initializer.js

Update the swagger-initializer.js file to point to your OpenAPI file:

```javascript
window.ui = SwaggerUIBundle({
  url: "openapi.json", // Replace with your file name if needed
  dom_id: "#swagger-ui",
  deepLinking: true,
  presets: [SwaggerUIBundle.presets.apis, SwaggerUIStandalonePreset],
  plugins: [SwaggerUIBundle.plugins.DownloadUrl],
  layout: "StandaloneLayout",
});
```

### 4. 🚀 Push to GitHub

```bash
git add .
git commit -m "Update OpenAPI documentation"
git push
```

### 5. 🌐 Enable GitHub Pages

1. Go to your repo on GitHub
2. Click Settings > Pages
3. Under Source, select main branch and root (/)
4. Save and wait ~30 seconds

You'll receive a public URL like:

```
https://your-username.github.io/your-repo/
```

Share this link with your team
