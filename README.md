
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#ec4899" />
  <title>일일수련회 모바일 초대장</title>

  <style>
    :root{
      --bg:#2b0f1c;
      --card:#3b1226;
      --card2:#4a1730;
      --text:#fff1f7;
      --muted:#f9a8d4;
      --line:rgba(255,255,255,.18);

      --brand:#ec4899;   /* 메인 핑크 */
      --brand2:#f472b6;  /* 서브 핑크 */
      --danger:#fb7185;

      --shadow:0 14px 40px rgba(236,72,153,.35);
      --radius:18px;
      --radius2:14px;
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      color:var(--text);
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Apple SD Gothic Neo", "Noto Sans KR", Arial, "Helvetica Neue", sans-serif;
      line-height:1.45;
      -webkit-font-smoothing: antialiased;
      padding: 22px 14px 80px;

      background:
        radial-gradient(1200px 700px at 20% -10%, rgba(236,72,153,.35), transparent 60%),
        radial-gradient(1200px 700px at 90% 10%, rgba(244,114,182,.25), transparent 55%),
        linear-gradient(180deg, var(--bg), #14060d 85%);
    }

    a{color:inherit}
    .wrap{max-width: 520px; margin:0 auto}

    .hero{
      position: relative;
      background: linear-gradient(135deg, rgba(236,72,153,.20), rgba(244,114,182,.12));
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 18px 18px 18px;
      box-shadow: var(--shadow);
      overflow:hidden;
    }

    .poster{
      width:100%;
      border-radius:20px;
      margin-bottom:16px;
      box-shadow: 0 16px 40px rgba(236,72,153,.35);
      background:#ffe4ea;
      display:block;
    }

    .badge{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding: 7px 11px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,.20);
      background: rgba(59,18,38,.55);
      color: var(--muted);
      font-size: 12.5px;
    }
    .badge .dot{
      width:8px; height:8px; border-radius:50%;
      background: var(--brand);
      box-shadow: 0 0 0 4px rgba(236,72,153,.18);
    }

    h1{
      margin: 12px 0 8px;
      font-size: 26px;
      letter-spacing:-.02em;
    }
    .subtitle{
      margin:0 0 14px;
      color: rgba(255,241,247,.80);
      font-size: 14px;
    }

    .grid{
      margin-top: 14px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }

    .pill{
      border:1px solid rgba(255,255,255,.16);
      background: rgba(74,23,48,.55);
      border-radius: 14px;
      padding: 12px 12px;
      min-height: 70px;
    }
    .pill .k{color: rgba(255,241,247,.72); font-size: 12.5px}
    .pill .v{margin-top:6px; font-weight:800; letter-spacing:-.01em}
    .muted{color: rgba(255,241,247,.72)}
    .mono{font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;}

    .verse{
      margin-top: 14px;
      padding: 14px 14px;
      border-radius: var(--radius2);
      background: rgba(74,23,48,.45);
      border: 1px solid rgba(255,255,255,.16);
    }
    .verse p{margin:0}
    .verse .ref{margin-top:6px; color: rgba(255,241,247,.72); font-size: 12.5px}

    .actions{
      margin-top: 14px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }

    .btn{
      appearance:none;
      border:none;
      border-radius: 14px;
      padding: 12px 12px;
      font-weight: 900;
      letter-spacing:-.01em;
      cursor:pointer;
      display:flex;
      justify-content:center;
      align-items:center;
      gap:8px;
      text-decoration:none;
      user-select:none;
      transition: transform .06s ease, filter .15s ease;
      text-align:center;
    }
    .btn:active{transform: translateY(1px)}

    .btn.pink{
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      color: #fff;
      box-shadow: 0 12px 26px rgba(236,72,153,.25);
    }
    .btn.ghost{
      background: rgba(255,255,255,.10);
      color: var(--text);
      border: 1px solid rgba(255,255,255,.22);
      box-shadow:none;
    }

    .section{
      margin-top: 12px;
      border: 1px solid rgba(255,255,255,.16);
      background: rgba(59,18,38,.55);
      border-radius: var(--radius);
      overflow:hidden;
    }
    .sec-h{
      width:100%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding: 14px 14px;
      background: rgba(74,23,48,.55);
      border:none;
      color: var(--text);
      cursor:pointer;
      font-weight:900;
      letter-spacing:-.01em;
    }
    .chev{opacity:.85; transition: transform .15s ease}
    .sec-h[aria-expanded="true"] .chev{transform: rotate(180deg)}
    .sec-b{
      padding: 12px 14px 14px;
      border-top:1px solid rgba(255,255,255,.10);
      color: rgba(255,241,247,.95);
    }
    .sec-b p{margin: 10px 0}
    ul{margin: 10px 0 0 18px; padding:0}
    li{margin: 6px 0}

    .tag{
      display:inline-flex;
      gap:6px;
      align-items:center;
      padding: 6px 10px;
      border-radius: 999px;
      background: rgba(236,72,153,.18);
      border: 1px solid rgba(236,72,153,.35);
      font-size: 12.5px;
      color: rgba(255,241,247,.98);
      font-weight:800;
    }

    .timeline{
      margin-top: 10px;
      display:flex;
      flex-direction:column;
      gap:10px;
    }
    .row{
      display:flex;
      gap:10px;
      align-items:flex-start;
      padding: 10px;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(74,23,48,.38);
    }
    .time{
      min-width: 76px;
      font-weight: 900;
      color: rgba(255,241,247,.95);
    }

    .toast{
      position: fixed;
      left: 50%;
      bottom: 18px;
      transform: translateX(-50%);
      background: rgba(59,18,38,.92);
      border: 1px solid rgba(255,255,255,.20);
      color: var(--text);
      padding: 10px 12px;
      border-radius: 999px;
      font-size: 13px;
      opacity: 0;
      pointer-events:none;
      transition: opacity .18s ease, transform .18s ease;
      display:flex;
      gap:8px;
      align-items:center;
      max-width: min(520px, calc(100vw - 24px));
    }
    .toast.show{opacity:1; transform: translateX(-50%) translateY(-2px)}

    .footer{
      margin-top: 16px;
      color: rgba(255,241,247,.72);
      font-size: 12.5px;
      text-align:center;
    }

    @media (max-width: 380px){
      .grid{grid-template-columns:1fr}
      .actions{grid-template-columns:1fr}
    }

    .music-btn{
  position: fixed;
  right: 14px;
  bottom: 72px;
  z-index: 999;
  padding: 10px 12px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,.22);
  background: rgba(59,18,38,.88);
  color: var(--text);
  font-weight: 900;
  box-shadow: 0 12px 26px rgba(236,72,153,.20);
  cursor: pointer;
}
.music-btn:active{transform: translateY(1px)}

  </style>
</head>

<body>
  <div class="wrap">
    <div class="hero">

      <!-- ✅ 포스터(네 링크) -->
      <img
        class="poster"
        src="https://i.postimg.cc/yBcFY6z8/jemog-eul-iblyeoghaejuseyo-%282%29.png"
        alt="2026 일일수련회 포스터"
        loading="lazy"
      />

      <div class="badge"><span class="dot"></span><span id="topLabel">2026 DAY RETREAT</span></div>
      <h1 id="title">일일수련회 초대장</h1>
      <p class="subtitle" id="subtitle">함께 예배하고, 회복하고, 다시 시작하는 하루</p>

      <div class="grid">
        <div class="pill">
          <div class="k">일시</div>
          <div class="v" id="whenText">2026.02.21 (토) 오전 10시</div>
          <div class="k muted" style="margin-top:6px">D-Day <span class="mono" id="dday">—</span></div>
        </div>
        <div class="pill">
          <div class="k">장소</div>
          <div class="v" id="whereText">시흥성전</div>
          <div class="k muted" style="margin-top:6px" id="addrText">주소(복사 가능)</div>
        </div>
      </div>

      <div class="verse">
        <p id="verseText">“백성이 각기 자녀들을 위하여 마음이 슬퍼서 다윗을 돌로 치자 하니 다윗이 크게 군급하였으나 그 하나님 여호와를 힘입고 용기를 얻었더라”</p>
        <div class="ref" id="verseRef">사무엘상 30장 6절</div>
      </div>

      <!-- ✅ 메일로 바로 받기(참석신청/문의하기) + 복사/공유 -->
      <div class="actions">
        
      
        <button class="btn ghost" id="copyBtn" type="button">📍 주소 복사</button>
        <button class="btn ghost" id="shareBtn" type="button">📤 공유하기</button>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="true" aria-controls="sec1">
        안내 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec1">
        <div class="tag">회복 · 용기 · 동행</div>
        <p class="muted" id="descText">
          다윗이 극심한 위기 속에서도 하나님을 힘입어 용기를 얻었던 것처럼,
          우리도 예배와 말씀, 공동체 안에서 다시 회복하는 시간을 갖고자 합니다.
        </p>
        <ul id="bullets">
          <li>대상: 김포 · 인천 · 부평 · 시흥 청년</li>
          <li>참석 목표: 80명</li>
          <li>준비물: 성경 / 노트 / 필기도구 / 편한복장</li>
        </ul>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="false" aria-controls="sec2">
        타임테이블 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec2" hidden>
        <div class="timeline">
          <div class="row"><div class="time">10:00-10:30</div><div><b>준비찬양</b><div class="muted">예배전 찬양</div></div></div>
          <div class="row"><div class="time">10:30-11:00</div><div><b>개회예배</b><div class="muted">말씀 · 찬양</div></div></div>
          <div class="row"><div class="time">11:00-11:50</div><div><b>아이스브레이킹</b><div class="muted">조별 게임</div></div></div>
          <div class="row"><div class="time">11:50-13:20</div><div><b>점심시간</b><div class="muted">맛있는 점심😝</div></div></div>
          <div class="row"><div class="time">13:20-14:20</div><div><b>전체특강</b><div class="muted">특강</div></div></div>
          <div class="row"><div class="time">14:20-16:20</div><div><b>"RE커버리"</b><div class="muted">회복의 길로!</div></div></div>
           <div class="row"><div class="time">16:20-16:50</div><div><b>"신령과진정"</b><div class="muted">예배전 찬양</div></div></div>
                <div class="row"><div class="time">16:50-18:20</div><div><b>"성령충만기도회"</b><div class="muted">예배&기도</div></div></div>
                 <div class="row"><div class="time">18:20</div><div><b>"사진촬영 및 귀가"</b><div class="muted">일상에서 계속되는 회복의 순간간으로</div></div></div>
        </div>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="false" aria-controls="sec3">
        문의 정보 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec3" hidden>
        <p class="muted">추가적인 문의사항은 연락부탁드립니다.</p>
        <ul>
          <li class="muted">담당자: <span id="contactName">권성경 010 -5780-7231</span></li>
          <li class="muted">이메일: <span class="mono" id="contactEmail">YOUR_EMAIL_HERE</span></li>
        </ul>
      </div>
    </div>

    <div class="footer">
      © 2026 일일수련회 · 모바일 초대장
    </div>
  </div>

  <div class="toast" id="toast">✅ 복사되었습니다</div>

  <script>
    /**********************
     * ✅ 여기만 바꾸면 끝
     **********************/
    const INVITE = {
      emailTo: "jnkwon1214@naver.com",  // ← 너의 이메일로 바꿔줘!
      title: "2026 일일수련회 [회복]",
      whenText: "2026.02.21 (토) 오전 10시",
      whereText: "시흥성전",
      address: "경기도 시흥시 신천로44번안길 20-1 은혜와진리교회",
      // 디데이 계산용 (로컬시간)
      startISO: "2026-02-21T10:00"
    };

    const $ = (id) => document.getElementById(id);

    $("whenText").textContent = INVITE.whenText;
    $("whereText").textContent = INVITE.whereText;
    $("addrText").textContent = INVITE.address;
    $("contactEmail").textContent = INVITE.emailTo;

    /**********************
     * D-Day
     **********************/
    function calcDday(startISO){
      const now = new Date();
      const start = new Date(startISO);
      const ms = start - now;
      const days = Math.ceil(ms / (1000*60*60*24));
      if (isNaN(days)) return "—";
      if (days > 0) return `D-${days}`;
      if (days === 0) return "D-DAY";
      return `D+${Math.abs(days)}`;
    }
    $("dday").textContent = calcDday(INVITE.startISO);

    /**********************
     * 아코디언
     **********************/
    document.querySelectorAll(".sec-h").forEach((btn) => {
      btn.addEventListener("click", () => {
        const expanded = btn.getAttribute("aria-expanded") === "true";
        const targetId = btn.getAttribute("aria-controls");
        const panel = document.getElementById(targetId);
        btn.setAttribute("aria-expanded", String(!expanded));
        panel.hidden = expanded ? true : false;
      });
    });

    /**********************
     * 토스트
     **********************/
    let toastTimer = null;
    function toast(msg){
      const t = $("toast");
      t.textContent = msg;
      t.classList.add("show");
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => t.classList.remove("show"), 1400);
    }

    /**********************
     * 주소 복사 / 공유
     **********************/
    $("copyBtn").addEventListener("click", async () => {
      try{
        await navigator.clipboard.writeText(INVITE.address);
        toast("✅ 주소가 복사됐어요");
      }catch(e){
        toast("⚠️ 복사 실패: 브라우저 권한 확인");
      }
    });

    $("shareBtn").addEventListener("click", async () => {
      const shareData = {
        title: INVITE.title,
        text: `${INVITE.title}\n${INVITE.whenText}\n${INVITE.whereText}`,
        url: location.href
      };
      if (navigator.share){
        try{ await navigator.share(shareData); }
        catch(e){ /* 사용자가 취소 */ }
      }else{
        try{
          await navigator.clipboard.writeText(location.href);
          toast("🔗 링크가 복사됐어요");
        }catch(e){
          toast("⚠️ 공유 불가: 링크를 직접 복사해 주세요");
        }
      }
    });


    function openSection(id){
  const panel = document.getElementById(id);
  const btn = document.querySelector(`.sec-h[aria-controls="${id}"]`);
  if (!panel || !btn) return;

  btn.setAttribute("aria-expanded", "true");
  panel.hidden = false;
}
window.addEventListener("DOMContentLoaded", () => {
  const ids = ["sec1","sec2","sec3"];
  ids.forEach((id, i) => {
    setTimeout(() => openSection(id), 180 * i); // 0.18초 간격으로 착착 열림
  });
});
    const bgm = document.getElementById("bgm");
const musicBtn = document.getElementById("musicBtn");
let isPlaying = false;

musicBtn.addEventListener("click", async () => {
  try{
    if (!isPlaying){
      await bgm.play();
      isPlaying = true;
      musicBtn.textContent = "🔇 BGM";
      toast("🎵 배경음악 재생");
    }else{
      bgm.pause();
      isPlaying = false;
      musicBtn.textContent = "🔊 BGM";
      toast("⏸️ 배경음악 정지");
    }
  }catch(e){
    toast("⚠️ 재생 실패: 파일/브라우저 정책 확인");
  }
});

// “첫 터치”로 자동 재생(모바일 정책 대응)
window.addEventListener("pointerdown", async () => {
  if (isPlaying) return;
  try{
    await bgm.play();
    isPlaying = true;
    musicBtn.textContent = "🔇 BGM";
  }catch(e){}
}, { once:true });


  </script>
   <audio id="bgm" preload="auto" loop playsinline>
    <source src="bgm.mp3" type="audio/mpeg" />
    <source src="bgm.m4a" type="audio/mp4" />
  </audio>

<button class="music-btn" id="musicBtn" type="button" aria-label="배경음악 재생">
  🔊 BGM
</button>

</body>
</html>
