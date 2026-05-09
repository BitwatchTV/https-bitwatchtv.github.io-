export default function UnapayCryptoDashboard() { const stats = [ { title: 'UPAY Price', value: '$0.0124', change: '+12.4%', }, { title: 'Market Cap', value: '$18.2M', change: '+8.7%', }, { title: 'Wallet Users', value: '142K+', change: '+24%', }, { title: 'Transactions', value: '1.2M+', change: '+17%', }, ];

const ecosystem = [ { title: 'UMWallet', desc: 'Secure wallet & UPAY transfers', icon: '💳', }, { title: 'Bookify', desc: 'Marketplace & creator economy', icon: '📚', }, { title: 'Bitflix', desc: 'Streaming & rewards platform', icon: '🎬', }, { title: 'Umpanalo', desc: 'Gaming rewards ecosystem', icon: '🎮', }, ];

return ( <div className="min-h-screen bg-[#020817] text-white overflow-hidden"> <div className="absolute inset-0 bg-[radial-gradient(circle_at_top,rgba(0,255,255,0.15),transparent_35%)]"></div>

{/* SIDEBAR */}
  <div className="fixed left-0 top-0 h-full w-24 bg-black/40 backdrop-blur-2xl border-r border-cyan-400/10 hidden lg:flex flex-col items-center py-8 z-50">
    <div className="w-14 h-14 rounded-2xl bg-cyan-400 flex items-center justify-center text-black font-black text-2xl mb-10">
      U
    </div>

    <div className="flex flex-col gap-5 text-center">
      {['🏠', '💳', '📈', '🎮', '📚', '⚙️'].map((icon, index) => (
        <button
          key={index}
          className="w-14 h-14 rounded-2xl bg-white/5 border border-white/10 hover:border-cyan-400/40 hover:bg-cyan-400/10 transition text-2xl"
        >
          {icon}
        </button>
      ))}
    </div>
  </div>

  <div className="lg:ml-24">
    {/* HEADER */}
    <header className="sticky top-0 z-40 backdrop-blur-xl bg-black/30 border-b border-cyan-400/10 px-6 lg:px-10 py-5">
      <div className="flex flex-wrap items-center justify-between gap-4">
        <div>
          <h1 className="text-3xl font-black text-cyan-300">
            🚀 UNAPAY Dashboard
          </h1>
          <p className="text-gray-400 text-sm">
            Premium Crypto Ecosystem Interface
          </p>
        </div>

        <div className="flex items-center gap-4">
          <button className="px-5 py-3 rounded-2xl bg-white/5 border border-white/10 text-gray-300 hover:border-cyan-400/40 transition">
            Connect Wallet
          </button>

          <div className="w-12 h-12 rounded-2xl bg-cyan-400 flex items-center justify-center text-black font-black">
            U
          </div>
        </div>
      </div>
    </header>

    {/* MAIN */}
    <main className="relative z-10 px-6 lg:px-10 py-10 space-y-10">
      {/* HERO */}
      <section className="grid lg:grid-cols-3 gap-8">
        <div className="lg:col-span-2 bg-gradient-to-br from-cyan-500/20 to-blue-500/10 border border-cyan-400/20 rounded-[36px] p-10 relative overflow-hidden">
          <div className="absolute top-0 right-0 w-72 h-72 bg-cyan-400/20 rounded-full blur-3xl"></div>

          <div className="relative z-10">
            <div className="inline-flex px-4 py-2 rounded-full bg-cyan-400/10 border border-cyan-400/20 text-cyan-300 text-sm mb-6">
              GLOBAL BLOCKCHAIN ECOSYSTEM
            </div>

            <h2 className="text-5xl lg:text-6xl font-black leading-tight mb-6 max-w-3xl">
              Building the Future of UPAY Utility 💎
            </h2>

            <p className="text-gray-300 text-lg leading-relaxed mb-10 max-w-2xl">
              Gaming rewards, marketplace economy, wallet payments, streaming services, and crypto trading in one ecosystem.
            </p>

            <div className="flex flex-wrap gap-4">
              <button className="px-8 py-4 rounded-2xl bg-cyan-400 text-black font-black hover:scale-105 transition">
                JOIN ECOSYSTEM
              </button>

              <button className="px-8 py-4 rounded-2xl border border-cyan-400 text-cyan-300 hover:bg-cyan-400/10 transition">
                VIEW ROADMAP
              </button>
            </div>
          </div>
        </div>

        {/* WALLET CARD */}
        <div className="bg-white/5 border border-cyan-400/10 rounded-[36px] p-8 backdrop-blur-xl">
          <div className="flex items-center justify-between mb-8">
            <div>
              <p className="text-gray-400 text-sm">Total Balance</p>
              <h3 className="text-4xl font-black text-cyan-300">2,458,920</h3>
            </div>

            <div className="w-16 h-16 rounded-full bg-cyan-400 flex items-center justify-center text-black font-black text-2xl">
              U
            </div>
          </div>

          <div className="space-y-5">
            <div className="bg-black/30 border border-white/10 rounded-3xl p-5">
              <p className="text-gray-400 text-sm mb-2">Token Supply</p>
              <h4 className="text-2xl font-black">21B UPAY</h4>
            </div>

            <div className="bg-black/30 border border-white/10 rounded-3xl p-5">
              <p className="text-gray-400 text-sm mb-2">Wallet Status</p>
              <h4 className="text-2xl font-black text-cyan-300">
                ACTIVE
              </h4>
            </div>

            <button className="w-full py-4 rounded-2xl bg-cyan-400 text-black font-black hover:scale-105 transition">
              SEND UPAY
            </button>
          </div>
        </div>
      </section>

      {/* STATS */}
      <section className="grid md:grid-cols-2 xl:grid-cols-4 gap-6">
        {stats.map((card) => (
          <div
            key={card.title}
            className="bg-white/5 border border-white/10 rounded-[30px] p-7 backdrop-blur-xl hover:border-cyan-400/30 transition"
          >
            <p className="text-gray-400 text-sm mb-3">{card.title}</p>
            <h3 className="text-4xl font-black mb-3">{card.value}</h3>
            <span className="text-cyan-300 font-semibold">{card.change}</span>
          </div>
        ))}
      </section>

      {/* CHARTS + ACTIVITY */}
      <section className="grid lg:grid-cols-3 gap-8">
        <div className="lg:col-span-2 bg-white/5 border border-white/10 rounded-[36px] p-8 backdrop-blur-xl">
          <div className="flex items-center justify-between mb-10">
            <div>
              <h3 className="text-3xl font-black mb-2">📈 UPAY Market Analytics</h3>
              <p className="text-gray-400">Real-time ecosystem growth</p>
            </div>

            <button className="px-5 py-2 rounded-xl bg-cyan-400/10 border border-cyan-400/20 text-cyan-300">
              Live
            </button>
          </div>

          <div className="h-80 rounded-[30px] bg-black/30 border border-white/5 p-6 flex items-end gap-4 overflow-hidden">
            {[25, 38, 44, 52, 47, 68, 74, 80, 72, 95, 100].map((height, index) => (
              <div
                key={index}
                className="flex-1 rounded-t-3xl bg-gradient-to-t from-cyan-500 to-cyan-300 shadow-lg shadow-cyan-400/30"
                style={{ height: `${height}%` }}
              ></div>
            ))}
          </div>
        </div>

        <div className="bg-white/5 border border-white/10 rounded-[36px] p-8 backdrop-blur-xl">
          <h3 className="text-3xl font-black mb-8">⚡ Live Activity</h3>

          <div className="space-y-5">
            {[
              'UPAY transferred via UMWallet',
              'New user joined Bookify',
              'Gaming rewards distributed',
              'Marketplace sale completed',
              'Bitflix subscription activated',
            ].map((item, index) => (
              <div
                key={index}
                className="flex items-start gap-4 bg-black/20 border border-white/5 rounded-2xl p-4"
              >
                <div className="w-3 h-3 rounded-full bg-cyan-400 mt-2"></div>
                <div>
                  <p className="text-gray-200">{item}</p>
                  <span className="text-gray-500 text-sm">Just now</span>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* ECOSYSTEM */}
      <section>
        <div className="flex items-center justify-between mb-10">
          <div>
            <h2 className="text-4xl font-black mb-2">🌐 Ecosystem Platforms</h2>
            <p className="text-gray-400">
              Connected applications powered by UPAY
            </p>
          </div>
        </div>

        <div className="grid md:grid-cols-2 xl:grid-cols-4 gap-8">
          {ecosystem.map((item) => (
            <div
              key={item.title}
              className="bg-white/5 border border-white/10 rounded-[32px] p-8 backdrop-blur-xl hover:scale-105 hover:border-cyan-400/30 transition"
            >
              <div className="text-6xl mb-6">{item.icon}</div>

              <h3 className="text-3xl font-black text-cyan-300 mb-4">
                {item.title}
              </h3>

              <p className="text-gray-400 leading-relaxed mb-8">
                {item.desc}
              </p>

              <button className="w-full py-3 rounded-2xl bg-cyan-400/10 border border-cyan-400/20 text-cyan-300 hover:bg-cyan-400/20 transition">
                Open Platform
              </button>
            </div>
          ))}
        </div>
      </section>
    </main>
  </div>
</div>

); }