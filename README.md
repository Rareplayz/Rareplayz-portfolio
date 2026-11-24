# Rareplayz-portfolio
<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rareplayz — Official Portfolio</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            brandDark: '#080c14',
            cardBg: '#0f172a',
            cardBorder: '#1e293b',
            accentIndigo: '#6366f1',
            accentCyan: '#06b6d4',
            accentEmerald: '#10b981',
            accentAmber: '#f59e0b'
          },
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            mono: ['JetBrains Mono', 'Fira Code', 'monospace']
          }
        }
      }
    }
  </script>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">

  <!-- React 18 & Babel CDN -->
  <script src="https://unpkg.com/react@18/umd/react.production.min.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js" crossorigin></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <style>
    body {
      background-color: #080c14;
      color: #f1f5f9;
      font-family: 'Inter', sans-serif;
    }
    .custom-scrollbar::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    .custom-scrollbar::-webkit-scrollbar-track {
      background: #080c14;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: #1e293b;
      border-radius: 4px;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb:hover {
      background: #6366f1;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fadeIn {
      animation: fadeIn 0.3s ease-out forwards;
    }
  </style>
</head>
<body class="selection:bg-indigo-600 selection:text-white">
  <div id="root"></div>

  <script type="text/babel">
    const { useState } = React;

    // Full Script 1 Data
    const SCRIPT_1_DATA = {
      title: "Script 1: I Broke Into Minecraft’s Biggest Heist (Underrated Weapon)",
      description: "High-retention story script focusing on sneaking into a locked vault to steal 'The Glitch Bow'.",
      content: [
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Arre bhai, sach bata raha hu, maine pichle 30 din se ek secret Minecraft server par chupke se game khela hai. Is server ka naam tha The Grand Vault of Netherstone." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Yahan ek bohot hi unique aur underrated weapon tha—The Glitch Bow—jo poore server me sirf ek hi baar milta hai aur iske arrows wall ke aar-paar jaakar enemies ko kahin se bhi target kar sakte hain. Problem yeh thi ki server ke admin aur bade players ne milkar isko bachane ke liye ek underground bunker banaya tha, jahan har step par khatarnak traps aur guards the." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Mera plan ekdum simple tha: security ko chakma do, bunker ke andar ghuso, woh weapon churao, aur admin ke aane se pehle patli gali se nikal lo." },
        { type: "scene", text: "--- Bunker Ke Andar Ghusna ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Day 1. Maine apna naam badal kar \"BlockArchitect99\" rakh liya aur ek aam player ki tarah seedha andar ghus gaya. Dekhte hain yeh log khud ko kitna bada pro maante hain." },
        { type: "narration", text: "Bunker ke baahar ek bada sa board laga tha:\n\"Yahan aana sakht mana hai, andar aaye toh security aisi bajayegi ki yaad rakhoge.\"" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main chupchaap logon ke ek group ke peeche chup kar lobby me nikal liya. Wahan ek guard khada tha jo full netherite armor pehne hua tha." },
        { type: "dialogue", speaker: "Guard", text: "Ruk be, yahan aane ki permission kisne di? Sirf bade developers aur donors andar ja sakte hain." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Arre bhai, main toh bas naya student hu, mujhe toh bas yeh deewar ke design aur glass blocks dekhne the ki kaise banaye tumne!" },
        { type: "dialogue", speaker: "Guard", text: "Hmm, chal theek hai, par aage mat badhna warna turant ban mar dunga. Chal nikal yaha se!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bhai ko zara bhi andaza nahi tha ki baaton-baaton me maine uski jeb se control room ka keycard uda liya tha." },
        { type: "scene", text: "--- Security Ko Paar Karna ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Agle do hafton tak maine raat ke sannate me server ke ventilation pipes aur underground rasto ko dhoondha." },
        { type: "narration", text: "Bunker ke andar 3 level ki security thi:\n1. Laser Grid: Redstone ka khatarnak jaal, jisko touch karte hi poore server me alarm baj jata.\n2. Warden Vault: Ek ekdum andheri jagah jahan bina ek bhi aawaz kiye chalna padta tha, warna Warden aakar turant kaam tamaam kar deta.\n3. Core Vault: Jahan wo chamakta hua Glitch Bow ek center table par rakha tha." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main pipe se hote hue dabe paav seedha Warden Vault me kood gaya." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Shhh, bhai saans bhi dheere leni hai." },
        { type: "narration", text: "Ek second ke liye mera paer thoda zorse zameen par pad gaya, aur wahan paas khade Warden ne aawaz sun li! Wo seedha meri taraf dauda." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Baap re, ab toh gaye!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Maine bina time waste kiye invisibility ka potion peena shuru kiya aur ek corner me chup gaya. Warden ekdum confuse ho gaya aur wapas andhere me chala gaya. Bach gaye bhai, dil ki dhadkan ruk gayi thi!" },
        { type: "scene", text: "--- Badi Chori (The Heist) ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Day 28. Aakhirkaar wo din aa hi gaya. Main saari security ki dhajiya udaate hue Core Vault ke darwaze par pahunch gaya." },
        { type: "narration", text: "Saamne ek bada sa vault door tha jiska password har 10 minute me apne aap badalta rehta tha." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Inhe laga hoga ki koi ise khol nahi payega. Par inko kya pata ki main pichle ek hafte se chupke se unka code track kar raha tha!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Maine console ke paas jaakar fatafat levers khinche. WHOOSH. Wo bhari-bhaarkam doors dheere-dheere khul gaye, aur saamne ekdam chamakta hua, rainbow-colored Glitch Bow hawa me floating state me dikhi." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Let’s goooo! Kasam se, itna underrated par OP weapon maine poore Minecraft me pehle kabhi nahi dekha!" },
        { type: "narration", text: "Jaise hi maine usko haath lagaya, poore server me laal alarm bajne laga aur screen par bada-bada likh kar aa gaya:\nWARNING: VAULT LOOTA JA CHUKA HAI! INTRUDER ANDAR HAI!" },
        { type: "scene", text: "--- Bhagam-Bhag (The Escape & Admin Ka Asli Chehra) ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Server ka admin aur uski poori elite team ek second me teleport ho kar wahan aa gayi!" },
        { type: "dialogue", speaker: "Admin", text: "Abe yeh kaun hai be, isne vault kaise khola? Kisi ko bhi zinda mat jaane dena!" },
        { type: "narration", text: "Poori server me afra-tafri mach gayi. 15 guards diamond swords aur elytra lekar meri taraf daude." },
        { type: "dialogue", speaker: "Admin", text: "Ruko sab log, isko mat maaro... kyunki yeh bow churane ka plan khud mera tha! Main is poore server ko hack karke saare players ka data delete karne wala tha, par yeh nalla pehle hi aa gaya!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Wah bhai, matlab security bachane wala khud hi sabse bada chor nikla! Par sorry, yeh underrated weapon ab mera hai!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main jaldi se ek ender-pearl nikalta hu aur chat ki taraf full speed me phenk deta hu. Pearl mujhe seedha upar roof par khinch leta hai." },
        { type: "dialogue", speaker: "Admin & Guards", text: "Arre usko pakdo, wo bhaag raha hai!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bunker toh tumne mast banaya tha, par apna evil plan chupana bhool gaye!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Maine jaldi se apni pocket se Elytra aur firework rocket nikala, pehna, aur kinare se seedha jump laga di." },
        { type: "dialogue", speaker: "Admin", text: "Abe yeh udh raha hai, NO WAY! Isko roko koi!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main hawa me glide karte hue firework se boost deta gaya aur server ke world border ke bahar nikal gaya." }
      ]
    };

    // Full Script 2 Data
    const SCRIPT_2_DATA = {
      title: "Script 2: I Joined My Haters' Minecraft Server (Bad Idea)",
      description: "Undercover SMP survival story featuring faction wars, secret diamond distribution, and a TNT climax.",
      content: [
        { type: "dialogue", speaker: "SENPAISPIDER", text: "So I spent the last 30 days secretly playing on a private Minecraft SMP. What these guys didn't know is that pretty much every single person on this server completely hates my guts." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "In logon ne poora server hi bas mujhey gaali dene aur mera mazaak banane ke liye banaya tha. So obviously, maine ek alt account liya, naam change kiya, and quietly andar ghus gaya." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "The second I joined though, I saw kya chal rha hai idar. Server poora do groups me bata hua tha: Rich guys jinke paas saara netherite tha, aur Poor group jo underground chote se dirt huts me reh rahe the. Adha time ye log diamonds ke liye ladte the aur baaki adha time mera downfall plan karte the." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Mera simple plan tha: secretely poor group ki help karo, rich group ka economy poora kharab kardo, aur dekho kitne din tak mera secret bacha rehta hai." },
        { type: "scene", text: "--- Joining the Server ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Day 1. I just spawned in on my alt, NotSenpaiSpider. Dekhte hain kitna time survive kar pata hu." },
        { type: "narration", text: "A rich player in full netherite gear mere paas daud ke aata hai." },
        { type: "dialogue", speaker: "Rich", text: "Ruk ek minute! Kaun hai tu? Apni inventory dikha chal!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bro main abhi abhi toh spawn hua hu, mere paas bas do sticks aur ek piece of bread hai." },
        { type: "dialogue", speaker: "Rich", text: "Ew. Ek aur gareeb player. Chalo neeche caves me jao isse pehle ki hum tujhe spawn kill kardein." },
        { type: "narration", text: "Rich mujhe wooden bridge se neeche ek dark ravine me dhakka de deta hai." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bhai sahab, kitna rude hai! Guess I’m joining the cave guys then!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main ek cave me jaata hu jahan bohot saare dirt huts bane hue the. Ek player mere paas aata hai." },
        { type: "dialogue", speaker: "Poor", text: "Arre bhai, welcome to the bottom. Upar wale rich logon se bachke rehna. Saari acchi cheezein unke paas hain aur stone mine karne ke liye bhi tax maangte hain." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Toh tum log accha gear banake fight back kyu nahi karte??" },
        { type: "dialogue", speaker: "Poor", text: "Bhai hum toh SenpaiSpider ke liye traps banane me busy hain, kya pata kab uska IP address mil jaye!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Ye log mere se nafrat karne me itne busy hain ki rich group inka poora faayda utha rha hai lol." },
        { type: "scene", text: "--- The Heist ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Agle do hafton ke liye mera plan simple tha: rich team ke vault me ghuso, unke extra diamonds churao, aur poor group ko de do." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main seedha unke vault ke wall par ender-pearl maarta hu, poora shulker box khali karta hu, aur pearl karke bahar nikal jaata hu. In logon ne saamne 3-3 redstone security doors lagaye the, par upar chhat banana hi bhool gaye. Easiest heist ever bhai!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main saare diamonds us poor player ke samne drop kar deta hu jab wo AFK khada tha." },
        { type: "dialogue", speaker: "Poor", text: "WAIT WHAT??? DIAMONDS?! Abe bhai, kisine poora crate bhar ke gear drop kiya hai! Ab aayega maza, ab hum fight karenge!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Sahi hai, isse accha armor craft kar lo. Agli baar jab wo tax maangne aayein toh peeche mat hatna." },
        { type: "scene", text: "--- The Confrontation ---" },
        { type: "narration", text: "Day 28. Dono groups center wall par milte hain, par is baar poor group ke paas full diamond armor tha." },
        { type: "dialogue", speaker: "Rich", text: "Abe tum logon ke paas itne diamonds kahan se aaye?! Tumne humara vault loota hai na?!" },
        { type: "dialogue", speaker: "Poor", text: "Humne kuch nahi churaaya! Kisine humari help ki hai! Ab se hum koi tax nahi dene wale!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bhai log relax! Gear ke liye kyu lad rahe ho jab hum sab milke ek mast server bana sakte hain?" },
        { type: "narration", text: "Poore server pe ekdum silence. Rich player apni character ko meri taraf ghumata hai." },
        { type: "dialogue", speaker: "Poor", text: "Ek sec rukna... \"Mast server bana sakte hain\"? Ye toh bilkul waisa sound kar raha hai jaise SenpaiSpider bolta hai..." },
        { type: "dialogue", speaker: "Poor", text: "Wait a minute... iska movement dekho. Ye parkour jump..." },
        { type: "dialogue", speaker: "Rich", text: "TAB DABA KE ACCOUNT CHECK KARO ABHI!" },
        { type: "narration", text: "A pop-up shows up jisme pata chalta ki alt account SenpaiSpider ka hi hai." },
        { type: "dialogue", speaker: "Rich & Poor", text: "ABEY YE TOH WOHI HAI! SENPAISPIDER IDAR HI HAI!" },
        { type: "scene", text: "--- The Escape ---" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Bhai ek second me dono groups apni dushmani bhool gaye. Rich aur poor factions ne team up kar liya bas mujhe maarne ke liye." },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Poora intense chase shuru hota hai forest me, 10 players mere peeche pad gaye hain." },
        { type: "dialogue", speaker: "Rich", text: "Diamonds ko goli maaro! Pehle SenpaiSpider ko pakdo!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Main bhaag ke seedha us statue ke paas gaya jo unhone spawn par banaya tha—mera ek giant wooden statue jo unhone jalane ke liye rakha tha. Main kisi tarah clutch karke statue ke top par pahunch jaata hu, aur poora server neeche khada ho jata hai." },
        { type: "dialogue", speaker: "Poor", text: "Ab tu phans gaya! Ab kahin bhaag ke nahi ja sakta tu!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Tum log aapas me ladne me itne busy the ki tumne dekha hi nahi maine pichle hafte is statue ke neeche kya lagaya tha." },
        { type: "narration", text: "Main flint and steel nikal ke TNT ko aag laga deta hu." },
        { type: "dialogue", speaker: "Rich", text: "Bhai... kya wo TNT hai?!" },
        { type: "dialogue", speaker: "SENPAISPIDER", text: "Chal bye guys, maza aaya!" },
        { type: "narration", text: "Main pearl maarke nikal jata hu aur poora statue ek boom ke saath explode hota hai, saare haters ko neeche paani me phenk ke!" }
      ]
    };

    const INITIAL_VIDEOS = [
      {
        id: "rp-1",
        title: "High-Stakes Negotiation RP",
        category: "Serious RP",
        focus: "Realistic character building, intense dialogue pacing, situational awareness, and staying in character during high-pressure scenarios.",
        url: ""
      },
      {
        id: "rp-2",
        title: "Character Storyline Finale",
        category: "Story Arc",
        focus: "Deep emotional delivery, dramatic plot climaxes, multi-character interactions, and cinematic execution.",
        url: ""
      },
      {
        id: "rp-3",
        title: "Unscripted Improv & Comedy",
        category: "Improv & Wit",
        focus: "Quick comedic timing, spontaneous banter, crowd interaction, and adapting instantly to chaotic server situations.",
        url: ""
      }
    ];

    function App() {
      const [activeTab, setActiveTab] = useState("rec");
      const [selectedScript, setSelectedScript] = useState("script1");
      const [videos, setVideos] = useState(INITIAL_VIDEOS);
      const [editingVideoId, setEditingVideoId] = useState(null);
      const [tempUrl, setTempUrl] = useState("");
      const [toast, setToast] = useState("");

      const showToast = (msg) => {
        setToast(msg);
        setTimeout(() => setToast(""), 3000);
      };

      const copyDiscord = () => {
        const textToCopy = "rareplayz1";
        if (navigator.clipboard && navigator.clipboard.writeText) {
          navigator.clipboard.writeText(textToCopy);
        } else {
          const textArea = document.createElement("textarea");
          textArea.value = textToCopy;
          document.body.appendChild(textArea);
          textArea.select();
          document.execCommand('copy');
          document.body.removeChild(textArea);
        }
        showToast("Discord ID copied: rareplayz1");
      };

      const handleSaveVideoUrl = (id) => {
        setVideos(videos.map(v => v.id === id ? { ...v, url: tempUrl } : v));
        setEditingVideoId(null);
        setTempUrl("");
        showToast("Video URL saved successfully!");
      };

      const currentScript = selectedScript === "script1" ? SCRIPT_1_DATA : SCRIPT_2_DATA;

      return (
        <div className="min-h-screen flex flex-col bg-brandDark text-slate-100">
          
          {/* Toast Notification */}
          {toast && (
            <div className="fixed bottom-6 right-6 z-50 bg-indigo-600 text-white px-4 py-3 rounded-xl shadow-2xl font-semibold text-sm flex items-center gap-2 border border-indigo-400/30 animate-bounce">
              <span>✨</span> {toast}
            </div>
          )}

          {/* Navigation Bar */}
          <nav className="border-b border-slate-800/80 bg-brandDark/90 backdrop-blur sticky top-0 z-40">
            <div className="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
              <div className="flex items-center gap-3">
                <span className="text-xl sm:text-2xl font-black tracking-tight text-white">
                  Rareplayz
                </span>
                <span className="hidden sm:inline-block px-2.5 py-0.5 rounded-full text-[10px] font-mono uppercase tracking-wider bg-indigo-500/10 text-indigo-400 border border-indigo-500/20">
                  Official Portfolio
                </span>
              </div>

              {/* Navigation Links */}
              <div className="flex items-center gap-2 sm:gap-6 text-xs sm:text-sm font-medium">
                <button
                  onClick={() => setActiveTab("rec")}
                  className={`px-3 py-1.5 rounded-lg transition-all ${
                    activeTab === "rec"
                      ? "bg-indigo-600/20 text-indigo-400 font-semibold border border-indigo-500/30"
                      : "text-slate-400 hover:text-white"
                  }`}
                >
                  Rec Manager
                </button>
                <button
                  onClick={() => setActiveTab("scripts")}
                  className={`px-3 py-1.5 rounded-lg transition-all ${
                    activeTab === "scripts"
                      ? "bg-cyan-500/20 text-cyan-400 font-semibold border border-cyan-500/30"
                      : "text-slate-400 hover:text-white"
                  }`}
                >
                  Scripts
                </button>
                <button
                  onClick={() => setActiveTab("roleplay")}
                  className={`px-3 py-1.5 rounded-lg transition-all ${
                    activeTab === "roleplay"
                      ? "bg-emerald-500/20 text-emerald-400 font-semibold border border-emerald-500/30"
                      : "text-slate-400 hover:text-white"
                  }`}
                >
                  Roleplay Clips
                </button>
              </div>

              {/* Discord ID Button */}
              <button
                onClick={copyDiscord}
                className="hidden md:flex items-center gap-2 bg-slate-900 hover:bg-slate-800 border border-slate-700/60 px-3.5 py-1.5 rounded-xl text-xs font-mono text-slate-200 transition-all hover:border-indigo-500/50"
              >
                <span className="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
                <span className="text-slate-400">DC ID:</span>
                <span className="text-indigo-400 font-bold">rareplayz1</span>
              </button>
            </div>
          </nav>

          {/* Hero Header */}
          <section className="relative py-12 sm:py-16 border-b border-slate-800/60 bg-gradient-to-b from-slate-900/40 via-brandDark to-brandDark">
            <div className="max-w-6xl mx-auto px-4">
              <div className="flex flex-col md:flex-row md:items-center justify-between gap-6">
                <div>
                  <h1 className="text-4xl sm:text-6xl font-black text-white tracking-tight mb-3">
                    Rareplayz
                  </h1>
                  <p className="text-slate-400 text-sm sm:text-base max-w-2xl font-normal leading-relaxed">
                    Recording Manager, Content & Gaming Scriptwriter, and Dedicated Roleplayer.
                  </p>

                  {/* Role Badges */}
                  <div className="flex flex-wrap items-center gap-2 mt-4">
                    <span className="inline-flex items-center gap-1.5 px-3 py-1 rounded-lg text-xs font-semibold bg-indigo-500/10 text-indigo-400 border border-indigo-500/20">
                      <span>🎬</span> Recording Manager
                    </span>
                    <span className="inline-flex items-center gap-1.5 px-3 py-1 rounded-lg text-xs font-semibold bg-cyan-500/10 text-cyan-400 border border-cyan-500/20">
                      <span>✍️</span> Scriptwriter
                    </span>
                    <span className="inline-flex items-center gap-1.5 px-3 py-1 rounded-lg text-xs font-semibold bg-emerald-500/10 text-emerald-400 border border-emerald-500/20">
                      <span>🎭</span> Roleplayer
                    </span>
                  </div>
                </div>

                {/* Mobile & Desktop Discord CTA Card */}
                <div className="bg-cardBg border border-slate-800 p-5 rounded-2xl md:min-w-[260px] flex flex-col justify-between shadow-xl">
                  <div>
                    <span className="text-[10px] font-mono text-slate-400 uppercase tracking-wider block mb-1">
                      Direct Contact
                    </span>
                    <div className="flex items-center gap-2 text-white font-mono font-bold text-base mb-3">
                      <span className="text-indigo-400">rareplayz1</span>
                    </div>
                  </div>
                  <button
                    onClick={copyDiscord}
                    className="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold text-xs py-2.5 px-4 rounded-xl transition-all shadow-lg shadow-indigo-600/20 flex items-center justify-center gap-2"
                  >
                    <span>📋</span> Copy Discord ID
                  </button>
                </div>
              </div>
            </div>
          </section>

          {/* About Me Banner */}
          <section className="py-8 bg-slate-950/60 border-b border-slate-800/60">
            <div className="max-w-6xl mx-auto px-4">
              <div className="bg-cardBg/80 border border-slate-800 p-6 rounded-2xl">
                <h2 className="text-xs font-mono font-bold uppercase tracking-wider text-indigo-400 mb-2">
                  About Me
                </h2>
                <p className="text-slate-300 text-sm sm:text-base leading-relaxed">
                  I am Rareplayz, a dedicated community builder, creative scriptwriter, and immersive roleplayer. Whether scaling a community from the ground up, writing high-retention video scripts, or bringing complex characters to life on screen, I bring consistency, creativity, and professionalism to every project.
                </p>
              </div>
            </div>
          </section>

          {/* Main Content */}
          <main className="max-w-6xl mx-auto px-4 py-10 flex-grow w-full">
            
            {/* SECTION 1: RECORDING MANAGER */}
            {activeTab === "rec" && (
              <div className="space-y-8 animate-fadeIn">
                <div className="border-b border-slate-800 pb-4">
                  <span className="text-xs font-mono uppercase text-indigo-400 tracking-wider">Operational Pillar 1</span>
                  <h2 className="text-2xl sm:text-3xl font-bold text-white mt-1">
                    Recording (Rec) Manager
                  </h2>
                  <p className="text-xs sm:text-sm text-slate-400 mt-1">
                    Managing recording sessions, multi-angle POV syncing, content schedules, and crew coordination.
                  </p>
                </div>

                <div className="bg-cardBg border border-slate-800 p-6 sm:p-8 rounded-2xl">
                  <h3 className="text-lg font-bold text-white mb-3">Core Role Description</h3>
                  <p className="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    As a Recording Manager, my focus is driving sustainable, high-quality community growth and maintaining a positive server culture. I specialize in targeted talent scouting, smooth onboarding systems, and building active teams that keep communities thriving long-term.
                  </p>

                  <div className="grid grid-cols-1 md:grid-cols-2 gap-5 pt-4 border-t border-slate-800">
                    <div className="bg-brandDark/80 p-5 rounded-xl border border-slate-800/80 hover:border-indigo-500/40 transition-all">
                      <div className="flex items-center gap-2 mb-2">
                        <span className="p-1.5 rounded-lg bg-indigo-500/10 text-indigo-400 text-sm font-bold">01</span>
                        <h4 className="text-sm font-bold text-white">Strategic Outreach & Scouting</h4>
                      </div>
                      <p className="text-xs text-slate-400 leading-relaxed">
                        Identifying and attracting active creators, skilled staff, and dedicated members without relying on spam.
                      </p>
                    </div>

                    <div className="bg-brandDark/80 p-5 rounded-xl border border-slate-800/80 hover:border-cyan-500/40 transition-all">
                      <div className="flex items-center gap-2 mb-2">
                        <span className="p-1.5 rounded-lg bg-cyan-500/10 text-cyan-400 text-sm font-bold">02</span>
                        <h4 className="text-sm font-bold text-white">Streamlined Onboarding</h4>
                      </div>
                      <p className="text-xs text-slate-400 leading-relaxed">
                        Setting up welcoming application processes, clear guidelines, and structured interviews so new recruits feel valued from day one.
                      </p>
                    </div>

                    <div className="bg-brandDark/80 p-5 rounded-xl border border-slate-800/80 hover:border-emerald-500/40 transition-all">
                      <div className="flex items-center gap-2 mb-2">
                        <span className="p-1.5 rounded-lg bg-emerald-500/10 text-emerald-400 text-sm font-bold">03</span>
                        <h4 className="text-sm font-bold text-white">Team Coordination</h4>
                      </div>
                      <p className="text-xs text-slate-400 leading-relaxed">
                        Working closely with server admins and department heads to fill roster gaps quickly and keep daily operations running smoothly.
                      </p>
                    </div>

                    <div className="bg-brandDark/80 p-5 rounded-xl border border-slate-800/80 hover:border-amber-500/40 transition-all">
                      <div className="flex items-center gap-2 mb-2">
                        <span className="p-1.5 rounded-lg bg-amber-500/10 text-amber-400 text-sm font-bold">04</span>
                        <h4 className="text-sm font-bold text-white">Community Retention</h4>
                      </div>
                      <p className="text-xs text-slate-400 leading-relaxed">
                        Fostering a safe, engaging environment that lowers member churn and keeps chat active.
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            )}

            {/* SECTION 2: SCRIPT WRITING */}
            {activeTab === "scripts" && (
              <div className="space-y-6 animate-fadeIn">
                <div className="border-b border-slate-800 pb-4 flex flex-col md:flex-row md:items-center justify-between gap-4">
                  <div>
                    <span className="text-xs font-mono uppercase text-cyan-400 tracking-wider">Operational Pillar 2</span>
                    <h2 className="text-2xl sm:text-3xl font-bold text-white mt-1">
                      Script Writing Showcase
                    </h2>
                    <p className="text-xs sm:text-sm text-slate-400 mt-1">
                      High-retention storytelling, character dialogue, pacing hooks, and narrative climaxes.
                    </p>
                  </div>

                  {/* Script Selector Tabs */}
                  <div className="flex gap-2">
                    <button
                      onClick={() => setSelectedScript("script1")}
                      className={`px-4 py-2 rounded-xl text-xs font-bold transition-all border ${
                        selectedScript === "script1"
                          ? "bg-cyan-500 text-black border-cyan-400 shadow-lg shadow-cyan-500/20"
                          : "bg-cardBg text-slate-300 border-slate-800 hover:border-slate-700"
                      }`}
                    >
                      Script 1: Glitch Bow Heist
                    </button>
                    <button
                      onClick={() => setSelectedScript("script2")}
                      className={`px-4 py-2 rounded-xl text-xs font-bold transition-all border ${
                        selectedScript === "script2"
                          ? "bg-cyan-500 text-black border-cyan-400 shadow-lg shadow-cyan-500/20"
                          : "bg-cardBg text-slate-300 border-slate-800 hover:border-slate-700"
                      }`}
                    >
                      Script 2: Joined Haters' SMP
                    </button>
                  </div>
                </div>

                {/* Script Display Terminal */}
                <div className="bg-cardBg border border-slate-800 rounded-2xl overflow-hidden shadow-2xl">
                  <div className="p-4 bg-slate-950/80 border-b border-slate-800 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <div>
                      <h3 className="text-sm font-bold text-white">{currentScript.title}</h3>
                      <p className="text-xs text-slate-400">{currentScript.description}</p>
                    </div>

                    <button
                      onClick={() => {
                        const fullText = currentScript.content.map(c => {
                          if (c.type === "scene") return `\n${c.text}\n`;
                          if (c.type === "narration") return `[NARRATION] ${c.text}`;
                          return `${c.speaker}: ${c.text}`;
                        }).join("\n\n");
                        if (navigator.clipboard && navigator.clipboard.writeText) {
                          navigator.clipboard.writeText(fullText);
                        } else {
                          const textArea = document.createElement("textarea");
                          textArea.value = fullText;
                          document.body.appendChild(textArea);
                          textArea.select();
                          document.execCommand('copy');
                          document.body.removeChild(textArea);
                        }
                        showToast("Script copied to clipboard!");
                      }}
                      className="self-start sm:self-auto bg-slate-900 hover:bg-slate-800 text-slate-300 text-xs px-3 py-1.5 rounded-lg border border-slate-700 flex items-center gap-1.5 transition-all"
                    >
                      <span>📋</span> Copy Script Text
                    </button>
                  </div>

                  {/* Formatted Script Body */}
                  <div className="p-6 max-h-[650px] overflow-y-auto custom-scrollbar bg-brandDark/50 space-y-4 font-sans text-xs sm:text-sm">
                    {currentScript.content.map((item, idx) => {
                      if (item.type === "scene") {
                        return (
                          <div key={idx} className="my-6 text-center">
                            <span className="inline-block bg-indigo-500/10 border border-indigo-500/30 text-indigo-400 font-mono text-xs px-4 py-1.5 rounded-full font-bold">
                              {item.text}
                            </span>
                          </div>
                        );
                      }

                      if (item.type === "narration") {
                        return (
                          <div key={idx} className="my-3 bg-slate-900/60 border-l-2 border-slate-600 p-3.5 rounded-r-xl italic text-slate-300 text-xs sm:text-sm leading-relaxed whitespace-pre-line">
                            {item.text}
                          </div>
                        );
                      }

                      const isMainChar = item.speaker === "SENPAISPIDER";
                      return (
                        <div key={idx} className={`p-4 rounded-xl border ${
                          isMainChar 
                            ? "bg-slate-900/90 border-indigo-500/30 ml-0 sm:ml-2" 
                            : "bg-slate-950/70 border-slate-800 mr-0 sm:mr-4"
                        }`}>
                          <div className="flex items-center gap-2 mb-1.5">
                            <span className={`text-xs font-mono font-bold px-2 py-0.5 rounded ${
                              isMainChar 
                                ? "bg-indigo-500/20 text-indigo-400 border border-indigo-500/30" 
                                : "bg-cyan-500/20 text-cyan-400 border border-cyan-500/30"
                            }`}>
                              {item.speaker}
                            </span>
                          </div>
                          <p className="text-slate-200 leading-relaxed">
                            {item.text}
                          </p>
                        </div>
                      );
                    })}
                  </div>
                </div>
              </div>
            )}

            {/* SECTION 3: ROLEPLAY SHOWCASE */}
            {activeTab === "roleplay" && (
              <div className="space-y-6 animate-fadeIn">
                <div className="border-b border-slate-800 pb-4">
                  <span className="text-xs font-mono uppercase text-emerald-400 tracking-wider">Operational Pillar 3</span>
                  <h2 className="text-2xl sm:text-3xl font-bold text-white mt-1">
                    Roleplay Showcase
                  </h2>
                  <p className="text-xs sm:text-sm text-slate-400 mt-1">
                    Improvisation, high-stakes dialogue, dynamic character interactions, and server storyline arcs.
                  </p>
                </div>

                <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
                  {videos.map((vid) => (
                    <div 
                      key={vid.id} 
                      className="bg-cardBg border border-slate-800 rounded-2xl p-5 flex flex-col justify-between hover:border-emerald-500/40 transition-all shadow-xl"
                    >
                      <div>
                        {/* Video Frame Placeholder */}
                        <div className="w-full aspect-video bg-slate-950 rounded-xl border border-slate-800 flex flex-col items-center justify-center p-4 text-center mb-4 relative overflow-hidden group">
                          <span className="text-3xl mb-2 group-hover:scale-110 transition-transform">🎭</span>
                          <span className="text-xs font-bold text-white mb-2">{vid.title}</span>
                          
                          {vid.url ? (
                            <a
                              href={vid.url}
                              target="_blank"
                              rel="noopener noreferrer"
                              className="text-xs font-bold bg-emerald-500 hover:bg-emerald-400 text-black px-4 py-1.5 rounded-lg transition-all shadow-lg shadow-emerald-500/20 flex items-center gap-1"
                            >
                              <span>▶</span> Play Video
                            </a>
                          ) : (
                            <span className="text-[11px] text-slate-500 font-mono bg-slate-900 px-2.5 py-1 rounded border border-slate-800">
                              No URL Added Yet
                            </span>
                          )}
                        </div>

                        <div className="flex items-center justify-between mb-2">
                          <h3 className="font-bold text-white text-base">{vid.title}</h3>
                          <span className="text-[10px] font-mono bg-emerald-500/10 text-emerald-400 border border-emerald-500/20 px-2 py-0.5 rounded-full font-semibold">
                            {vid.category}
                          </span>
                        </div>
                        
                        <p className="text-xs text-slate-400 leading-relaxed mb-4">
                          {vid.focus}
                        </p>
                      </div>

                      {/* Link Editor */}
                      <div className="pt-3 border-t border-slate-800 flex items-center justify-between">
                        {editingVideoId === vid.id ? (
                          <div className="flex gap-1.5 items-center w-full">
                            <input
                              type="text"
                              placeholder="Paste video URL"
                              value={tempUrl}
                              onChange={(e) => setTempUrl(e.target.value)}
                              className="w-full bg-slate-950 text-xs text-white p-2 rounded-lg border border-slate-700 outline-none focus:border-emerald-500"
                            />
                            <button
                              onClick={() => handleSaveVideoUrl(vid.id)}
                              className="bg-emerald-500 text-black text-xs font-bold px-3 py-2 rounded-lg hover:bg-emerald-400 shrink-0"
                            >
                              Save
                            </button>
                          </div>
                        ) : (
                          <div className="flex items-center justify-between w-full">
                            <span className="text-[10px] font-mono text-slate-500 uppercase">
                              {vid.url ? "Link Ready" : "Empty Slot"}
                            </span>
                            <button
                              onClick={() => {
                                setEditingVideoId(vid.id);
                                setTempUrl(vid.url);
                              }}
                              className="text-xs font-semibold text-emerald-400 hover:underline flex items-center gap-1"
                            >
                              <span>✏️</span> {vid.url ? "Edit Link" : "+ Add Video URL"}
                            </button>
                          </div>
                        )}
                      </div>
                    </div>
                  ))}
                </div>
              </div>
            )}

          </main>

          {/* Footer */}
          <footer className="border-t border-slate-800/80 bg-slate-950 py-10 mt-12">
            <div className="max-w-6xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-6">
              <div>
                <h3 className="text-lg font-black text-white tracking-tight">Rareplayz</h3>
                <p className="text-xs text-slate-400">Recording Manager | Scriptwriter | Roleplayer</p>
              </div>

              <div className="flex items-center gap-3 bg-cardBg px-4 py-2.5 rounded-xl border border-slate-800 shadow-xl">
                <span className="text-xs text-slate-400 font-mono">Discord:</span>
                <code className="text-xs font-bold text-indigo-400 font-mono">rareplayz1</code>
                <button
                  onClick={copyDiscord}
                  className="text-xs bg-indigo-600 hover:bg-indigo-500 text-white px-3 py-1 rounded-lg font-semibold transition-all shadow-md shadow-indigo-600/20"
                >
                  Copy ID
                </button>
              </div>
            </div>
          </footer>

        </div>
      );
    }

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
