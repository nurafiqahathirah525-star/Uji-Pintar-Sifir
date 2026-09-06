<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pintar Sifir by TZ Edu Kids</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- React & ReactDOM -->
    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <!-- Babel for JSX -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; -webkit-tap-highlight-color: transparent; }
        @media print {
            body { background: white; -webkit-print-color-adjust: exact; print-color-adjust: exact; }
            .no-print { display: none !important; }
        }
    </style>
</head>
<body class="bg-slate-100">
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;

        function App() {
            const [view, setView] = useState('home');
            const [name, setName] = useState(() => localStorage.getItem('ps_name') || '');
            const [sifir, setSifir] = useState(2);
            const [score, setScore] = useState(0);
            const [qIndex, setQIndex] = useState(0);
            const [timeLeft, setTimeLeft] = useState(60);
            const [questions, setQuestions] = useState([]);
            const [answered, setAnswered] = useState(false);
            const [selectedAns, setSelectedAns] = useState(null);

            // Simpan nama dalam memori telefon
            useEffect(() => { localStorage.setItem('ps_name', name); }, [name]);

            const startGame = (selected) => {
                setSifir(selected);
                let qs = [];
                // Jana 10 soalan
                for(let i=0; i<10; i++){
                    let multiplier = Math.floor(Math.random() * 12) + 1;
                    let ans = selected * multiplier;
                    let options = [ans];
                    while(options.length < 4){
                        let wrong = ans + (Math.floor(Math.random() * 20) - 10);
                        if(wrong > 0 && !options.includes(wrong)) options.push(wrong);
                    }
                    options.sort(() => Math.random() - 0.5);
                    qs.push({ q: `${selected} × ${multiplier}`, ans, options });
                }
                setQuestions(qs);
                setScore(0);
                setQIndex(0);
                setTimeLeft(60);
                setAnswered(false);
                setView('quiz');
            };

            useEffect(() => {
                if(view !== 'quiz' || answered) return;
                if(timeLeft <= 0) {
                    handleAnswer(-1); // Masa tamat
                    return;
                }
                const timer = setInterval(() => setTimeLeft(t => t - 1), 1000);
                return () => clearInterval(timer);
            }, [timeLeft, view, answered]);

            const handleAnswer = (opt) => {
                if(answered) return;
                setAnswered(true);
                setSelectedAns(opt);
                if(opt === questions[qIndex].ans) setScore(s => s + 1);
                
                setTimeout(() => {
                    if(qIndex < 9) {
                        setQIndex(q => q + 1);
                        setTimeLeft(60);
                        setAnswered(false);
                        setSelectedAns(null);
                    } else {
                        setView('result');
                    }
                }, 1500);
            };

            if(view === 'home') return (
                <div className="min-h-screen flex flex-col items-center justify-center p-4">
                    <div className="bg-white p-6 w-full max-w-md rounded-3xl shadow-xl text-center">
                        <div className="bg-blue-900 text-white py-2 px-4 rounded-full inline-block font-bold mb-4 text-sm tracking-widest">TZ EDU KIDS</div>
                        <h1 className="text-4xl font-black text-blue-600 mb-6">PINTAR SIFIR</h1>
                        
                        <input 
                            type="text" 
                            placeholder="Sila Masukkan Nama Anda" 
                            className="w-full p-4 border-2 border-gray-200 rounded-xl mb-6 text-center font-bold text-lg focus:border-blue-500 focus:outline-none" 
                            value={name} 
                            onChange={e => setName(e.target.value.toUpperCase())} 
                        />
                        
                        <h2 className="text-gray-500 font-bold mb-4">PILIH SIFIR UNTUK MULA:</h2>
                        <div className="grid grid-cols-4 gap-3 mb-4">
                            {[2,3,4,5,6,7,8,9,10,11,12].map(num => (
                                <button 
                                    key={num} 
                                    onClick={() => startGame(num)} 
                                    disabled={!name} 
                                    className={`p-3 rounded-xl font-black text-xl shadow-sm transition-transform active:scale-95 ${name ? 'bg-blue-100 text-blue-700 hover:bg-blue-600 hover:text-white border-b-4 border-blue-200' : 'bg-gray-100 text-gray-300'}`}
                                >
                                    {num}
                                </button>
                            ))}
                        </div>
                        {!name && <p className="text-red-500 text-sm font-semibold animate-pulse">Sila masukkan nama untuk mula</p>}
                    </div>
                </div>
            );

            if(view === 'quiz') return (
                <div className="min-h-screen flex flex-col items-center justify-center p-4">
                    <div className="bg-white p-6 w-full max-w-md rounded-3xl shadow-xl text-center">
                        <div className="flex justify-between items-center mb-8">
                            <span className="bg-gray-100 text-gray-600 px-4 py-2 rounded-full font-bold text-sm">Soalan {qIndex + 1}/10</span>
                            <span className={`font-bold px-4 py-2 rounded-full text-sm ${timeLeft < 11 ? 'bg-red-100 text-red-600 animate-pulse' : 'bg-green-100 text-green-700'}`}>⏱️ {timeLeft} Saat</span>
                        </div>
                        
                        <h2 className="text-6xl font-black text-gray-800 mb-10 tracking-wider">{questions[qIndex].q}</h2>
                        
                        <div className="grid grid-cols-2 gap-4">
                            {questions[qIndex].options.map((opt, i) => {
                                let btnStyle = "bg-white border-2 border-gray-200 text-gray-700 hover:bg-blue-50 shadow-sm";
                                if(answered) {
                                    if(opt === questions[qIndex].ans) btnStyle = "bg-green-500 border-green-600 text-white scale-105 shadow-md";
                                    else if(opt === selectedAns) btnStyle = "bg-red-500 border-red-600 text-white scale-95 opacity-50";
                                    else btnStyle = "opacity-50 border-gray-200 text-gray-400";
                                }
                                return (
                                    <button 
                                        key={i} 
                                        onClick={() => handleAnswer(opt)} 
                                        className={`p-6 rounded-2xl text-3xl font-black transition-all duration-200 ${btnStyle}`}
                                    >
                                        {opt}
                                    </button>
                                );
                            })}
                        </div>
                        {answered && timeLeft <= 0 && <p className="text-red-500 font-bold mt-6">Masa Tamat!</p>}
                    </div>
                </div>
            );

            if(view === 'result') return (
                <div className="min-h-screen flex flex-col items-center justify-center p-4">
                    <div className="bg-white p-8 w-full max-w-md rounded-3xl shadow-xl text-center">
                        <h2 className="text-2xl font-bold text-gray-700 mb-2">Tamat! Tahniah, {name} 🎉</h2>
                        <p className="text-gray-500 mb-6 font-semibold">Ujian Sifir {sifir}</p>
                        
                        <div className="relative mb-8 inline-block">
                            <svg className="w-40 h-40 transform -rotate-90">
                                <circle cx="80" cy="80" r="70" stroke="#f3f4f6" strokeWidth="12" fill="none" />
                                <circle cx="80" cy="80" r="70" stroke={score >= 8 ? "#10b981" : score >= 5 ? "#f59e0b" : "#ef4444"} strokeWidth="12" fill="none" strokeDasharray="440" strokeDashoffset={440 - (440 * (score * 10)) / 100} className="transition-all duration-1000" />
                            </svg>
                            <div className="absolute inset-0 flex flex-col items-center justify-center">
                                <span className="text-4xl font-black">{score * 10}%</span>
                            </div>
                        </div>

                        <p className="text-lg font-bold mb-8 text-gray-600">
                            {score === 10 ? "Hebat! Markah Penuh! 🌟" : score >= 5 ? "Bagus! Teruskan Usaha! 👍" : "Jangan putus asa, cuba lagi! 🌱"}
                        </p>

                        <div className="flex flex-col gap-3">
                            {score >= 5 && (
                                <button onClick={() => setView('cert')} className="w-full bg-yellow-400 hover:bg-yellow-500 text-yellow-900 font-black p-4 rounded-xl transition-all shadow-sm active:scale-95">
                                    🎓 LIHAT SIJIL PENCAPAIAN
                                </button>
                            )}
                            <button onClick={() => setView('home')} className="w-full bg-blue-600 hover:bg-blue-700 text-white font-black p-4 rounded-xl transition-all shadow-sm active:scale-95">
                                🏠 KEMBALI KE MENU
                            </button>
                        </div>
                    </div>
                </div>
            );

            if(view === 'cert') return (
                <div className="min-h-screen flex flex-col items-center bg-gray-100 md:p-8">
                    <div className="no-print flex w-full max-w-2xl justify-between p-4 bg-white md:bg-transparent shadow-sm md:shadow-none mb-4 sticky top-0 z-10">
                        <button onClick={() => setView('result')} className="bg-gray-200 text-gray-700 font-bold px-5 py-2 rounded-lg active:scale-95">⬅️ Kembali</button>
                        <button onClick={() => window.print()} className="bg-blue-600 text-white font-bold px-5 py-2 rounded-lg active:scale-95">🖨️ Cetak / Simpan PDF</button>
                    </div>
                    
                    {/* Sijil A4 Format */}
                    <div className="bg-white w-full max-w-[210mm] aspect-[1/1.414] p-8 md:p-16 shadow-2xl relative border-[16px] border-double border-blue-900 flex flex-col items-center justify-center text-center">
                        <div className="absolute inset-2 border-2 border-yellow-500"></div>
                        
                        <div className="bg-blue-900 text-white py-2 px-6 rounded-full font-black text-sm tracking-widest mb-8">TZ EDU KIDS</div>
                        
                        <h1 className="text-4xl md:text-5xl font-black text-yellow-600 mb-6 uppercase font-serif">Sijil Pencapaian</h1>
                        
                        <p className="text-gray-700 mb-4 text-lg font-medium">Sijil ini dengan bangganya dianugerahkan kepada</p>
                        
                        <h2 className="text-4xl md:text-5xl font-black text-blue-900 mb-6 font-serif border-b-2 border-gray-300 pb-2 w-full px-4 break-words">
                            {name}
                        </h2>
                        
                        <p className="text-gray-700 text-lg mb-6 font-medium">Kerana telah berjaya melepasi ujian hafalan</p>
                        
                        <h3 className="text-3xl md:text-4xl font-black text-blue-700 mb-8 tracking-wide">PINTAR SIFIR {sifir}</h3>
                        
                        <div className="flex gap-4 items-center mb-12">
                            <div className="bg-yellow-50 px-8 py-4 rounded-2xl border-4 border-yellow-400">
                                <p className="text-sm font-bold text-yellow-700 uppercase mb-1">Skor Diperolehi</p>
                                <span className="text-4xl font-black text-yellow-700">{score * 10}%</span>
                            </div>
                        </div>

                        <div className="mt-auto w-full flex justify-between items-end px-8">
                            <div className="text-center">
                                <div className="border-b-2 border-gray-800 w-32 mb-2"></div>
                                <p className="text-sm font-bold text-gray-600">Tandatangan</p>
                            </div>
                            <div className="text-center">
                                <p className="text-sm font-bold text-gray-600 mb-1">Tarikh Dicetak:</p>
                                <p className="font-bold">{new Date().toLocaleDateString('ms-MY')}</p>
                            </div>
                        </div>
                    </div>
                </div>
            );

            return null;
        }

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>
