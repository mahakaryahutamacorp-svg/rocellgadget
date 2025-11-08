<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Rocell Gadget | Katalog Handphone (Admin)</title>
  <meta name="description" content="Rocell Gadget - Katalog. Admin bisa tambah, edit, hapus produk (disimpan di browser)." />
  <link rel="icon" href="rocell_gadget_logo.png" />

  <!-- CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous" />
  <link href="https://cdn.datatables.net/v/bs5/dt-2.1.7/r-3.0.3/datatables.min.css" rel="stylesheet" />
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet" />
  <style>
    :root{--bg:#0d1117;--card:#0f1524;--muted:#91a5c6;--accent:#2563eb}
    body{background:var(--bg);color:#e6edf3;font-family:Inter,system-ui,Segoe UI,Roboto,'Helvetica Neue',Arial}
    .navbar,.modal-content{background:#161b22}
    .card{background:var(--card);border:1px solid #23375a}
    .form-control,.form-select{background:#0b1220;color:#e6edf3;border-color:#23375a}
    .btn-primary{background:var(--accent);border-color:var(--accent)}
    .wa-btn{position:fixed;right:18px;bottom:18px;z-index:9999;border-radius:999px;padding:12px 14px;box-shadow:0 6px 18px rgba(0,0,0,.35)}
    .logo-container{text-align:center;margin-top:10px;margin-bottom:10px}
    .logo-container img{max-width:160px;border-radius:10px}
    @media (max-width:576px){.brand-filter-grid{grid-template-columns:repeat(2,1fr)}}
    .admin-badge{background:#1b7a2f;padding:.25rem .5rem;border-radius:.4rem;color:#fff}
    .dt-fallback { color: #cfe3ff; }
  </style>
</head>
<body>
  <div class="container py-3">
    <div class="logo-container">
      <img src="rocell_gadget_logo.png" alt="Rocell Gadget Logo" onerror="this.style.display='none'" />
    </div>

    <nav class="navbar navbar-expand-lg border-bottom border-dark sticky-top py-2 mb-3">
      <div class="container-fluid px-0">
        <div class="d-flex align-items-center gap-2">
          <button class="btn btn-outline-light" id="btnToggleView"><i class="bi bi-list"></i> Terbuka</button>
          <input id="searchInput" class="form-control ms-2" style="min-width:260px;max-width:420px" type="search" placeholder="Cari Nama Barang…" autocomplete="off" />
        </div>

        <div class="ms-auto d-flex align-items-center gap-2">
          <span id="adminStatus"></span>
          <button id="btnLogin" class="btn btn-outline-light">Login</button>
          <button id="btnLogout" class="btn btn-danger d-none">Logout</button>
          <button id="btnTambahTop" class="btn btn-primary d-none"><i class="bi bi-plus-lg"></i> Tambah</button>
        </div>
      </div>
    </nav>

    <div class="card p-3">
      <div class="table-responsive">
        <table id="tblBarang" class="table table-hover align-middle w-100 dt-fallback" aria-live="polite">
          <thead>
            <tr>
              <th>Gambar</th>
              <th>Barang</th>
              <th>Stok</th>
              <th>Harga</th>
              <th class="text-center">Aksi</th>
            </tr>
          </thead>
          <tbody></tbody>
        </table>
      </div>
    </div>

    <div class="mt-3 small text-muted">Catatan: Semua perubahan tersimpan di browser (localStorage). Hanya admin yang login bisa melakukan CRUD.</div>

  </div>

  <!-- Modals -->
  <div class="modal fade" id="modalLogin" tabindex="-1">
    <div class="modal-dialog modal-sm modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Login Admin</h5>
          <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <div class="mb-2">Password:</div>
          <input id="loginPassword" type="password" class="form-control" />
          <div class="form-text mt-2">Password default: <code>rocelladmin</code></div>
          <div id="loginError" class="text-danger mt-2 d-none"></div>
        </div>
        <div class="modal-footer">
          <button class="btn btn-outline-light" data-bs-dismiss="modal">Batal</button>
          <button id="btnDoLogin" class="btn btn-primary">Masuk</button>
        </div>
      </div>
    </div>
  </div>

  <div class="modal fade" id="modalItem" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="modalItemTitle">Tambah Produk</h5>
          <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <div class="mb-2"><label class="form-label">Nama</label><input id="mNama" class="form-control" /></div>
          <div class="mb-2"><label class="form-label">Brand</label><input id="mBrand" class="form-control" /></div>
          <div class="mb-2 row g-2"><div class="col-6"><label class="form-label">Stok</label><input id="mStok" type="number" class="form-control" value="1" min="0" /></div><div class="col-6"><label class="form-label">Harga (Rp)</label><input id="mHarga" type="number" class="form-control" value="0" min="0" /></div></div>
          <div class="mb-2"><label class="form-label">URL Gambar (opsional)</label><input id="mGambar" class="form-control" placeholder="https://...jpg" /></div>
          <input type="hidden" id="mId" />
        </div>
        <div class="modal-footer">
          <button class="btn btn-outline-light" data-bs-dismiss="modal">Batal</button>
          <button id="btnSaveItem" class="btn btn-primary">Simpan</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Scripts -->
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://cdn.datatables.net/v/bs5/dt-2.1.7/r-3.0.3/datatables.min.js"></script>

  <script>
    // Defensive wrapper - avoid uncaught script errors
    (function(){
      'use strict';

      const STORAGE_KEY = 'rocell_items_v1';
      const ADMIN_FLAG = 'rocell_admin_logged';
      const ADMIN_PASSWORD = 'rocelladmin'; // change later if needed

      // sample test cases (initial seed) - acts as test cases
      const SAMPLE = [
        { id:'t1', nama:'Ipad Mini 2 4G 16GB', brand:'Apple', stok:1, harga:400000, gambar:'' },
        { id:'t2', nama:'Samsung Note 5 4/32', brand:'Samsung', stok:1, harga:200000, gambar:'' },
        { id:'t3', nama:'Oppo A37 2/16', brand:'Oppo', stok:10, harga:0, gambar:'' }
      ];

      // helpers
      const $ = window.jQuery;
      const el = id => document.getElementById(id);

      function loadItems(){
        try{
          const raw = localStorage.getItem(STORAGE_KEY);
          if(!raw) { localStorage.setItem(STORAGE_KEY, JSON.stringify(SAMPLE)); return SAMPLE.slice(); }
          return JSON.parse(raw);
        }catch(e){ console.error('loadItems', e); return SAMPLE.slice(); }
      }
      function saveItems(arr){ try{ localStorage.setItem(STORAGE_KEY, JSON.stringify(arr)); }catch(e){ console.error('saveItems', e); } }

      let items = loadItems();
      let dataTable = null;

      // Render rows (DataTables-safe)
      function renderRows(data){
        const tbody = document.querySelector('#tblBarang tbody');
        tbody.innerHTML = '';
        data.forEach(it => {
          const tr = document.createElement('tr');
          tr.dataset.id = it.id;
          tr.innerHTML = `
            <td style="width:90px"><img src="${escapeHtml(it.gambar||'')}" alt="" style="max-width:80px;max-height:60px;object-fit:cover;border-radius:6px" onerror="this.src='';this.style.display='none'" /></td>
            <td><strong>${escapeHtml(it.nama)}</strong><div class="small text-muted">${escapeHtml(it.brand)}</div></td>
            <td>${Number(it.stok)||0} unit</td>
            <td>${Number(it.harga)>0 ? 'Rp ' + new Intl.NumberFormat('id-ID').format(Number(it.harga)) : '<span class="text-secondary">Hubungi</span>'}</td>
            <td class="text-center">
              <div class="btn-group btn-group-sm" role="group">
                <button class="btn btn-outline-light btn-edit">Edit</button>
                <button class="btn btn-outline-danger btn-delete">Hapus</button>
              </div>
            </td>
          `;
          tbody.appendChild(tr);
        });

        // re-init DataTable if present
        try{
          if(window.jQuery && $.fn && $.fn.dataTable){
            if($.fn.dataTable.isDataTable('#tblBarang')){
              $('#tblBarang').DataTable().destroy();
            }
            dataTable = $('#tblBarang').DataTable({
              responsive:true, paging:true, pageLength:10, ordering:true, info:true, autoWidth:false,
              language:{ searchPlaceholder:'Cari…', lengthMenu:'Tampil _MENU_', zeroRecords:'Tidak ada data', info:'_START_–_END_ dari _TOTAL_ barang' }
            });
          }
        }catch(e){ console.warn('DataTable init skipped', e); }
      }

      // basic XSS escape for inserted text
      function escapeHtml(s){ if(!s) return ''; return String(s).replace(/[&"'<>]/g, function(c){ return {'&':'&amp;','"':'&quot;',"'":'&#39;','<':'&lt;','>':'&gt;'}[c]; }); }

      // CRUD operations
      function addItem(obj){ items.unshift(obj); saveItems(items); renderRows(items); }
      function updateItem(id, obj){ const idx = items.findIndex(x=>x.id===id); if(idx>-1){ items[idx] = obj; saveItems(items); renderRows(items); } }
      function deleteItem(id){ items = items.filter(x=>x.id!==id); saveItems(items); renderRows(items); }

      // UI helpers
      function setAdminMode(on){ try{
        if(on){ localStorage.setItem(ADMIN_FLAG, '1'); el('adminStatus').innerHTML = '<span class="admin-badge">ADMIN</span>'; el('btnLogin').classList.add('d-none'); el('btnLogout').classList.remove('d-none'); el('btnTambahTop').classList.remove('d-none'); document.querySelectorAll('.btn-edit,.btn-delete').forEach(b=>b.classList.remove('d-none'));
        } else { localStorage.removeItem(ADMIN_FLAG); el('adminStatus').innerHTML = ''; el('btnLogin').classList.remove('d-none'); el('btnLogout').classList.add('d-none'); el('btnTambahTop').classList.add('d-none'); document.querySelectorAll('.btn-edit,.btn-delete').forEach(b=>b.classList.add('d-none')); }
      }catch(e){ console.error('setAdminMode', e); } }

      function isAdmin(){ return localStorage.getItem(ADMIN_FLAG) === '1'; }

      // Event wiring (delegated)
      function attachEvents(){
        // Login flow
        try{
          const loginModal = new bootstrap.Modal('#modalLogin');
          el('btnLogin').addEventListener('click', ()=>{ el('loginPassword').value=''; el('loginError').classList.add('d-none'); loginModal.show(); });
          el('btnDoLogin').addEventListener('click', ()=>{
            const pw = el('loginPassword').value || '';
            if(pw === ADMIN_PASSWORD){ setAdminMode(true); loginModal.hide(); } else { el('loginError').textContent = 'Password salah'; el('loginError').classList.remove('d-none'); }
          });
          el('btnLogout').addEventListener('click', ()=>{ setAdminMode(false); });
        }catch(e){ console.error('login events', e); }

        // Add top button
        try{ el('btnTambahTop').addEventListener('click', ()=>{ openItemModal(); }); }catch(e){ console.error('add top', e); }

        // Table actions (delegation)
        document.querySelector('#tblBarang tbody').addEventListener('click', function(ev){
          const tr = ev.target.closest('tr'); if(!tr) return;
          const id = tr.dataset.id;
          if(ev.target.closest('.btn-edit')){ if(!isAdmin()){ alert('Hanya admin yang bisa mengedit'); return; } const it = items.find(x=>x.id===id); openItemModal(it); }
          if(ev.target.closest('.btn-delete')){ if(!isAdmin()){ alert('Hanya admin yang bisa menghapus'); return; } if(confirm('Hapus item ini?')) deleteItem(id); }
        });

        // Save item modal
        try{
          const itemModal = new bootstrap.Modal('#modalItem');
          el('btnSaveItem').addEventListener('click', ()=>{
            const id = el('mId').value || 'id'+Math.random().toString(36).slice(2,9);
            const obj = { id, nama: el('mNama').value.trim(), brand: el('mBrand').value.trim(), stok: Number(el('mStok').value)||0, harga: Number(el('mHarga').value)||0, gambar: el('mGambar').value.trim() };
            if(!obj.nama){ alert('Nama wajib diisi'); return; }
            const existing = items.find(x=>x.id===id);
            if(existing) updateItem(id, obj); else addItem(obj);
            itemModal.hide();
          });
        }catch(e){ console.error('save item', e); }

        // Search input behavior
        try{
          el('searchInput').addEventListener('input', function(){ const q = this.value.trim().toLowerCase(); const filtered = items.filter(i => (i.nama+' '+i.brand).toLowerCase().includes(q)); renderRows(filtered); });
        }catch(e){ console.error('search event', e); }

        // Toggle view (compact / full)
        try{ el('btnToggleView').addEventListener('click', function(){ const txt = this.textContent.trim(); if(txt==='Terbuka'){ this.innerHTML = '<i class="bi bi-list"></i> Compact'; document.querySelectorAll('.logo-container,img').forEach(i=>i.style.display='none'); } else { this.innerHTML = '<i class="bi bi-list"></i> Terbuka'; document.querySelectorAll('.logo-container,img').forEach(i=>i.style.display='block'); } }); }catch(e){ console.error('toggle view', e); }

        // Test helpers (developer only) - add sample test, clear storage
        try{
          window.__rocell_test_addSample = function(){ SAMPLE.forEach(s => addItem(Object.assign({}, s, { id:'t'+Math.random().toString(36).slice(2,8) }))); alert('Sample items added'); };
          window.__rocell_test_clear = function(){ if(confirm('Clear semua data?')){ localStorage.removeItem(STORAGE_KEY); items = []; renderRows(items); } };
        }catch(e){ console.warn('test helpers', e); }
      }

      function openItemModal(item){ try{
        const modal = new bootstrap.Modal('#modalItem');
        if(item){ el('modalItemTitle').textContent = 'Edit Produk'; el('mId').value = item.id; el('mNama').value = item.nama; el('mBrand').value = item.brand; el('mStok').value = item.stok; el('mHarga').value = item.harga; el('mGambar').value = item.gambar || ''; }
        else { el('modalItemTitle').textContent = 'Tambah Produk'; el('mId').value=''; el('mNama').value=''; el('mBrand').value=''; el('mStok').value=1; el('mHarga').value=0; el('mGambar').value=''; }
        modal.show();
      }catch(e){ console.error('openItemModal', e); }

      // boot
      function boot(){ try{
        renderRows(items);
        attachEvents();
        // set admin UI based on stored flag
        setAdminMode(isAdmin());
        console.log('Rocell Gadget ready');
      }catch(e){ console.error('boot error', e); }
      }

      if(document.readyState === 'loading') document.addEventListener('DOMContentLoaded', boot); else boot();

    })();
  </script>
</body>
</html>
