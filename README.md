<!-- README (HTML) — JS HW #01 -->
<!doctype html>
<html lang="tr">
<head>
  <meta charset="utf-8" />
  <title>goit-js-hw-01 — Ödevler</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root{
      --bg:#0d1117;--card:#161b22;--text:#e6edf3;--muted:#a5b1c2;
      --accent:#2f81f7;--ok:#3fb950;--warn:#d29922;--err:#f85149;
      --code:#0b1220;--border:#30363d;
    }
    html,body{background:var(--bg);color:var(--text);font:16px/1.6 system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue","Noto Sans",Arial,"Apple Color Emoji","Segoe UI Emoji";margin:0}
    .wrap{max-width:980px;margin:40px auto;padding:0 20px}
    .hero{padding:18px 20px;border:1px solid var(--border);border-radius:12px;background:linear-gradient(180deg,var(--card),#111723)}
    h1,h2,h3{line-height:1.2;margin:0 0 .5rem}
    h1{font-size:2rem} h2{font-size:1.25rem;margin-top:2rem}
    p{margin:.5rem 0 1rem}
    .badges{display:flex;gap:.5rem;flex-wrap:wrap;margin:.75rem 0 0}
    .badge{font-size:.75rem;border:1px solid var(--border);border-radius:999px;padding:.2rem .6rem}
    .badge.ok{border-color:var(--ok);color:var(--ok)}
    .badge.warn{border-color:var(--warn);color:var(--warn)}
    .grid{display:grid;gap:16px}
    @media(min-width:800px){.grid{grid-template-columns:1.1fr .9fr}}
    .card{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:16px}
    .meta{color:var(--muted);font-size:.9rem}
    details{border:1px solid var(--border);border-radius:10px;background:var(--card);padding:10px 12px}
    details+details{margin-top:10px}
    summary{cursor:pointer;color:var(--accent);font-weight:600}
    pre{background:var(--code);border:1px solid var(--border);border-radius:10px;padding:12px;overflow:auto}
    code,kbd{font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,"Liberation Mono","Courier New",monospace}
    .checklist li{margin:.25rem 0}
    .sep{height:1px;background:var(--border);margin:24px 0}
    a{color:var(--accent);text-decoration:none}
  </style>
</head>
<body>
  <main class="wrap">
    <section class="hero">
      <h1>JavaScript HW #01 — Görevler</h1>
      <p class="meta">Bu depo; üç ayrı görevi ve her görev için açıklama, örnek kullanım ve kontrol listelerini içerir. Aşağıdaki içeriği doğrudan <code>README.md</code> dosyanıza HTML olarak ekleyebilirsiniz.</p>
      <div class="badges">
        <span class="badge">Dil: JavaScript (ES6)</span>
        <span class="badge">Dosyalar: <code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code></span>
        <span class="badge ok">Durum: Tamamlandı</span>
      </div>
    </section>

    <!-- GÖREV 1 -->
    <section>
      <h2>Görev 1 · Droid Siparişi</h2>
      <div class="grid">
        <div class="card">
          <p><strong>Dosya:</strong> <code>task-1.js</code></p>
          <p><strong>Açıklama:</strong> Tamir droidleri için sipariş özeti döndüren bir fonksiyon yazın.</p>
          <ul>
            <li><code>makeTransaction(quantity, pricePerDroid)</code></li>
            <li><em>quantity</em>: Sipariş adedi (number)</li>
            <li><em>pricePerDroid</em>: Bir droidin fiyatı (number)</li>
          </ul>
          <p><strong>Beklenen çıktı:</strong> <code>"You ordered &lt;quantity&gt; droids worth &lt;totalPrice&gt; credits!"</code></p>

          <details>
            <summary>Doğrulama için örnek çağrılar</summary>
            <pre><code>console.log(makeTransaction(5, 3000)); // "You ordered 5 droids worth 15000 credits!"
console.log(makeTransaction(3, 1000)); // "You ordered 3 droids worth 3000 credits!"
console.log(makeTransaction(10, 500)); // "You ordered 10 droids worth 5000 credits!"</code></pre>
          </details>
        </div>
        <div class="card">
          <h3>Mentör Kontrol Listesi</h3>
          <ul class="checklist">
            <li><code>makeTransaction(quantity, pricePerDroid)</code> tanımlı.</li>
            <li>Toplam: <code>quantity * pricePerDroid</code>.</li>
            <li>Örnek çağrılar beklenen stringi döndürüyor.</li>
            <li>Tüm sonuçlar konsola yazdırılıyor.</li>
            <li>Geçerli argümanlarla doğru sonuç üretir.</li>
          </ul>
        </div>
      </div>
    </section>

    <div class="sep"></div>

    <!-- GÖREV 2 -->
    <section>
      <h2>Görev 2 · Ürün Teslimatı</h2>
      <div class="grid">
        <div class="card">
          <p><strong>Dosya:</strong> <code>task-2.js</code></p>
          <p><strong>Açıklama:</strong> Ülkeye göre toplam teslimat maliyeti mesajı üretin.</p>
          <ul>
            <li><code>getShippingMessage(country, price, deliveryFee)</code></li>
            <li><em>country</em>: Teslimat ülkesi (string)</li>
            <li><em>price</em>: Ürün bedeli (number)</li>
            <li><em>deliveryFee</em>: Teslimat bedeli (number)</li>
          </ul>
          <p><strong>Format:</strong> <code>"Shipping to &lt;country&gt; will cost &lt;totalPrice&gt; credits"</code></p>

          <details>
            <summary>Doğrulama için örnek çağrılar</summary>
            <pre><code>console.log(getShippingMessage("Australia", 120, 50)); // "Shipping to Australia will cost 170 credits"
console.log(getShippingMessage("Germany", 80, 20));    // "Shipping to Germany will cost 100 credits"
console.log(getShippingMessage("Sweden", 100, 20));    // "Shipping to Sweden will cost 120 credits"</code></pre>
          </details>
        </div>
        <div class="card">
          <h3>Mentör Kontrol Listesi</h3>
          <ul class="checklist">
            <li><code>getShippingMessage(country, price, deliveryFee)</code> tanımlı.</li>
            <li>Toplam: <code>price + deliveryFee</code>.</li>
            <li>Örnek çağrılar doğru metni döndürüyor.</li>
            <li>Geçerli argümanlarla doğru sonuç üretir.</li>
          </ul>
        </div>
      </div>
    </section>

    <div class="sep"></div>

    <!-- GÖREV 3 -->
    <section>
      <h2>Görev 3 · Öğe Genişliği (border-box)</h2>
      <div class="grid">
        <div class="card">
          <p><strong>Dosya:</strong> <code>task-3.js</code></p>
          <p><strong>Açıklama:</strong> <code>box-sizing: border-box</code> varsayımıyla toplam genişliği hesaplayın.</p>
          <ul>
            <li><code>getElementWidth(content, padding, border)</code></li>
            <li>Tüm parametreler: <em>"Npx"</em> formatında string (örn. <code>"8px"</code>, <code>"8.5px"</code>)</li>
            <li><strong>border-box</strong>’ta toplam genişlik formülü: <code>content + 2*padding + 2*border</code></li>
          </ul>

          <details>
            <summary>Doğrulama için örnek çağrılar</summary>
            <pre><code>console.log(getElementWidth("50px", "8px", "4px"));     // 74
console.log(getElementWidth("60px", "12px", "8.5px")); // 101
console.log(getElementWidth("200px", "0px", "0px"));   // 200</code></pre>
          </details>
        </div>
        <div class="card">
          <h3>Mentör Kontrol Listesi</h3>
          <ul class="checklist">
            <li><code>getElementWidth(content, padding, border)</code> tanımlı.</li>
            <li><code>px</code> değerleri doğru şekilde sayıya dönüştürülüyor.</li>
            <li>Örnek çağrılar doğru sonucu döndürüyor (74, 101, 200).</li>
            <li>Geçerli argümanlarla doğru sonuç üretir.</li>
          </ul>
        </div>
      </div>
    </section>

    <div class="sep"></div>

    <section class="card">
      <h2>Notlar</h2>
      <ul>
        <li>String formatlama için şablon dizeleri: <code>\`\${value}\`</code></li>
        <li><code>"Npx"</code> → sayıya dönüştürmek için örnek: <code>parseFloat("8.5px")</code> → <code>8.5</code></li>
        <li>Testler için <code>console.log</code> çıktıları eklenmiştir.</li>
      </ul>
      <p class="meta">Soruların olursa issue açabilir ya da PR yorumunda belirtebilirsin. 🎯</p>
    </section>
  </main>
</body>
</html>
