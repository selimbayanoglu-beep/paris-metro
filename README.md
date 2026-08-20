# Paris Metro

Paris'te serbest yazılmış başlangıç ve varış konumlarını en yakın Metro/RER istasyonlarına eşleyip rota önerisi sunan web uygulaması.

## Özellikler

- Başlangıç ve varış konumu arama
- Adres/konum bilgisini koordinata çevirme
- En yakın Metro/RER istasyonunu hesaplama
- Paris metro ağı üzerinde rota önerisi
- Bonjour RATP haritalarına yönlendirme
- Netlify Function üzerinden canlı trafik verisi desteği
- Responsive arayüz

## Yerelde çalıştırma

Derleme gerektirmez.

```bash
python3 -m http.server 8080
```

Sonra tarayıcıdan:

```text
http://localhost:8080
```

## Netlify'a dağıtma

```bash
npx netlify-cli deploy --prod --dir=. --functions=netlify/functions
```

Canlı trafik özelliği kullanılıyorsa Netlify ortam değişkenlerine `IDFM_API_KEY` eklenmelidir.

> API anahtarlarını GitHub reposuna veya kaynak koda eklemeyin.

## Dosya yapısı

```text
.
├── index.html
├── style.css
├── enhancements.css
├── traffic-neutral.css
├── app.js
├── official-network.js
├── alternatif-test.html
├── package.json
├── netlify.toml
└── netlify/
    └── functions/
        └── traffic.mjs
```
