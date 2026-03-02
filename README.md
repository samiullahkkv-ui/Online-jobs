<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>APK PRO · premium jobs & apps</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Poppins:wght@600;700&display=swap" rel="stylesheet">
    
    <!-- AdSense Auto Ads -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-9654539721896304" crossorigin="anonymous"></script>

    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body {
            font-family: "Inter", sans-serif;
            background: linear-gradient(145deg, #0d0b1a 0%, #1a1435 100%);
            min-height: 100vh;
            color: #f1ecff;
            padding: 10px 12px 40px;
            overflow-x: hidden;
        }
        .glass-wrapper { max-width: 900px; margin: 0 auto; position: relative; z-index: 1; }

        /* Header */
        .premium-header {
            background: linear-gradient(135deg, rgba(128, 90, 213, 0.95) 0%, rgba(79, 70, 229, 0.95) 100%);
            border: 1px solid rgba(255, 255, 255, 0.25);
            border-radius: 35px;
            padding: 22px 15px;
            margin-bottom: 20px;
            text-align: center;
            cursor: pointer;
            box-shadow: 0 15px 40px rgba(0,0,0,0.6);
            transition: transform 0.3s ease;
        }
        .premium-header:hover { transform: scale(1.03); }
        .premium-header h1 { font-family: 'Poppins', sans-serif; font-size: 2.4rem; font-weight: 700; color: white; }
        .premium-header p { font-size: 0.9rem; opacity: 0.95; margin-top: 5px; }

        /* Navigation */
        .nav-pills { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-bottom: 30px; }
        .nav-pills button {
            padding: 12px 22px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.15);
            background: rgba(35, 30, 55, 0.85); color: #cdc6f0; cursor: pointer; font-weight: 600; font-size: 0.9rem;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .nav-pills button.active, .nav-pills button:hover {
            background: linear-gradient(145deg, #9f7aea, #667eea);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.5);
        }

        /* Secret Login */
        #secret-login { 
            display: none; background: rgba(255, 255, 255, 0.08); 
            padding: 20px; border-radius: 25px; margin-bottom: 25px; 
            text-align: center; border: 1px dashed rgba(255, 255, 255, 0.3);
            animation: popIn 0.5s ease;
        }
        #secret-login input { 
            padding: 14px 18px; border-radius: 30px; border: none; width: 80%; 
            margin-bottom: 12px; outline: none; background: #fff; color: #333; font-size: 1rem;
        }
        #secret-login button { 
            background: #2fcb7c; color: white; border: none; padding: 12px 30px; 
            border-radius: 30px; font-weight: bold; cursor: pointer; transition: 0.3s;
        }
        #secret-login button:active { transform: scale(0.95); }

        /* Grid & Cards with Animation */
        .cards-grid { 
            display: grid; grid-template-columns: 1fr; gap: 22px; 
        }
        @media (min-width: 600px) { .cards-grid { grid-template-columns: 1fr 1fr; } }
        
        .post-card { 
            background: rgba(30, 25, 48, 0.85); 
            border-radius: 28px; overflow: hidden; 
            border: 1px solid rgba(255, 255, 255, 0.08);
            display: flex; flex-direction: column;
            opacity: 0;
            transform: translateY(40px);
            animation: fadeInUp 0.7s forwards;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .post-card:hover {
            transform: translateY(-12px) scale(1.03);
            box-shadow: 0 20px 40px rgba(0,0,0,0.6);
        }
        .card-img { 
            width: 100%; height: 190px; object-fit: cover; 
            background: #231f35; transition: transform 0.5s ease;
        }
        .post-card:hover .card-img { transform: scale(1.08); }
        
        .card-content { padding: 20px; flex: 1; display: flex; flex-direction: column; }
        .category-tag { 
            font-size: 0.7rem; background: linear-gradient(90deg, #6d4faa, #9f7aea); 
            padding: 5px 14px; border-radius: 20px; margin-bottom: 12px; 
            display: inline-block; text-transform: uppercase; font-weight: bold;
        }
        .card-title { font-size: 1.15rem; margin-bottom: 18px; font-weight: 600; line-height: 1.3; }
        
        .action-btn { 
            background: linear-gradient(145deg, #8b6de0, #5f4bcb); 
            padding: 14px; border-radius: 22px; color: white; text-align: center; 
            text-decoration: none; font-weight: 700; margin-top: auto; 
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s ease;
        }
        .action-btn:active { transform: scale(0.95); }

        /* Admin Panel */
        #admin-panel { 
            display: none; background: #161226; border-radius: 28px; 
            padding: 25px; margin-top: 35px; border: 2px solid #2fcb7c;
            animation: popIn 0.6s ease;
        }
        .admin-form input, .admin-form select { 
            width: 100%; padding: 16px; margin-bottom: 15px; border-radius: 16px; 
            border: 1px solid #444; background: #0d0b1a; color: white; font-size: 1rem;
        }
        .save-btn { 
            background: #2fcb7c; color: white; padding: 16px; border: none; 
            width: 100%; border-radius: 16px; font-weight: 700; cursor: pointer;
            font-size: 1.1rem; transition: 0.3s;
        }
        .save-btn:active { transform: scale(0.96); }

        /* Toast */
        #toast {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            background: #2fcb7c; color: white; padding: 16px 28px; border-radius: 30px;
            box-shadow: 0 15px 35px rgba(47, 203, 124, 0.4);
            z-index: 9999; font-weight: 700; display: none; align-items: center; gap: 10px;
            animation: toastPop 0.4s ease;
        }

        /* Animations */
        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes popIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
        @keyframes toastPop {
            0% { transform: translateX(-50%) translateY(30px); opacity: 0; }
            100% { transform: translateX(-50%) translateY(0); opacity: 1; }
        }

        .ad-slot { margin: 20px 0; min-height: 110px; background: rgba(255,255,255,0.05); border-radius: 20px; }
    </style>
</head>
<body>

<div class="glass-wrapper">
    <header class="premium-header" id="mainHeader">
        <h1>APK PRO</h1>
        <p>premium jobs · apps · websites</p>
    </header>

    <div class="nav-pills" id="category-nav">
        <button class="active" data-cat="All">All</button>
        <button data-cat="Job">Jobs</button>
        <button data-cat="App">Apps</button>
        <button data-cat="Website">Websites</button>
        <button data-cat="APK PRO">APK PRO</button>
    </div>

    <div id="secret-login">
        <p style="margin-bottom: 12px; font-size: 0.85rem; color: #cdc6f0;">Subscribe for VIP Updates</p>
        <input type="text" id="fakeEmail" placeholder="Enter your email...">
        <button id="submitSecret">Submit</button>
    </div>

    <div class="ad-slot">
        <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-9654539721896304" data-ad-slot="2571500310" data-ad-format="auto" data-full-width-responsive="true"></ins>
    </div>

    <div id="posts-display" class="cards-grid"></div>

    <div id="admin-panel">
        <h3 style="margin-bottom: 20px; color: #2fcb7c; text-align: center;">⚡ Admin Control Panel</h3>
        <div class="admin-form">
            <input type="text" id="postTitle" placeholder="Enter Title">
            <select id="postCategory">
                <option value="Job">Job</option>
                <option value="App">App</option>
                <option value="Website">Website</option>
                <option value="APK PRO">APK PRO</option>
            </select>
            <input type="text" id="postImage" placeholder="Image URL">
            <input type="text" id="postLink" placeholder="Destination Link">
            <button class="save-btn" id="savePostBtn">📢 PUBLISH POST</button>
            <button onclick="location.reload()" style="background:none; color:#888; border:none; margin-top:20px; width:100%; cursor:pointer; font-size: 0.85rem;">Logout Admin</button>
        </div>
    </div>
</div>

<!-- Toast -->
<div id="toast"></div>

<script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
    import { getFirestore, collection, addDoc, onSnapshot, deleteDoc, doc } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";
    import { getAuth, signInAnonymously, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";

    // 🔥 YOUR REAL FIREBASE CONFIG (tumhara diya hua)
    const firebaseConfig = {
      apiKey: "AIzaSyDpoRdrVoEwn9p3RjuhcnUc6esivlpbTDI",
      authDomain: "jobs-248da.firebaseapp.com",
      databaseURL: "https://jobs-248da-default-rtdb.firebaseio.com",
      projectId: "jobs-248da",
      storageBucket: "jobs-248da.firebasestorage.app",
      messagingSenderId: "516203193248",
      appId: "1:516203193248:web:575763e3f075c158cafac5"
    };

    const appId = "apkpro";   // Data isme save hoga (change kar sakte ho)

    const app = initializeApp(firebaseConfig);
    const db = getFirestore(app);
    const auth = getAuth(app);

    let posts = [];
    let isAdmin = false;
    let currentFilter = 'All';

    const initApp = async () => {
        try {
            await signInAnonymously(auth);
            onAuthStateChanged(auth, (user) => { if (user) loadData(); });
        } catch (e) { console.error("Auth Error", e); }
    };

    const loadData = () => {
        const q = collection(db, 'artifacts', appId, 'public', 'data', 'posts');
        onSnapshot(q, (snapshot) => {
            posts = snapshot.docs.map(d => ({ id: d.id, ...d.data() }));
            posts.sort((a, b) => b.createdAt - a.createdAt);
            render();
        });
    };

    const render = () => {
        const display = document.getElementById('posts-display');
        const filtered = currentFilter === 'All' ? posts : posts.filter(p => p.category === currentFilter);
        
        display.innerHTML = filtered.length ? '' : '<div style="grid-column:1/-1; text-align:center; padding:60px; opacity:0.5; font-size:1.1rem;">No posts found yet 😕</div>';
        
        filtered.forEach((post, index) => {
            const card = document.createElement('div');
            card.className = 'post-card';
            card.style.animationDelay = `${index * 80}ms`;
            card.innerHTML = `
                <img src="${post.image}" class="card-img" onerror="this.src='https://via.placeholder.com/400x200/1a1435/ffffff?text=APK+PRO'">
                <div class="card-content">
                    <span class="category-tag">${post.category}</span>
                    <div class="card-title">${post.title}</div>
                    <a href="\( {post.link}" target="_blank" class="action-btn"> \){post.category === 'Job' ? 'Apply Now' : 'Get Details'}</a>
                    \( {isAdmin ? `<button class="del-btn" data-id=" \){post.id}" style="margin-top:12px; color:#ff4d4d; background:none; border:1px solid #ff4d4d; padding:6px 12px; border-radius:12px; cursor:pointer;">🗑 Delete</button>` : ''}
                </div>
            `;
            display.appendChild(card);
        });

        // Delete buttons
        document.querySelectorAll('.del-btn').forEach(btn => {
            btn.onclick = async () => {
                if(confirm("Delete this post?")) {
                    await deleteDoc(doc(db, 'artifacts', appId, 'public', 'data', 'posts', btn.dataset.id));
                }
            };
        });
    };

    // Toast Function
    const showToast = (message, color = "#2fcb7c") => {
        const toast = document.getElementById('toast');
        toast.textContent = message;
        toast.style.background = color;
        toast.style.display = "flex";
        setTimeout(() => { toast.style.display = "none"; }, 2800);
    };

    // Event Listeners
    document.getElementById('mainHeader').onclick = () => {
        document.getElementById('secret-login').style.display = 'block';
    };

    document.getElementById('submitSecret').onclick = () => {
        const val = document.getElementById('fakeEmail').value.trim();
        if(val === "sami21") {
            isAdmin = true;
            document.getElementById('secret-login').style.display = 'none';
            document.getElementById('admin-panel').style.display = 'block';
            render();
            window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
            showToast("✅ Admin Mode Activated");
        } else {
            showToast("Thanks for subscribing! ✅");
            document.getElementById('secret-login').style.display = 'none';
        }
    };

    document.querySelectorAll('#category-nav button').forEach(btn => {
        btn.onclick = () => {
            document.querySelectorAll('#category-nav button').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
            currentFilter = btn.dataset.cat;
            render();
        };
    });

    document.getElementById('savePostBtn').onclick = async () => {
        const title = document.getElementById('postTitle').value.trim();
        const category = document.getElementById('postCategory').value;
        const image = document.getElementById('postImage').value.trim();
        const link = document.getElementById('postLink').value.trim();

        if(!title || !image || !link) return showToast("All fields are required!", "#ff4d4d");

        try {
            await addDoc(collection(db, 'artifacts', appId, 'public', 'data', 'posts'), {
                title, category, image, link, createdAt: Date.now()
            });
            showToast("✅ Post Published Successfully!");
            document.getElementById('admin-panel').style.display = 'none';
            document.getElementById('postTitle').value = '';
            document.getElementById('postImage').value = '';
            document.getElementById('postLink').value = '';
        } catch(e) { 
            showToast("Error: " + e.message, "#ff4d4d"); 
        }
    };

    // Initialize
    initApp();

    // AdSense push
    setTimeout(() => {
        try { (adsbygoogle = window.adsbygoogle || []).push({}); } catch(e){}
    }, 1200);
</script>

</body>
</html>
