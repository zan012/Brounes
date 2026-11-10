<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>RotiRapi — Bakery Distribution System</title>
    <style>
      :root {
        --bg: #f5f6f8;
        --panel: #fff;
        --ink: #202633;
        --muted: #778091;
        --line: #e8ebf0;
        --brand: #276653;
        --brand2: #e8f3ee;
        --orange: #e99b4b;
        --red: #c65d5d;
        --shadow: 0 8px 24px rgba(29, 42, 55, 0.05);
      }
      * {
        box-sizing: border-box;
      }
      body {
        margin: 0;
        background: var(--bg);
        color: var(--ink);
        font:
          14px/1.5 Inter,
          ui-sans-serif,
          system-ui,
          -apple-system,
          Segoe UI,
          sans-serif;
      }
      button,
      input,
      select {
        font: inherit;
      }
      button {
        cursor: pointer;
      }
      .app {
        display: flex;
        min-height: 100vh;
      }
      .sidebar {
        width: 245px;
        background: #172b27;
        color: #fff;
        padding: 24px 16px;
        display: flex;
        flex-direction: column;
        gap: 24px;
        flex-shrink: 0;
      }
      .brand {
        display: flex;
        align-items: center;
        gap: 11px;
        padding: 0 10px;
      }
      .brandmark {
        width: 38px;
        height: 38px;
        border-radius: 12px;
        background: #d8eee3;
        color: #205b46;
        display: grid;
        place-items: center;
        font-size: 20px;
      }
      .brand strong {
        font-size: 17px;
        letter-spacing: 0.2px;
      }
      .brand small {
        display: block;
        color: #a9beb5;
        font-size: 11px;
      }
      .navlabel {
        font-size: 10px;
        letter-spacing: 1.5px;
        color: #8da59a;
        padding: 0 12px;
        margin-bottom: 5px;
      }
      .nav {
        display: grid;
        gap: 5px;
      }
      .nav button {
        border: 0;
        background: transparent;
        color: #c5d2cc;
        text-align: left;
        padding: 11px 12px;
        border-radius: 9px;
        display: flex;
        gap: 12px;
        align-items: center;
      }
      .nav button.active,
      .nav button:hover {
        background: #29453d;
        color: white;
      }
      .nav .ico {
        width: 19px;
        text-align: center;
        font-size: 16px;
      }
      .sidebottom {
        margin-top: auto;
        color: #9fb4aa;
        font-size: 11px;
        padding: 12px;
      }
      .main {
        flex: 1;
        min-width: 0;
      }
      .topbar {
        height: 70px;
        background: #fff;
        border-bottom: 1px solid var(--line);
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 34px;
        position: sticky;
        top: 0;
        z-index: 4;
      }
      .crumb {
        color: var(--muted);
        font-size: 12px;
      }
      .user {
        display: flex;
        align-items: center;
        gap: 10px;
        font-size: 12px;
      }
      .avatar {
        width: 32px;
        height: 32px;
        border-radius: 50%;
        background: #e4eee8;
        color: #276653;
        display: grid;
        place-items: center;
        font-weight: 700;
      }
      .content {
        padding: 30px 34px;
        max-width: 1500px;
        margin: auto;
      }
      .pagehead {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        gap: 16px;
        margin-bottom: 24px;
      }
      .eyebrow {
        color: var(--brand);
        font-size: 11px;
        font-weight: 700;
        letter-spacing: 1.2px;
        text-transform: uppercase;
      }
      .pagehead h1 {
        font-size: 25px;
        margin: 4px 0;
        font-weight: 750;
        letter-spacing: -0.7px;
      }
      .sub {
        color: var(--muted);
        margin: 0;
      }
      .btn {
        border: 1px solid var(--line);
        background: #fff;
        color: var(--ink);
        padding: 9px 13px;
        border-radius: 9px;
        font-weight: 600;
        font-size: 12px;
        transition: 0.2s;
      }
      .btn:hover {
        background: #f8faf9;
      }
      .btn.primary {
        background: var(--brand);
        border-color: var(--brand);
        color: #fff;
      }
      .btn.primary:hover {
        background: #205b46;
      }
      .btn.danger {
        color: #fff;
        background: var(--red);
        border-color: var(--red);
      }
      .btn.danger:hover {
        background: #b04e4e;
      }
      .actions {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
      }
      .grid {
        display: grid;
        gap: 15px;
      }
      .stats {
        grid-template-columns: repeat(4, minmax(0, 1fr));
        margin-bottom: 18px;
      }
      .card {
        background: var(--panel);
        border: 1px solid var(--line);
        border-radius: 13px;
        padding: 18px;
        box-shadow: var(--shadow);
      }
      .stat-top {
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: var(--muted);
        font-size: 12px;
      }
      .stat-icon {
        width: 33px;
        height: 33px;
        border-radius: 10px;
        background: #edf5f0;
        display: grid;
        place-items: center;
        color: var(--brand);
        font-size: 16px;
      }
      .stat-value {
        font-size: 24px;
        font-weight: 750;
        letter-spacing: -0.7px;
        margin: 13px 0 2px;
      }
      .stat-foot {
        font-size: 11px;
        color: var(--muted);
      }
      .two {
        grid-template-columns: 1.35fr 1fr;
      }
      .section-title {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
      }
      .section-title h3 {
        font-size: 14px;
        margin: 0;
      }
      .section-title span {
        font-size: 11px;
        color: var(--muted);
      }
      .campusrow {
        display: flex;
        align-items: center;
        gap: 10px;
        margin: 17px 0;
      }
      .campusrow .name {
        width: 100px;
        font-size: 12px;
        font-weight: 600;
      }
      .track {
        height: 8px;
        background: #eef0f2;
        border-radius: 8px;
        flex: 1;
        overflow: hidden;
      }
      .fill {
        height: 100%;
        border-radius: 8px;
        transition: width 0.4s ease;
      }
      .amount {
        font-size: 11px;
        width: 100px;
        text-align: right;
        line-height: 1.2;
      }
      .tablewrap {
        overflow: auto;
        background: white;
        border: 1px solid var(--line);
        border-radius: 12px;
        box-shadow: var(--shadow);
      }
      .tablewrap.scrollable {
        max-height: 480px;
        overflow-y: auto;
      }
      .tablewrap.scrollable th {
        position: sticky;
        top: 0;
        z-index: 2;
        box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
      }
      table {
        width: 100%;
        border-collapse: collapse;
        white-space: nowrap;
      }
      th,
      td {
        padding: 12px 15px;
        text-align: left;
        border-bottom: 1px solid var(--line);
        font-size: 12px;
      }
      th {
        background: #fafbfc;
        color: var(--muted);
        font-size: 10px;
        text-transform: uppercase;
        letter-spacing: 0.7px;
      }
      tr:last-child td {
        border-bottom: 0;
      }
      .pill {
        display: inline-flex;
        padding: 4px 8px;
        border-radius: 20px;
        font-size: 10px;
        font-weight: 700;
        background: #edf5f0;
        color: var(--brand);
        align-items: center;
        justify-content: center;
      }
      .empty {
        padding: 35px;
        text-align: center;
        color: var(--muted);
      }
      .formgrid {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 13px;
      }
      .formgrid.four-cols {
        grid-template-columns: repeat(4, minmax(0, 1fr));
      }
      .field {
        display: grid;
        gap: 5px;
      }
      .field label {
        font-size: 11px;
        font-weight: 700;
        color: #5e6877;
      }
      .field input,
      .field select {
        width: 100%;
        padding: 10px;
        border: 1px solid var(--line);
        border-radius: 8px;
        background: white;
        color: var(--ink);
      }
      .modalback {
        position: fixed;
        inset: 0;
        background: #101c1b80;
        display: none;
        align-items: center;
        justify-content: center;
        padding: 18px;
        z-index: 10;
      }
      .modalback.show {
        display: flex;
      }
      .modal {
        width: min(620px, 100%);
        max-height: 90vh;
        overflow: auto;
        background: white;
        border-radius: 15px;
        padding: 22px;
        box-shadow: 0 20px 60px #0003;
      }
      .modalhead {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 18px;
      }
      .modalhead h2 {
        font-size: 17px;
        margin: 0;
      }
      .close {
        border: 0;
        background: #f1f3f4;
        border-radius: 8px;
        width: 30px;
        height: 30px;
      }
      .modalfoot {
        display: flex;
        justify-content: flex-end;
        gap: 8px;
        margin-top: 20px;
      }
      .hint {
        background: #f3f7f4;
        border-radius: 9px;
        padding: 11px;
        color: #527061;
        font-size: 11px;
        margin: 12px 0;
      }
      .reportgrid {
        grid-template-columns: repeat(3, 1fr);
      }
      .reportbox {
        background: #f8faf9;
        border: 1px solid var(--line);
        border-radius: 10px;
        padding: 14px;
      }
      .reportbox small {
        color: var(--muted);
      }
      .reportbox strong {
        display: block;
        font-size: 19px;
        margin-top: 5px;
      }
      .search-bar-container {
        display: flex;
        margin-bottom: 12px;
      }
      .search-input {
        width: 100%;
        max-width: 320px;
        padding: 9px 14px;
        border: 1px solid var(--line);
        border-radius: 8px;
        font-size: 13px;
        outline: none;
      }
      .search-input:focus {
        border-color: var(--brand);
        box-shadow: 0 0 0 3px var(--brand2);
      }
      .footer {
        color: #9aa2ad;
        font-size: 10px;
        text-align: center;
        padding: 25px;
      }
      #toast {
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: #202633;
        color: #fff;
        padding: 12px 24px;
        border-radius: 8px;
        z-index: 9999;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        font-size: 13px;
        font-weight: 600;
        opacity: 0;
        transition: opacity 0.3s;
        display: none;
      }
      #toast.error {
        background: #c62828;
      }
      @media (max-width: 900px) {
        .sidebar {
          width: 70px;
          padding: 18px 9px;
        }
        .brand {
          padding: 0 7px;
        }
        .brand strong,
        .brand small,
        .navlabel,
        .nav button span:not(.ico),
        .sidebottom {
          display: none;
        }
        .nav button {
          justify-content: center;
        }
        .nav .ico {
          font-size: 18px;
        }
        .stats {
          grid-template-columns: repeat(2, 1fr);
        }
        .two {
          grid-template-columns: 1fr;
        }
        .content {
          padding: 23px 18px;
        }
        .topbar {
          padding: 0 18px;
        }
        .formgrid.four-cols {
          grid-template-columns: repeat(2, minmax(0, 1fr));
        }
      }
      @media (max-width: 560px) {
        .sidebar {
          width: 55px;
        }
        .stats {
          gap: 9px;
        }
        .card {
          padding: 13px;
        }
        .stat-value {
          font-size: 19px;
        }
        .pagehead {
          display: block;
        }
        .pagehead .actions {
          margin-top: 14px;
        }
        .formgrid,
        .formgrid.four-cols,
        .reportgrid {
          grid-template-columns: 1fr;
        }
        .topbar {
          height: 58px;
        }
        .search-input {
          max-width: 100%;
        }
      }
    </style>
  </head>
  <body>
    <div class="app">
      <aside class="sidebar">
        <div class="brand">
          <div class="brandmark">🥐</div>
          <div><strong>RotiRapi</strong><small>Bakery management</small></div>
        </div>
        <div>
          <div class="navlabel">MENU UTAMA</div>
          <nav class="nav" id="nav">
            <button class="active" data-page="dashboard">
              <span class="ico">▦</span><span>Dashboard</span>
            </button>
            <button data-page="products">
              <span class="ico">▤</span><span>Data Produk</span>
            </button>
            <button data-page="campuses">
              <span class="ico">⌂</span><span>Data Kampus</span>
            </button>
            <button data-page="deliveries">
              <span class="ico">⇧</span><span>Setoran</span>
            </button>
            <button data-page="returns">
              <span class="ico">↩</span><span>Retur Mingguan</span>
            </button>
            <button data-page="payments">
              <span class="ico">↗</span><span>Pembayaran</span>
            </button>
            <button data-page="expenses">
              <span class="ico">▣</span><span>Pengeluaran</span>
            </button>
            <button data-page="recap">
              <span class="ico">📊</span><span>Rekap Bulanan</span>
            </button>
            <button data-page="reports">
              <span class="ico">▥</span><span>Laporan Laba</span>
            </button>
          </nav>
        </div>
        <div class="sidebottom">MULTI-DEVICE SUPPORT<br /></div>
      </aside>
      <main class="main">
        <header class="topbar">
          <div class="crumb">Workspace / <b id="crumb">Dashboard</b></div>
          <div class="user">
            <div class="avatar">A</div>
            <div>
              <b>Admin</b><br /><span style="color: #8993a0"
                >Sistem Lokal & Cloud</span
              >
            </div>
          </div>
        </header>
        <div class="content" id="content"></div>
        <div class="footer">ROTI RAPI · Sistem distribusi bakery</div>
      </main>
    </div>

    <!-- Modal Utama Form -->
    <div class="modalback" id="modalback">
      <div class="modal">
        <div class="modalhead">
          <h2 id="modalTitle">Tambah data</h2>
          <button class="close" onclick="closeModal()">✕</button>
        </div>
        <div id="modalBody"></div>
        <div class="modalfoot">
          <button
            class="btn"
            style="border-color: #e8ebf0"
            onclick="closeModal()"
          >
            Batal</button
          ><button class="btn primary" id="saveBtn">Simpan</button>
        </div>
      </div>
    </div>

    <!-- FITUR BARU UX: Modal Konfirmasi Custom -->
    <div class="modalback" id="confirmModal">
      <div
        class="modal"
        style="width: 380px; text-align: center; padding: 30px"
      >
        <div style="font-size: 36px; margin-bottom: 10px">⚠️</div>
        <h3 id="confirmMsg" style="margin-top: 0; font-size: 18px">
          Konfirmasi
        </h3>
        <p style="color: var(--muted); font-size: 13px; margin-bottom: 24px">
          Tindakan ini tidak dapat dibatalkan.
        </p>
        <div class="modalfoot" style="justify-content: center">
          <button
            class="btn"
            style="border-color: #e8ebf0"
            onclick="closeConfirmModal()"
          >
            Batal
          </button>
          <button class="btn danger" onclick="executeConfirm()">
            Ya, Lanjutkan
          </button>
        </div>
      </div>
    </div>

    <div id="toast"></div>

    <script>
      const money = (n) =>
        "Rp" + Math.round(Number(n) || 0).toLocaleString("id-ID");
      const today = () => new Date().toISOString().slice(0, 10);
      const addDays = (days) => {
        let d = new Date();
        d.setDate(d.getDate() + days);
        return d.toISOString().slice(0, 10);
      };

      let db = {
        products: [],
        campuses: [],
        deliveries: [],
        returns: [],
        payments: [],
        expenses: [],
      };
      let current = "dashboard";

      // --- UX: Toast Alert Lanjutan ---
      function showToast(msg, duration = 3000, type = "info") {
        let toast = document.getElementById("toast");
        toast.className = type === "error" ? "error" : "";
        toast.innerHTML = msg;
        toast.style.display = "block";
        setTimeout(() => (toast.style.opacity = "1"), 10);
        if (duration > 0)
          setTimeout(() => {
            toast.style.opacity = "0";
            setTimeout(() => (toast.style.display = "none"), 300);
          }, duration);
      }

      // --- UX: Confirm Modal Custom ---
      let confirmCallback = null;
      function openConfirmModal(msg, callback) {
        document.getElementById("confirmMsg").textContent = msg;
        confirmCallback = callback;
        document.getElementById("confirmModal").classList.add("show");
      }
      function closeConfirmModal() {
        document.getElementById("confirmModal").classList.remove("show");
      }
      function executeConfirm() {
        if (confirmCallback) confirmCallback();
        closeConfirmModal();
      }

      // --- UX: Fitur Pencarian Tabel (Search Bar) ---
      function searchBarHTML() {
        return `<div class="search-bar-container"><input type="text" class="search-input" placeholder="🔍 Cari data dalam tabel..." onkeyup="filterTable(this)"></div>`;
      }
      function filterTable(input) {
        let val = input.value.toLowerCase();
        let rows =
          input.parentElement.nextElementSibling.querySelectorAll("tbody tr");
        rows.forEach((row) => {
          row.style.display = row.innerText.toLowerCase().includes(val)
            ? ""
            : "none";
        });
      }

      // --- SINKRONISASI KONFLIK (PATCH/DELTA SYNC) ---
      let syncQueue = [];
      let syncTimeout = null;

      function pushSync(table, action, data) {
        syncQueue.push({ table, action, data });
        // Simpan sementara di local untuk backup
        localStorage.setItem("rotirapi_db", JSON.stringify(db));

        clearTimeout(syncTimeout);
        syncTimeout = setTimeout(triggerSync, 2000); // Debounce 2 detik
      }

      function triggerSync() {
        if (syncQueue.length === 0) return;
        if (typeof google === "undefined" || !google.script) {
          showToast("✅ Disimpan ke memori lokal (Offline)", 2500);
          return;
        }

        let payload = [...syncQueue];
        syncQueue = []; // kosongkan antrian
        showToast("⏳ Menyinkronkan ke Cloud...", 0);

        google.script.run
          .withSuccessHandler(() =>
            showToast("✅ Sinkronisasi Berhasil!", 2500),
          )
          .withFailureHandler(() => {
            syncQueue = payload.concat(syncQueue); // Kembalikan ke antrian jika gagal
            showToast(
              "❌ Gagal Sinkron. Akan dicoba lagi nanti.",
              4000,
              "error",
            );
          })
          .syncDeltas(payload);
      }

      // Initial Load
      document.getElementById("content").innerHTML =
        '<div class="empty"><h3>Memuat sistem...</h3></div>';
      if (typeof google !== "undefined" && google.script) {
        google.script.run
          .withSuccessHandler(function (serverDataStr) {
            if (serverDataStr) db = JSON.parse(serverDataStr);
            render();
            startAutoSync();
          })
          .withFailureHandler(() => {
            document.getElementById("content").innerHTML =
              '<div class="empty" style="color:var(--red)"><h3>❌ Gagal Terhubung</h3><p>Periksa koneksi internet Anda.</p></div>';
          })
          .getDatabase();
      } else {
        let localData = localStorage.getItem("rotirapi_db");
        if (localData) db = JSON.parse(localData);
        render();
        showToast("✓ Mode Offline Aktif", 3000);
      }

      function startAutoSync() {
        if (typeof google === "undefined" || !google.script) return;
        setInterval(() => {
          if (
            !document.getElementById("modalback").classList.contains("show") &&
            syncQueue.length === 0
          ) {
            google.script.run
              .withSuccessHandler(function (serverDataStr) {
                if (serverDataStr) {
                  let serverData = JSON.parse(serverDataStr);
                  if (JSON.stringify(db) !== JSON.stringify(serverData)) {
                    db = serverData;
                    render();
                    showToast("🔄 Data baru dimuat", 3000);
                  }
                }
              })
              .getDatabase();
          }
        }, 15000); // Tarik data tiap 15 detik jika tidak ada aktivitas push
      }

      const prod = (id) => {
        let p = db.products && db.products.find((x) => x.id == id);
        return p ? p.name : "Produk dihapus";
      };
      const campus = (id) => {
        let c = db.campuses && db.campuses.find((x) => x.id == id);
        return c ? c.name : "Kampus dihapus";
      };

      const deliveryValue = (d) => {
        return d.items.reduce((s, i) => {
          let r = db.returns.filter(
            (x) => x.deliveryId == d.id && x.productId == i.productId,
          );
          let rem = r.reduce((sum, x) => sum + Number(x.remaining), 0);
          let bad = r.reduce((sum, x) => sum + Number(x.damaged), 0);
          let sold = Math.max(0, Number(i.qty) - rem - bad);
          return s + sold * Number(i.price);
        }, 0);
      };

      function calc() {
        let gross = 0,
          sold = 0,
          damaged = 0,
          stock = 0,
          total_cost = 0;
        db.deliveries.forEach((d) => {
          d.items.forEach((i) => {
            let r = db.returns.filter(
              (x) => x.deliveryId == d.id && x.productId == i.productId,
            );
            let rem = r.reduce((s, x) => s + Number(x.remaining), 0);
            let bad = r.reduce((s, x) => s + Number(x.damaged), 0);
            let q = Math.max(0, Number(i.qty) - rem - bad);
            sold += q;
            damaged += bad;
            stock += rem;
            gross += q * Number(i.price);

            // PERBAIKAN: HPP/Biaya Produksi dihitung dari TOTAL yang disetor/diproduksi
            total_cost += Number(i.qty) * Number(i.cost);
          });
        });
        let paid = db.payments.reduce((s, x) => s + Number(x.amount), 0);
        let expenses = db.expenses.reduce((s, x) => s + Number(x.amount), 0);

        return {
          gross,
          sold,
          damaged,
          stock,
          cogs: total_cost,
          paid,
          expenses,
          profit: gross - total_cost - expenses,
          receivable: Math.max(0, gross - paid),
        };
      }

      function pageHead(kicker, title, sub, action = "") {
        return `<div class="pagehead"><div><div class="eyebrow">${kicker}</div><h1>${title}</h1><p class="sub">${sub}</p></div>${action ? `<div class="actions">${action}</div>` : ""}</div>`;
      }
      function btn(label, fn, cls = "") {
        return `<button class="btn ${cls}" onclick="${fn}">${label}</button>`;
      }
      function stat(label, value, icon, foot = "Ringkasan data tercatat") {
        return `<div class="card"><div class="stat-top"><span>${label}</span><span class="stat-icon">${icon}</span></div><div class="stat-value">${value}</div><div class="stat-foot">${foot}</div></div>`;
      }

      function checkStatus(d) {
        if (!d.items || d.items.length === 0) return "Aktif";
        let allChecked = true;
        d.items.forEach((i) => {
          let r = db.returns.find(
            (x) => x.deliveryId == d.id && x.productId == i.productId,
          );
          if (!r) allChecked = false;
        });
        return allChecked ? "Selesai" : "Aktif";
      }

      function deliveryTable(rows, customHeight = "") {
        let heightStyle = customHeight
          ? ` style="max-height:${customHeight};"`
          : "";
        return `<div class="tablewrap scrollable"${heightStyle}><table>
          <thead>
            <tr><th>Tgl & Kampus</th><th>Rincian Terjual</th><th>Tagihan</th><th>Dibayar</th><th>Status</th></tr>
          </thead>
          <tbody>
            ${
              rows
                .map((d) => {
                  let tagihan = deliveryValue(d);
                  let terbayar = db.payments
                    .filter((p) => p.deliveryId == d.id)
                    .reduce((s, x) => s + Number(x.amount), 0);
                  let kurang = tagihan - terbayar;
                  let returStatus = checkStatus(d);

                  let payBadge = "";
                  if (tagihan > 0 && kurang <= 1)
                    payBadge = `<span class="pill" style="background:#e0f2f1;color:#00796b">Lunas</span>`;
                  else if (tagihan <= 0 && returStatus === "Selesai")
                    payBadge = `<span class="pill" style="background:#f1f3f4;color:#444">Lunas (Nihil)</span>`;
                  else if (terbayar > 0)
                    payBadge = `<span class="pill" style="background:#fff3e0;color:#e65100">Nyicil</span>`;
                  else
                    payBadge = `<span class="pill" style="background:#ffebee;color:#c62828">Belum Bayar</span>`;

                  // FITUR BARU: Kadaluwarsa
                  let expWarning = "";
                  if (d.expDate && returStatus !== "Selesai") {
                    let exp = new Date(d.expDate),
                      now = new Date();
                    let diffDays = Math.ceil(
                      (exp - now) / (1000 * 60 * 60 * 24),
                    );
                    if (diffDays < 0)
                      expWarning = `<span class="pill" style="background:#ffebee;color:#c62828; margin-top:5px">Kadaluwarsa!</span>`;
                    else if (diffDays <= 1)
                      expWarning = `<span class="pill" style="background:#fff3e0;color:#e65100; margin-top:5px">Hampir Exp (${diffDays} hr)</span>`;
                    else
                      expWarning = `<span style="display:inline-block; font-size:10px; color:var(--muted); margin-top:4px">Exp: ${d.expDate}</span>`;
                  }

                  let detail = d.items
                    .map((i) => {
                      let r = db.returns.filter(
                        (x) =>
                          x.deliveryId == d.id && x.productId == i.productId,
                      );
                      let sold = Math.max(
                        0,
                        Number(i.qty) -
                          r.reduce((s, x) => s + Number(x.remaining), 0) -
                          r.reduce((s, x) => s + Number(x.damaged), 0),
                      );
                      return `${prod(i.productId)}: <b>${sold}</b>/${i.qty}`;
                    })
                    .join("<br>");

                  return `<tr>
                <td>${d.date}<br><b>${campus(d.campusId)}</b><br><small>#${d.id}</small><br>${expWarning}</td>
                <td style="line-height:1.4">${detail}</td>
                <td><b>${money(tagihan)}</b></td>
                <td>
                  <span style="color:#276653; font-weight:600">${money(terbayar)}</span><br>
                  <small style="color:${kurang > 0 ? "var(--red)" : "var(--muted)"}">${kurang > 0 ? "- " + money(kurang) : "Tidak ada sisa"}</small>
                </td>
                <td>
                  <div style="display:flex; flex-direction:column; gap:4px; align-items:flex-start">
                    ${returStatus === "Selesai" ? `<span class="pill" style="background:#f1f3f4;color:#444">Retur Selesai</span>` : `<span class="pill" style="background:#fff3e0;color:#e65100">Retur Aktif</span>`}
                    ${payBadge}
                  </div>
                </td>
              </tr>`;
                })
                .join("") ||
              '<tr><td colspan="5" class="empty">Belum ada setoran.</td></tr>'
            }
          </tbody>
        </table></div>`;
      }

      function dashboard() {
        let c = calc();
        let campTotals = db.campuses.map((cp) => {
          let deliveries = db.deliveries.filter((d) => d.campusId == cp.id);
          let billed = deliveries.reduce((s, d) => s + deliveryValue(d), 0);
          let paid = db.payments
            .filter((p) => p.campusId == cp.id)
            .reduce((s, p) => s + Number(p.amount), 0);
          return { name: cp.name, billed: billed, paid: paid };
        });

        return (
          pageHead(
            "OVERVIEW",
            "Dashboard",
            "Pantau performa.",
            btn("＋ Buat setoran", "openDelivery()", "primary"),
          ) +
          `<div class="grid stats">
            ${stat("Omzet Penjualan", money(c.gross), "↗")}
            ${stat("Produk terjual", c.sold + " pcs", "▤")}
            ${stat("Estimasi Laba", money(c.profit), "💰", "Laba bersih saat ini")}
            ${stat("Uang Diterima", money(c.paid), "◈")}
          </div>
          <div class="grid two">
            <div class="card">
              <div class="section-title"><h3>Tagihan Kampus (Terjual)</h3><span>Status Pembayaran</span></div>
              ${
                campTotals
                  .map((x) => {
                    let pct =
                      x.billed > 0
                        ? Math.min(100, (x.paid / x.billed) * 100)
                        : 0;
                    let isLunas = x.paid >= x.billed && x.billed > 0;
                    let barColor = isLunas ? "#76a58d" : "#e99b4b";
                    return `<div class="campusrow"><div class="name">${x.name}</div><div class="track"><div class="fill" style="width:${pct}%; background:${barColor}"></div></div><div class="amount"><div style="font-size:12px; font-weight:700; color:${barColor}">${money(x.paid)}</div><div style="font-size:9px; color:var(--muted)">Tagihan: ${money(x.billed)}</div></div></div>`;
                  })
                  .join("") || '<div class="empty">Belum ada data.</div>'
              }
            </div>
            <div class="card">
              <div class="section-title"><h3>Ringkasan</h3><span>Semua periode</span></div>
              <div class="campusrow"><div class="name">Produk rusak</div><div class="amount">${c.damaged} pcs</div></div>
              <div class="campusrow"><div class="name">Total Sisa Stok</div><div class="amount">${c.stock} pcs</div></div>
              <div class="campusrow"><div class="name">Total Piutang</div><div class="amount" style="color:var(--red); font-size:14px; font-weight:700">${money(c.receivable)}</div></div>
            </div>
          </div>
          <div class="section-title" style="margin-top:22px">
            <h3>Aktivitas Setoran Terkini</h3><span style="cursor:pointer; color:var(--brand); font-weight:600; font-size:11px;" onclick="go('deliveries')">Lihat Semua ➔</span>
          </div>
          ${deliveryTable(
            db.deliveries
              .slice()
              .sort((a, b) => b.id - a.id)
              .slice(0, 15),
            "280px",
          )}`
        );
      }

      function products() {
        return (
          pageHead(
            "MASTER",
            "Data Produk",
            "",
            btn("＋ Tambah produk", "openProduct()", "primary"),
          ) +
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>SKU</th><th>Nama</th><th>Harga Jual</th><th>HPP (Modal)</th><th>Aksi</th></tr></thead><tbody>${db.products.map((p) => `<tr><td>${p.sku}</td><td><b>${p.name}</b></td><td>${money(p.price)}</td><td>${money(p.cost)}</td><td>${btn("Edit", `editProduct(${p.id})`)} ${btn("Hapus", `removeItem('products',${p.id})`, "danger")}</td></tr>`).join("") || '<tr><td colspan="5" class="empty">Kosong</td></tr>'}</tbody></table></div>`
        );
      }
      function campuses() {
        return (
          pageHead(
            "MASTER",
            "Data Kampus",
            "",
            btn("＋ Tambah kampus", "openCampus()", "primary"),
          ) +
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>Kampus</th><th>Kontak</th><th>Telepon</th><th>Aksi</th></tr></thead><tbody>${db.campuses.map((p) => `<tr><td><b>${p.name}</b></td><td>${p.contact || "-"}</td><td>${p.phone || "-"}</td><td>${btn("Edit", `editCampus(${p.id})`)} ${btn("Hapus", `removeItem('campuses',${p.id})`, "danger")}</td></tr>`).join("") || '<tr><td colspan="4" class="empty">Kosong</td></tr>'}</tbody></table></div>`
        );
      }
      function deliveries() {
        return (
          pageHead(
            "DISTRIBUSI",
            "Data Setoran",
            "",
            btn("＋ Buat setoran", "openDelivery()", "primary"),
          ) +
          searchBarHTML() +
          deliveryTable(db.deliveries.slice().sort((a, b) => b.id - a.id))
        );
      }

      function returnsPage() {
        let campusOpts =
          `<option value="all">Semua Kampus</option>` +
          db.campuses
            .map((c) => `<option value="${c.id}">${c.name}</option>`)
            .join("");
        let header = pageHead(
          "STOK",
          "Retur Mingguan",
          "Update sisa dan rusak untuk perhitungan produk laku.",
          btn("＋ Catat Sisa/Rusak", "openReturn()", "primary"),
        );
        let filters = `<div class="card" style="margin-bottom: 20px;"><div class="formgrid">${selectField("Filter Kampus", "filterReturnCampus", campusOpts)}${field("Filter Tanggal Cek", "filterReturnDate", "date", "")}</div></div>`;

        setTimeout(() => {
          ["filterReturnCampus", "filterReturnDate"].forEach((id) => {
            document
              .getElementById(id)
              .addEventListener("change", updateReturnTable);
          });
          updateReturnTable();
        }, 50);
        return header + filters + `<div id="returnTableContainer"></div>`;
      }

      function updateReturnTable() {
        let cId = val("filterReturnCampus"),
          dateVal = val("filterReturnDate");
        let filteredReturns = db.returns
          .filter((r) => {
            let d = db.deliveries.find((x) => x.id == r.deliveryId);
            if (cId !== "all" && d && d.campusId != cId) return false;
            if (dateVal && r.date !== dateVal) return false;
            return true;
          })
          .sort((a, b) => b.id - a.id);

        let rows = filteredReturns
          .map((r) => {
            let d = db.deliveries.find((x) => x.id == r.deliveryId),
              item = d ? d.items.find((x) => x.productId == r.productId) : null;
            let sold = item
              ? Math.max(
                  0,
                  Number(item.qty) - Number(r.remaining) - Number(r.damaged),
                )
              : 0;
            return `<tr>
              <td>${r.date}</td><td><b>${d ? campus(d.campusId) : "-"}</b><br><small style="color:var(--muted)">Setoran #${r.deliveryId}</small></td>
              <td><b>${prod(r.productId)}</b></td>
              <td><div style="display:flex; gap:6px; flex-wrap:wrap"><span class="pill" style="background:#fff3e0;color:#e65100">${r.remaining} Sisa</span><span class="pill" style="background:#ffebee;color:#c62828">${r.damaged} Rusak</span><span class="pill" style="background:#e0f2f1;color:#00796b">${sold} Laku</span></div></td>
              <td>${btn("Edit", `openReturn(${r.deliveryId})`)} ${btn("Hapus", `removeItem('returns',${r.id})`, "danger")}</td>
            </tr>`;
          })
          .join("");
        document.getElementById("returnTableContainer").innerHTML =
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>Tanggal Cek</th><th>Faktur & Kampus</th><th>Produk</th><th>Status Produk</th><th>Aksi</th></tr></thead><tbody>${rows || '<tr><td colspan="5" class="empty">Tidak ada data retur yang sesuai filter.</td></tr>'}</tbody></table></div>`;
      }

      function payments() {
        return (
          pageHead(
            "KEUANGAN",
            "Pembayaran",
            "Riwayat pembayaran dan sisa tagihan per setoran.",
            btn("＋ Catat bayar", "openPayment()", "primary"),
          ) +
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>Tanggal</th><th>Setoran Kampus</th><th>Total Tagihan</th><th>Dibayar (Riwayat Ini)</th><th>Status & Sisa Kurang</th><th>Catatan</th><th>Aksi</th></tr></thead><tbody>${
            db.payments
              .map((p) => {
                let d = db.deliveries.find((x) => x.id == p.deliveryId);
                let tagihan = d ? deliveryValue(d) : 0;
                let terbayarTotal = db.payments
                  .filter((x) => x.deliveryId == p.deliveryId)
                  .reduce((s, x) => s + Number(x.amount), 0);
                let kurang = Math.max(0, tagihan - terbayarTotal);

                return `<tr><td>${p.date}</td><td><b>${campus(p.campusId)}</b><br><small style="color:var(--muted)">Ref Setoran: #${p.deliveryId || "-"}</small></td><td>${money(tagihan)}</td><td><b style="color:var(--brand); font-size:14px;">${money(p.amount)}</b></td>
              <td>${kurang <= 1 ? `<span class="pill" style="background:#e0f2f1;color:#00796b">LUNAS</span>` : `<b style="color:var(--red)">Sisa: ${money(kurang)}</b><br><small style="color:var(--muted)">Total masuk: ${money(terbayarTotal)}</small>`}</td>
              <td>${p.note || "-"}</td><td>${btn("Hapus", `removeItem('payments',${p.id})`, "danger")}</td></tr>`;
              })
              .join("") || '<tr><td colspan="7" class="empty">Kosong</td></tr>'
          }</tbody></table></div>`
        );
      }

      function expenses() {
        return (
          pageHead(
            "KEUANGAN",
            "Pengeluaran",
            "",
            btn("＋ Tambah biaya", "openExpense()", "primary"),
          ) +
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>Tanggal</th><th>Kategori</th><th>Nominal</th><th>Keterangan</th><th>Aksi</th></tr></thead><tbody>${db.expenses.map((p) => `<tr><td>${p.date}</td><td>${p.category}</td><td><b>${money(p.amount)}</b></td><td>${p.note || "-"}</td><td>${btn("Hapus", `removeItem('expenses',${p.id})`, "danger")}</td></tr>`).join("") || '<tr><td colspan="5" class="empty">Kosong</td></tr>'}</tbody></table></div>`
        );
      }

      function reports() {
        let c = calc();

        // FITUR BARU: Analisis Laba/Margin per Produk
        let prodStats = db.products
          .map((p) => {
            let delivered = 0,
              sold = 0,
              remain = 0,
              bad = 0;
            db.deliveries.forEach((d) => {
              let item = d.items.find((i) => i.productId == p.id);
              if (item) {
                delivered += Number(item.qty);
                let rets = db.returns.filter(
                  (x) => x.deliveryId == d.id && x.productId == p.id,
                );
                let r = rets.reduce((s, x) => s + Number(x.remaining), 0);
                let b = rets.reduce((s, x) => s + Number(x.damaged), 0);
                remain += r;
                bad += b;
                sold += Math.max(0, Number(item.qty) - r - b);
              }
            });
            let revenue = sold * p.price;
            let cogs = delivered * p.cost; // Modal dari total yang diproduksi (dikirim)
            let profit = revenue - cogs;
            let margin =
              revenue > 0 ? ((profit / revenue) * 100).toFixed(1) : 0;
            return {
              name: p.name,
              delivered,
              sold,
              remain,
              bad,
              revenue,
              cogs,
              profit,
              margin,
            };
          })
          .sort((a, b) => b.profit - a.profit);

        let prodTable = `<div class="section-title" style="margin-top:25px"><h3>Analisis Laba per Produk</h3><span>Berdasarkan total produksi vs terjual</span></div>
        ${searchBarHTML()}
        <div class="tablewrap scrollable"><table>
          <thead><tr><th>Produk</th><th>Produksi (Disetor)</th><th>Terjual</th><th>Sisa & Rusak</th><th>HPP Total (Modal)</th><th>Omzet (Kotor)</th><th>Laba Bersih</th><th>Margin</th></tr></thead>
          <tbody>
            ${prodStats
              .map(
                (x) => `<tr>
              <td><b>${x.name}</b></td>
              <td style="text-align:center">${x.delivered}</td>
              <td style="text-align:center"><b style="color:var(--brand)">${x.sold}</b></td>
              <td style="text-align:center">${x.remain} S / ${x.bad} R</td>
              <td>${money(x.cogs)}</td>
              <td>${money(x.revenue)}</td>
              <td><b style="color:${x.profit >= 0 ? "var(--brand)" : "var(--red)"}">${money(x.profit)}</b></td>
              <td><span class="pill" style="background:${x.margin >= 30 ? "#edf5f0" : x.margin > 0 ? "#fff3e0" : "#ffebee"}; color:${x.margin >= 30 ? "var(--brand)" : x.margin > 0 ? "var(--orange)" : "var(--red)"}">${x.margin}%</span></td>
            </tr>`,
              )
              .join("")}
          </tbody>
        </table></div>`;

        return (
          pageHead(
            "ANALISIS",
            "Laporan Keuangan",
            "",
            btn("⇩ Ekspor CSV", "exportAll()", "primary"),
          ) +
          `<div class="grid reportgrid">${[
            ["Omzet Penjualan", money(c.gross)],
            ["HPP Total Produksi", money(c.cogs)],
            ["Laba Kotor", money(c.gross - c.cogs)],
            ["Pengeluaran (Operasional)", money(c.expenses)],
            ["Estimasi Laba Bersih", money(c.profit)],
          ]
            .map(
              (x) =>
                `<div class="reportbox"><small>${x[0]}</small><strong>${x[1]}</strong></div>`,
            )
            .join("")}</div>` +
          prodTable
        );
      }

      function recap() {
        let years = [
          ...new Set(db.deliveries.map((d) => d.date.substring(0, 4))),
        ].sort((a, b) => b - a);
        if (years.length === 0) years = [new Date().getFullYear().toString()];
        let yOpts =
          `<option value="all">Semua Tahun</option>` +
          years
            .map(
              (y) =>
                `<option value="${y}" ${y == new Date().getFullYear() ? "selected" : ""}>${y}</option>`,
            )
            .join("");
        let mOpts =
          `<option value="all">Semua Bulan</option>` +
          [
            "Januari",
            "Februari",
            "Maret",
            "April",
            "Mei",
            "Juni",
            "Juli",
            "Agustus",
            "September",
            "Oktober",
            "November",
            "Desember",
          ]
            .map(
              (m, i) =>
                `<option value="${(i + 1).toString().padStart(2, "0")}" ${i + 1 === new Date().getMonth() + 1 ? "selected" : ""}>${m}</option>`,
            )
            .join("");

        let html =
          pageHead(
            "STATISTIK",
            "Rekap Bulanan",
            "Filter penjualan untuk memprediksi setoran bulan depan.",
          ) +
          `<div class="card" style="margin-bottom: 20px;"><div class="formgrid four-cols">
            ${selectField("Tahun", "filterYear", yOpts)} ${selectField("Bulan", "filterMonth", mOpts)}
            ${selectField("Kampus", "filterCampus", `<option value="all">Semua Kampus</option>` + db.campuses.map((c) => `<option value="${c.id}">${c.name}</option>`).join(""))}
            ${selectField("Produk", "filterProduct", `<option value="all">Semua Produk</option>` + db.products.map((p) => `<option value="${p.id}">${p.name}</option>`).join(""))}
        </div></div><div id="recapTableContainer"></div>`;

        setTimeout(() => {
          [
            "filterYear",
            "filterMonth",
            "filterCampus",
            "filterProduct",
          ].forEach((id) => {
            document
              .getElementById(id)
              .addEventListener("change", updateRecapTable);
          });
          updateRecapTable();
        }, 50);
        return html;
      }

      function updateRecapTable() {
        let y = val("filterYear"),
          m = val("filterMonth"),
          c = val("filterCampus"),
          p = val("filterProduct"),
          results = {};
        db.deliveries.forEach((d) => {
          let dYear = d.date.substring(0, 4),
            dMonth = d.date.substring(5, 7);
          if (
            (y !== "all" && dYear !== y) ||
            (m !== "all" && dMonth !== m) ||
            (c !== "all" && d.campusId != c)
          )
            return;
          d.items.forEach((item) => {
            if (p !== "all" && item.productId != p) return;
            let key = d.campusId + "_" + item.productId;
            if (!results[key])
              results[key] = {
                campusId: d.campusId,
                productId: item.productId,
                delivered: 0,
                sold: 0,
                remain: 0,
                bad: 0,
              };
            results[key].delivered += Number(item.qty);
            let rets = db.returns.filter(
              (x) => x.deliveryId == d.id && x.productId == item.productId,
            );
            results[key].remain += rets.reduce(
              (s, x) => s + Number(x.remaining),
              0,
            );
            results[key].bad += rets.reduce((s, x) => s + Number(x.damaged), 0);
          });
        });

        let rows = Object.values(results)
          .map((r) => {
            r.sold = Math.max(0, r.delivered - r.remain - r.bad);
            let rate =
              r.delivered > 0 ? Math.round((r.sold / r.delivered) * 100) : 0;
            let rekomen =
              rate >= 90
                ? "Tingkatkan Qty ⬆️"
                : rate <= 60
                  ? "Kurangi Qty ⬇️"
                  : "Pertahankan (Normal)";
            let col =
              rate >= 90
                ? "var(--brand)"
                : rate <= 60
                  ? "var(--red)"
                  : "var(--orange)";
            let bgCol =
              rate >= 90 ? "#edf5f0" : rate <= 60 ? "#ffebee" : "#fff3e0";
            return `<tr><td><b>${campus(r.campusId)}</b></td><td>${prod(r.productId)}</td>
              <td style="text-align:center">${r.delivered} pcs</td><td style="text-align:center"><b>${r.sold} pcs</b></td>
              <td style="text-align:center"><span style="color:var(--orange)">${r.remain} Sisa</span> / <span style="color:var(--red)">${r.bad} Rusak</span></td>
              <td style="text-align:center"><span class="pill" style="background:${bgCol}; color:${col}; font-size:11px;">${rate}% Laku</span></td>
              <td style="color:${col}; font-weight:700;">${rekomen}</td></tr>`;
          })
          .join("");
        document.getElementById("recapTableContainer").innerHTML =
          searchBarHTML() +
          `<div class="tablewrap scrollable"><table><thead><tr><th>Kampus</th><th>Produk</th><th style="text-align:center">Disetor</th><th style="text-align:center">Terjual</th><th style="text-align:center">Rincian</th><th style="text-align:center">Persentase</th><th>Rekomendasi Setoran</th></tr></thead><tbody>${rows || '<tr><td colspan="7" class="empty">Tidak ada data.</td></tr>'}</tbody></table></div>`;
      }

      const pages = {
        dashboard,
        products,
        campuses,
        deliveries,
        returns: returnsPage,
        payments,
        expenses,
        reports,
        recap,
      };
      const titles = {
        dashboard: "Dashboard",
        products: "Data Produk",
        campuses: "Kampus",
        deliveries: "Setoran",
        returns: "Retur",
        payments: "Pembayaran",
        expenses: "Pengeluaran",
        reports: "Laporan",
        recap: "Rekap Bulanan",
      };
      function render() {
        document.getElementById("crumb").textContent = titles[current];
        document
          .querySelectorAll("#nav button")
          .forEach((b) =>
            b.classList.toggle("active", b.dataset.page === current),
          );
        document.getElementById("content").innerHTML = pages[current]();
      }
      function go(p) {
        current = p;
        render();
      }
      document.getElementById("nav").addEventListener("click", (e) => {
        let b = e.target.closest("button[data-page]");
        if (b) go(b.dataset.page);
      });
      function openModal(title, body, save) {
        document.getElementById("modalTitle").textContent = title;
        document.getElementById("modalBody").innerHTML = body;
        document.getElementById("saveBtn").onclick = save;
        document.getElementById("modalback").classList.add("show");
      }
      function closeModal() {
        document.getElementById("modalback").classList.remove("show");
      }
      function val(id) {
        return document.getElementById(id).value;
      }
      function field(label, id, type = "text", value = "", extra = "") {
        return `<div class="field"><label>${label}</label><input id="${id}" type="${type}" value="${value}" ${extra}></div>`;
      }
      function selectField(label, id, opts) {
        return `<div class="field"><label>${label}</label><select id="${id}">${opts}</select></div>`;
      }

      function openProduct(p) {
        p = p || {};
        openModal(
          p.id ? "Edit" : "Tambah produk",
          `<div class="formgrid">${field("Nama", "pname", "text", p.name || "")}${field("SKU", "psku", "text", p.sku || "")}${field("Harga Jual", "pprice", "number", p.price || "")}${field("HPP (Modal Produksi)", "pcost", "number", p.cost || "")}</div>`,
          () => {
            let o = {
              id: p.id || Date.now(),
              name: val("pname").trim(),
              sku: val("psku").trim(),
              price: +val("pprice"),
              cost: +val("pcost"),
            };
            if (!o.name || !o.sku || o.price < 0 || o.cost < 0)
              return showToast("⚠️ Harap lengkapi semua data.", 3000, "error");
            let i = db.products.findIndex((x) => x.id == o.id);
            i < 0 ? db.products.push(o) : (db.products[i] = o);
            closeModal();
            render();
            pushSync("products", "UPSERT", o);
          },
        );
      }
      function editProduct(id) {
        openProduct(db.products.find((x) => x.id == id));
      }

      function openCampus(p) {
        p = p || {};
        openModal(
          p.id ? "Edit" : "Tambah kampus",
          `<div class="formgrid">${field("Nama", "cname", "text", p.name || "")}${field("Kontak", "ccontact", "text", p.contact || "")}${field("Telepon", "cphone", "text", p.phone || "")}</div>`,
          () => {
            let o = {
              id: p.id || Date.now(),
              name: val("cname").trim(),
              contact: val("ccontact"),
              phone: val("cphone"),
            };
            if (!o.name)
              return showToast("⚠️ Nama kampus wajib diisi.", 3000, "error");
            let i = db.campuses.findIndex((x) => x.id == o.id);
            i < 0 ? db.campuses.push(o) : (db.campuses[i] = o);
            closeModal();
            render();
            pushSync("campuses", "UPSERT", o);
          },
        );
      }
      function editCampus(id) {
        openCampus(db.campuses.find((x) => x.id == id));
      }

      function openDelivery() {
        if (!db.products.length || !db.campuses.length)
          return showToast(
            "⚠️ Tambah produk & kampus terlebih dahulu.",
            4000,
            "error",
          );
        let rows = db.products
          .map(
            (p) =>
              `<div class="formgrid" style="margin:8px 0;padding:9px;background:#f8faf9;border-radius:8px"><div class="field"><label>${p.name} · ${money(p.price)}</label><input type="number" min="0" id="qty_${p.id}" value="0"></div><div class="field"><label>Harga jual</label><input type="number" id="price_${p.id}" value="${p.price}"></div></div>`,
          )
          .join("");

        openModal(
          "Buat setoran",
          `<div class="formgrid">${field("Tanggal Setor", "ddate", "date", today())}${selectField("Kampus", "dcampus", db.campuses.map((c) => `<option value="${c.id}">${c.name}</option>`).join(""))}</div><div class="formgrid" style="margin-top:10px">${field("Tanggal Kadaluwarsa", "dexp", "date", addDays(3))}</div><br>${rows}`,
          () => {
            let items = db.products
              .map((p) => ({
                productId: p.id,
                qty: +val("qty_" + p.id),
                price: +val("price_" + p.id),
                cost: p.cost,
              }))
              .filter((x) => x.qty > 0);
            if (!items.length)
              return showToast(
                "⚠️ Setidaknya isi QTY pada satu produk.",
                4000,
                "error",
              );
            let deliv = {
              id: Date.now(),
              date: val("ddate"),
              expDate: val("dexp"),
              campusId: +val("dcampus"),
              items,
              status: "Aktif",
            };
            db.deliveries.push(deliv);
            closeModal();
            render();
            pushSync("deliveries", "UPSERT", deliv);
          },
        );
      }

      function openReturn(deliveryIdStr = null) {
        if (!db.deliveries.length)
          return showToast("⚠️ Belum ada setoran yang dibuat.", 3000, "error");
        let filteredDeliveries = db.deliveries
          .slice()
          .sort((a, b) => b.id - a.id)
          .filter((d) => checkStatus(d) !== "Selesai" || deliveryIdStr == d.id);
        if (filteredDeliveries.length === 0)
          return showToast(
            "✅ Semua setoran yang ada sudah diselesaikan retur-nya.",
            4000,
          );

        let opts = filteredDeliveries
          .map(
            (d) =>
              `<option value="${d.id}" ${deliveryIdStr == d.id ? "selected" : ""}>#${d.id} · ${campus(d.campusId)} · ${d.date}</option>`,
          )
          .join("");

        openModal(
          "Catat Sisa & Rusak",
          `<div class="formgrid">${field("Tanggal Pengecekan", "rdate", "date", today())}${selectField("Pilih Setoran Kampus", "rdelivery", opts)}</div><div id="rItems" style="margin-top:15px; max-height: 400px; overflow-y: auto;"></div>`,
          () => {
            let d = db.deliveries.find((x) => x.id == val("rdelivery"));
            if (!d) return;
            let dateVal = val("rdate"),
              hasError = false;

            d.items.forEach((item) => {
              let r = +val("rem_" + item.productId) || 0,
                b = +val("bad_" + item.productId) || 0;
              if (r + b > Number(item.qty)) {
                showToast(
                  `⚠️ Total sisa + rusak <b>${prod(item.productId)}</b> lebih besar dari jumlah dikirim.`,
                  4000,
                  "error",
                );
                hasError = true;
              }
            });

            if (hasError) return;

            d.items.forEach((item) => {
              let r = {
                id:
                  Date.now() + item.productId + Math.floor(Math.random() * 100),
                date: dateVal,
                deliveryId: d.id,
                productId: item.productId,
                remaining: +val("rem_" + item.productId) || 0,
                damaged: +val("bad_" + item.productId) || 0,
              };
              let dup = db.returns.findIndex(
                (x) =>
                  x.deliveryId == r.deliveryId && x.productId == r.productId,
              );
              if (dup >= 0) {
                Object.assign(db.returns[dup], r);
                pushSync("returns", "UPSERT", db.returns[dup]);
              } else {
                db.returns.push(r);
                pushSync("returns", "UPSERT", r);
              }
            });
            closeModal();
            render();
          },
        );
        let updateItems = () => {
          let d = db.deliveries.find((x) => x.id == val("rdelivery"));
          if (!d) {
            document.getElementById("rItems").innerHTML = "";
            return;
          }
          document.getElementById("rItems").innerHTML =
            `<div class="hint">Isi sisa dan rusak. Sistem menghitung: <b>Terjual = Disetor - Sisa - Rusak</b>.</div>` +
            d.items
              .map((item) => {
                let ex = db.returns.find(
                  (x) => x.deliveryId == d.id && x.productId == item.productId,
                ) || { remaining: 0, damaged: 0 };
                return `<div class="card" style="margin-bottom:10px; padding:12px; background:#fafbfc; border-color:#e8ebf0;"><div style="font-weight:600; margin-bottom:8px; font-size:12px; color:var(--brand)">${prod(item.productId)} <span style="color:var(--muted); font-weight:normal;">(Disetor: ${item.qty} pcs)</span></div><div class="formgrid">${field("Sisa (pcs)", "rem_" + item.productId, "number", ex.remaining, 'min="0"')}${field("Rusak (pcs)", "bad_" + item.productId, "number", ex.damaged, 'min="0"')}</div></div>`;
              })
              .join("");
        };
        document.getElementById("rdelivery").onchange = updateItems;
        updateItems();
      }

      function openPayment() {
        let filteredDeliveries = db.deliveries
          .slice()
          .sort((a, b) => b.id - a.id)
          .filter((d) => {
            let tagihan = deliveryValue(d);
            let terbayar = db.payments
              .filter((x) => x.deliveryId == d.id)
              .reduce((s, x) => s + Number(x.amount), 0);
            return checkStatus(d) === "Selesai" && tagihan - terbayar > 1;
          });

        if (filteredDeliveries.length === 0) {
          openModal(
            "Pemberitahuan",
            `<div class="empty" style="padding: 30px 10px;"><div style="font-size:30px; margin-bottom:10px;">✅</div><h3 style="color:var(--brand); margin:0 0 5px 0;">Tidak Ada Tagihan!</h3><p style="margin:0;">Semua setoran yang sudah diretur telah lunas,<br>atau <b>setoran baru belum diretur</b> (selesaikan retur agar muncul di sini).</p></div>`,
            closeModal,
          );
          document.getElementById("saveBtn").textContent = "Tutup";
          return;
        }

        document.getElementById("saveBtn").textContent = "Simpan";
        let opts = filteredDeliveries
          .map((d) => {
            let tagihan = deliveryValue(d);
            let terbayar = db.payments
              .filter((x) => x.deliveryId == d.id)
              .reduce((s, x) => s + Number(x.amount), 0);
            let kurang = Math.max(0, tagihan - terbayar);
            return `<option value="${d.id}" data-campus="${d.campusId}" data-sisa="${kurang}">#${d.id} · ${campus(d.campusId)} (Sisa: ${money(kurang)})</option>`;
          })
          .join("");

        openModal(
          "Catat Cicilan / Pelunasan",
          `<div class="formgrid" style="grid-template-columns: 1fr;">${selectField("Pilih Kode Setoran (Faktur)", "paydelivery", opts)}</div><div class="formgrid" style="margin-top:13px">${field("Tanggal Bayar", "paydate", "date", today())}${field("Nominal Bayar Rp", "payamount", "number", "")}</div><div class="formgrid" style="margin-top:13px; grid-template-columns: 1fr;">${field("Catatan", "paynote", "text", "Pelunasan / Cicilan")}</div>`,
          () => {
            let delivSelect = document.getElementById("paydelivery");
            let dId = +delivSelect.value;
            let cId =
              +delivSelect.options[delivSelect.selectedIndex].getAttribute(
                "data-campus",
              );
            let p = {
              id: Date.now(),
              date: val("paydate"),
              deliveryId: dId,
              campusId: cId,
              amount: +val("payamount"),
              note: val("paynote"),
            };

            if (p.amount <= 0)
              return showToast("⚠️ Nominal harus lebih dari 0.", 3000, "error");
            db.payments.push(p);
            closeModal();
            render();
            pushSync("payments", "UPSERT", p);
          },
        );

        let selectEl = document.getElementById("paydelivery"),
          amountEl = document.getElementById("payamount");
        let updateAmount = () => {
          if (selectEl.selectedIndex >= 0) {
            amountEl.value =
              selectEl.options[selectEl.selectedIndex].getAttribute(
                "data-sisa",
              );
          }
        };
        selectEl.addEventListener("change", updateAmount);
        setTimeout(updateAmount, 50);
      }

      function openExpense() {
        openModal(
          "Tambah pengeluaran",
          `<div class="formgrid">${field("Tanggal", "edate", "date", today())}${selectField("Kategori", "ecat", ["Bahan baku", "Operasional Kurir", "Gaji", "Lainnya"].map((x) => `<option>${x}</option>`).join(""))}${field("Nominal Rp", "eamount", "number", "")}${field("Keterangan", "enote", "text", "")}</div>`,
          () => {
            let p = {
              id: Date.now(),
              date: val("edate"),
              category: val("ecat"),
              amount: +val("eamount"),
              note: val("enote"),
            };
            if (p.amount <= 0)
              return showToast("⚠️ Nominal harus lebih dari 0.", 3000, "error");
            db.expenses.push(p);
            closeModal();
            render();
            pushSync("expenses", "UPSERT", p);
          },
        );
      }

      function removeItem(key, id) {
        openConfirmModal(
          "Apakah Anda yakin ingin menghapus baris data ini?",
          () => {
            db[key] = db[key].filter((x) => x.id != id);
            render();
            pushSync(key, "DELETE", { id: id });
          },
        );
      }

      // --- CSV EXPORT ---
      function csv(rows, filename) {
        let text = rows
          .map((r) =>
            r
              .map(
                (x) =>
                  '"' + String(x != null ? x : "").replace(/"/g, '""') + '"',
              )
              .join(";"),
          )
          .join("\n");
        let blob = new Blob(["\ufeff" + text], {
            type: "text/csv;charset=utf-8;",
          }),
          a = document.createElement("a");
        a.href = URL.createObjectURL(blob);
        a.download = filename + ".csv";
        a.click();
        URL.revokeObjectURL(a.href);
      }
      function exportCSV(key) {
        let rows;
        if (key === "products")
          rows = [
            ["SKU", "Produk", "Harga Jual", "Modal"],
            ...db.products.map((x) => [x.sku, x.name, x.price, x.cost]),
          ];
        if (key === "deliveries")
          rows = [
            [
              "ID",
              "Tanggal",
              "Tgl Kadaluwarsa",
              "Kampus",
              "Produk",
              "Qty",
              "Harga",
              "Total",
            ],
            ...db.deliveries.flatMap((d) =>
              d.items.map((i) => [
                d.id,
                d.date,
                d.expDate,
                campus(d.campusId),
                prod(i.productId),
                i.qty,
                i.price,
                i.qty * i.price,
              ]),
            ),
          ];
        if (key === "returns")
          rows = [
            ["Tanggal", "ID Setoran", "Kampus", "Produk", "Sisa", "Rusak"],
            ...db.returns.map((r) => {
              let d = db.deliveries.find((d) => d.id == r.deliveryId);
              return [
                r.date,
                r.deliveryId,
                campus(d ? d.campusId : null),
                prod(r.productId),
                r.remaining,
                r.damaged,
              ];
            }),
          ];
        if (key === "payments")
          rows = [
            ["Tanggal", "Setoran Ref", "Kampus", "Nominal", "Catatan"],
            ...db.payments.map((p) => [
              p.date,
              p.deliveryId || "-",
              campus(p.campusId),
              p.amount,
              p.note,
            ]),
          ];
        if (key === "expenses")
          rows = [
            ["Tanggal", "Kategori", "Nominal", "Keterangan"],
            ...db.expenses.map((p) => [p.date, p.category, p.amount, p.note]),
          ];
        if (rows) csv(rows, "rotirapi_" + key);
      }
      function exportAll() {
        ["products", "deliveries", "returns", "payments", "expenses"].forEach(
          (k, i) => setTimeout(() => exportCSV(k), i * 350),
        );
      }
    </script>
  </body>
</html>
