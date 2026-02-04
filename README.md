<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#111827" />
  <title>일일수련회 모바일 초대장</title>
  <style>
    :root{
      --bg:#0b1020;
      --card:#111827;
      --card2:#0f172a;
      --text:#e5e7eb;
      --muted:#9ca3af;
      --line:rgba(255,255,255,.10);
      --brand:#22c55e;
      --brand2:#60a5fa;
      --danger:#ef4444;
      --shadow: 0 14px 40px rgba(0,0,0,.35);
      --radius: 18px;
      --radius2: 14px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background:
        radial-gradient(1200px 700px at 20% -10%, rgba(34,197,94,.25), transparent 60%),
        radial-gradient(1200px 700px at 90% 10%, rgba(96,165,250,.20), transparent 55%),
        linear-gradient(180deg, var(--bg), #050814 85%);
      color:var(--text);
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Apple SD Gothic Neo", "Noto Sans KR", Arial, "Helvetica Neue", sans-serif;
      line-height:1.45;
      -webkit-font-smoothing: antialiased;
      padding: 22px 14px 80px;
    }
    a{color:inherit}
    .wrap{max-width: 520px; margin:0 auto}
    .hero{
      position: relative;
      background: linear-gradient(135deg, rgba(34,197,94,.18), rgba(96,165,250,.12));
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 22px 18px 18px;
      box-shadow: var(--shadow);
      overflow:hidden;
    }
    .badge{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding: 7px 11px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(17,24,39,.55);
      color: var(--muted);
      font-size: 12.5px;
    }
    .badge .dot{
      width:8px; height:8px; border-radius:50%;
      background: var(--brand);
      box-shadow: 0 0 0 4px rgba(34,197,94,.14);
    }
    h1{
      margin: 12px 0 8px;
      font-size: 26px;
      letter-spacing:-.02em;
    }
    .subtitle{
      margin:0 0 14px;
      color: var(--muted);
      font-size: 14px;
    }
    .verse{
      margin-top: 14px;
      padding: 14px 14px;
      border-radius: var(--radius2);
      background: rgba(17,24,39,.65);
      border: 1px solid rgba(255,255,255,.10);
    }
    .verse p{margin:0}
    .verse .ref{margin-top:6px; color:var(--muted); font-size: 12.5px}
    .grid{
      margin-top: 14px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }
    .pill{
      border:1px solid rgba(255,255,255,.10);
      background: rgba(15,23,42,.72);
      border-radius: 14px;
      padding: 12px 12px;
      min-height: 64px;
    }
    .pill .k{color:var(--muted); font-size: 12.5px}
    .pill .v{margin-top:6px; font-weight:700; letter-spacing:-.01em}
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
      font-weight: 800;
      letter-spacing:-.01em;
      color: #0b1020;
      background: var(--brand);
      box-shadow: 0 12px 26px rgba(34,197,94,.18);
      cursor:pointer;
      display:flex;
      justify-content:center;
      align-items:center;
      gap:8px;
      text-decoration:none;
      user-select:none;
      transition: transform .06s ease, filter .15s ease;
    }
    .btn:active{transform: translateY(1px)}
    .btn.secondary{
      background: rgba(96,165,250,.95);
      box-shadow: 0 12px 26px rgba(96,165,250,.18);
    }
    .btn.ghost{
      background: rgba(17,24,39,.55);
      color: var(--text);
      border: 1px solid rgba(255,255,255,.12);
      box-shadow:none;
    }
    .btn.danger{
      background: rgba(239,68,68,.95);
      box-shadow: 0 12px 26px rgba(239,68,68,.18);
    }
    .section{
      margin-top: 12px;
      border: 1px solid rgba(255,255,255,.10);
      background: rgba(17,24,39,.55);
      border-radius: var(--radius);
      overflow:hidden;
    }
    .sec-h{
      width:100%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding: 14px 14px;
      background: rgba(15,23,42,.55);
      border:none;
      color: var(--text);
      cursor:pointer;
      font-weight:800;
      letter-spacing:-.01em;
    }
    .chev{opacity:.8; transition: transform .15s ease}
    .sec-h[aria-expanded="true"] .chev{transform: rotate(180deg)}
    .sec-b{
      padding: 12px 14px 14px;
      border-top:1px solid rgba(255,255,255,.08);
      color: rgba(229,231,235,.95);
    }
    .sec-b p{margin: 10px 0}
    ul{margin: 10px 0 0 18px; padding:0}
    li{margin: 6px 0}
    .muted{color:var(--muted)}
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
      border:1px solid rgba(255,255,255,.09);
      background: rgba(15,23,42,.55);
    }
    .time{
      min-width: 76px;
      font-weight: 900;
      color: rgba(229,231,235,.95);
    }
    .tag{
      display:inline-flex;
      gap:6px;
      align-items:center;
      padding: 6px 10px;
      border-radius: 999px;
      background: rgba(34,197,94,.14);
      border: 1px solid rgba(34,197,94,.28);
      font-size: 12.5px;
      color: rgba(229,231,235,.98);
    }
    .toast{
      position: fixed;
      left: 50%;
      bottom: 18px;
      transform: translateX(-50%);
      background: rgba(17,24,39,.92);
      border: 1px solid rgba(255,255,255,.16);
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
      color: var(--muted);
      font-size: 12.5px;
      text-align:center;
    }
    .small-actions{margin-top:10px; display:grid; grid-template-columns: 1fr 1fr; gap:10px;}
    .mono{font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;}
  </style>
</head>

<body>
  <div class="wrap">
    <div class="hero">
      <div class="badge"><span class="dot"></span><span id="topLabel">DAY RETREAT · RECOVERY</span></div>
      <h1 id="title">일일수련회 초대장</h1>
      <p class="subtitle" id="subtitle">함께 예배하고, 회복하고, 다시 시작하는 하루</p>

      <div class="grid">
        <div class="pill">
          <div class="k">일시</div>
          <div class="v" id="whenText">2026-02-?? (토) 10:00–18:00</div>
          <div class="k muted" style="margin-top:6px">D-Day <span class="mono" id="dday">—</span></div>
        </div>
        <div class="pill">
          <div class="k">장소</div>
          <div class="v" id="whereText">OO교회 3층 본당</div>
          <div class="k muted" style="margin-top:6px" id="addrText">서울시 … (복사 가능)</div>
        </div>
      </div>

      <div class="verse">
        <p id="verseText">“Have I not commanded you? Be strong and courageous… for the Lord your God will be with you wherever you go.”</p>
        <div class="ref" id="verseRef">Joshua 1:9</div>
      </div>

      <div class="actions">
        <a class="btn" id="rsvpBtn" href="#" role="button" aria-label="참석 신청">
          ✅ 참석 신청
        </a>
        <a class="btn secondary" id="kakaoBtn" href="#" role="button" aria-label="문의하기">
          💬 문의하기
        </a>
        <button class="btn ghost" id="copyBtn" type="button">📍 주소 복사</button>
        <button class="btn ghost" id="shareBtn" type="button">📤 공유하기</button>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="true" aria-controls="sec1">
        프로그램 안내 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec1">
        <div class="tag">RECOVERY 코스</div>
        <p class="muted" id="descText">
          회복은 “문제 해결”이 아니라 “다시 하나님께 붙는 것”에서 시작됩니다.
          예배 · 미션 · 나눔으로 구성된 참여형 프로그램입니다.
        </p>
        <ul id="bullets">
          <li>미션형 코스(실내) + 팀전</li>
          <li>말씀/기도/회복 나눔</li>
          <li>초대장 링크 하나로 안내/신청/공유까지</li>
        </ul>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="false" aria-controls="sec2">
        타임테이블 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec2" hidden>
        <div class="timeline" id="timeline">
          <div class="row"><div class="time">10:00</div><div><b>체크인 & 아이스브레이킹</b><div class="muted">팀 배정 / 안내</div></div></div>
          <div class="row"><div class="time">11:00</div><div><b>개회예배</b><div class="muted">회복의 시작</div></div></div>
          <div class="row"><div class="time">12:00</div><div><b>점심</b><div class="muted">교제</div></div></div>
          <div class="row"><div class="time">13:30</div><div><b>미션 코스</b><div class="muted">RECOVERY 퍼즐/게임</div></div></div>
          <div class="row"><div class="time">16:30</div><div><b>회복 나눔</b><div class="muted">간증/소그룹</div></div></div>
          <div class="row"><div class="time">17:30</div><div><b>기도회</b><div class="muted">결단과 파송</div></div></div>
        </div>

        <div class="small-actions">
          <a class="btn ghost" id="gcalBtn" href="#" role="button">📅 Google 캘린더 추가</a>
          <button class="btn ghost" id="icsBtn" type="button">🗓️ iPhone/Outlook(.ics)</button>
        </div>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="false" aria-controls="sec3">
        준비물 & 안내 <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec3" hidden>
        <ul>
          <li>개인 성경/노트/필기도구</li>
          <li>활동하기 편한 복장(실내)</li>
          <li class="muted">문의: <span id="contactName">담당자 OOO</span> · <span class="mono" id="contactPhone">010-0000-0000</span></li>
        </ul>
      </div>
    </div>

    <div class="section">
      <button class="sec-h" type="button" aria-expanded="false" aria-controls="sec4">
        커스텀 메시지 (이름 넣기) <span class="chev">▾</span>
      </button>
      <div class="sec-b" id="sec4" hidden>
        <p class="muted">링크에 <span class="mono">?name=성경&msg=함께가요</span> 처럼 붙이면 초대장이 개인화돼요.</p>
        <div class="pill" style="margin-top:10px">
          <div class="k">미리보기</div>
          <div class="v" id="personalMsg">—</div>
        </div>
        <div class="small-actions">
          <button class="btn ghost" id="copyLinkBtn" type="button">🔗 개인화 링크 복사</button>
          <button class="btn ghost" id="resetBtn" type="button">↩︎ 기본으로</button>
        </div>
      </div>
    </div>

    <div class="footer" id="footerText">
      © 일일수련회 초대장 · 링크 하나로 안내/신청/공유
    </div>
  </div>

  <div class="toast" id="toast">✅ 복사되었습니다</div>

  <script>
    /**********************
     * 1) 여기만 바꾸면 됨
     **********************/
    const INVITE = {
      topLabel: "DAY RETREAT · RECOVERY",
      title: "일일수련회 초대장",
      subtitle: "함께 예배하고, 회복하고, 다시 시작하는 하루",
      // ISO 형식 권장: YYYY-MM-DDTHH:mm (로컬시간 기준)
      startISO: "2026-02-22T10:00",
      endISO:   "2026-02-22T18:00",
      whenText: "2026-02-22 (토) 10:00–18:00",
      whereText: "OO교회 3층 본당",
      address: "서울시 ○○구 ○○로 123 (OO교회)",

      verseText: "“Have I not commanded you? Be strong and courageous… for the Lord your God will be with you wherever you go.”",
      verseRef: "Joshua 1:9",

      descText: "회복은 ‘문제 해결’이 아니라 ‘다시 하나님께 붙는 것’에서 시작됩니다. 예배 · 미션 · 나눔으로 구성된 참여형 프로그램입니다.",

      contactName: "담당자 OOO",
      contactPhone: "010-0000-0000",

      // RSVP / 문의 링크 (원하는 걸로 교체)
      // 예: 구글폼, 카톡채널, 오픈채팅, 네이버폼 등
      rsvpUrl: "https://forms.gle/XXXXXXXXXXXXXXX",
      문의Url: "https://open.kakao.com/o/XXXXXXXX",

      // 지도 링크(선택)
      mapUrl: "https://map.naver.com/"
    };

    /**********************
     * 2) 렌더링
     **********************/
    const $ = (id) => document.getElementById(id);
    $("topLabel").textContent = INVITE.topLabel;
    $("title").textContent = INVITE.title;
    $("subtitle").textContent = INVITE.subtitle;
    $("whenText").textContent = INVITE.whenText;
    $("whereText").textContent = INVITE.whereText;
    $("addrText").textContent = INVITE.address;
    $("verseText").textContent = INVITE.verseText;
    $("verseRef").textContent = INVITE.verseRef;
    $("descText").textContent = INVITE.descText;
    $("contactName").textContent = INVITE.contactName;
    $("contactPhone").textContent = INVITE.contactPhone;

    // 버튼 링크
    $("rsvpBtn").href = INVITE.rsvpUrl || "#";
    $("kakaoBtn").href = INVITE.문의Url || "#";

    /**********************
     * 3) D-Day
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
     * 4) 아코디언
     **********************/
    document.querySelectorAll(".sec-h").forEach((btn) => {
      btn.addEventListener("click", () => {
        const expanded = btn.getAttribute("aria-expanded") === "true";
        const targetId = btn.getAttribute("aria-controls");
        const panel = document.getElementById(targetId);
        btn.setAttribute("aria-expanded", String(!expanded));
        if (!expanded) panel.hidden = false;
        else panel.hidden = true;
      });
    });

    /**********************
     * 5) 토스트
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
     * 6) 주소 복사 / 공유
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
        catch(e){ /* 사용자가 취소한 경우 무시 */ }
      }else{
        try{
          await navigator.clipboard.writeText(location.href);
          toast("🔗 링크가 복사됐어요");
        }catch(e){
          toast("⚠️ 공유 불가: 링크를 직접 복사해 주세요");
        }
      }
    });

    /**********************
     * 7) Google 캘린더 링크 생성
     **********************/
    function toGcalTime(iso){
      // Google Calendar expects UTC in YYYYMMDDTHHMMSSZ
      const d = new Date(iso);
      const pad = (n) => String(n).padStart(2,"0");
      const yyyy = d.getUTCFullYear();
      const mm = pad(d.getUTCMonth()+1);
      const dd = pad(d.getUTCDate());
      const hh = pad(d.getUTCHours());
      const mi = pad(d.getUTCMinutes());
      const ss = pad(d.getUTCSeconds());
      return `${yyyy}${mm}${dd}T${hh}${mi}${ss}Z`;
    }
    const gcalUrl = (() => {
      const dates = `${toGcalTime(INVITE.startISO)}/${toGcalTime(INVITE.endISO)}`;
      const params = new URLSearchParams({
        action: "TEMPLATE",
        text: INVITE.title,
        dates,
        details: `${INVITE.subtitle}\n\nRSVP: ${INVITE.rsvpUrl}`,
        location: `${INVITE.whereText} · ${INVITE.address}`
      });
      return `https://calendar.google.com/calendar/render?${params.toString()}`;
    })();
    $("gcalBtn").href = gcalUrl;

    /**********************
     * 8) ICS 다운로드 (iPhone/Outlook)
     **********************/
    function makeICS(){
      const dt = (iso) => {
        const d = new Date(iso);
        const pad = (n) => String(n).padStart(2,"0");
        // UTC
        return `${d.getUTCFullYear()}${pad(d.getUTCMonth()+1)}${pad(d.getUTCDate())}T${pad(d.getUTCHours())}${pad(d.getUTCMinutes())}${pad(d.getUTCSeconds())}Z`;
      };
      const uid = `invite-${Math.random().toString(16).slice(2)}@local`;
      const lines = [
        "BEGIN:VCALENDAR",
        "VERSION:2.0",
        "PRODID:-//Mobile Invite//KR//EN",
        "CALSCALE:GREGORIAN",
        "METHOD:PUBLISH",
        "BEGIN:VEVENT",
        `UID:${uid}`,
        `DTSTAMP:${dt(new Date().toISOString())}`,
        `DTSTART:${dt(INVITE.startISO)}`,
        `DTEND:${dt(INVITE.endISO)}`,
        `SUMMARY:${escapeICS(INVITE.title)}`,
        `DESCRIPTION:${escapeICS(`${INVITE.subtitle}\\n\\nRSVP: ${INVITE.rsvpUrl}`)}`,
        `LOCATION:${escapeICS(`${INVITE.whereText} · ${INVITE.address}`)}`,
        "END:VEVENT",
        "END:VCALENDAR"
      ];
      return lines.join("\r\n");
    }
    function escapeICS(s){
      return String(s)
        .replace(/\\/g, "\\\\")
        .replace(/\n/g, "\\n")
        .replace(/,/g, "\\,")
        .replace(/;/g, "\\;");
    }
    $("icsBtn").addEventListener("click", () => {
      const blob = new Blob([makeICS()], {type:"text/calendar;charset=utf-8"});
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = `${INVITE.title}.ics`;
      document.body.appendChild(a);
      a.click();
      a.remove();
      URL.revokeObjectURL(url);
      toast("🗓️ .ics 파일을 다운로드했어요");
    });

    /**********************
     * 9) 개인화 (name/msg)
     **********************/
    const params = new URLSearchParams(location.search);
    const name = params.get("name");
    const msg  = params.get("msg");
    const personal = (() => {
      if (!name && !msg) return "—";
      const n = name ? `${name}님, ` : "";
      const m = msg ? msg : "함께해요!";
      return `${n}${m}`;
    })();
    $("personalMsg").textContent = personal;

    $("copyLinkBtn").addEventListener("click", async () => {
      const url = new URL(location.href);
      if (!url.searchParams.get("name")) url.searchParams.set("name", "성경");
      if (!url.searchParams.get("msg"))  url.searchParams.set("msg", "일일수련회에서 만나요!");
      try{
        await navigator.clipboard.writeText(url.toString());
        toast("🔗 개인화 링크 복사 완료");
      }catch(e){
        toast("⚠️ 복사 실패: 브라우저 권한 확인");
      }
    });

    $("resetBtn").addEventListener("click", () => {
      const url = new URL(location.href);
      url.search = "";
      location.href = url.toString();
    });

    /**********************
     * 10) 옵션: 장소 탭하면 지도 열기
     **********************/
    $("whereText").style.cursor = "pointer";
    $("whereText").addEventListener("click", () => {
      if (INVITE.mapUrl) window.open(INVITE.mapUrl, "_blank");
    });
  </script>
</body>
</html>
