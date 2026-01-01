import React, { useState, useEffect } from 'react';
import { Share2, Info, X } from 'lucide-react';

const DailyCardApp = () => {
  const [currentCard, setCurrentCard] = useState(null);
  const [isFlipped, setIsFlipped] = useState(false);
  const [showInfo, setShowInfo] = useState(false);

  // מאגר של 50 מסרים (במציאות אלו יהיו כתובות לתמונות שלך)
  // כדי להשתמש בתמונות אמיתיות, שנה את ה-type ל-'image' ואת ה-content ל-URL
  const cardDeck = Array.from({ length: 50 }, (_, i) => ({
    id: i + 1,
    type: 'text', // שנה ל-'image' אם יש לך קבצים
    content: `מסר מספר ${i + 1}: ${
      [
        "היום זה הזמן להתחלה חדשה",
        "הקשב לאינטואיציה שלך",
        "שחרר את מה שלא משרת אותך",
        "התשובה נמצאת בשקט",
        "צעד קטן יוביל לשינוי גדול",
        "הכל קורה בזמן הנכון",
        "סמוך על התהליך",
        "השפע בדרך אליך",
        "בחר באהבה על פני פחד",
        "אתה בדרך הנכונה",
        "פתח את הלב לאפשרויות חדשות",
        "הסבלנות משתלמת",
        "התמקד בחיובי",
        "היום הוא מתנה",
        "הכוח לשנות נמצא בידיך"
      ][i % 15] // מחזוריות רק לצורך הדגמה
    }`,
    bgColor: [
      "from-purple-500 to-indigo-500",
      "from-pink-500 to-rose-500", 
      "from-blue-400 to-cyan-300",
      "from-emerald-400 to-teal-500",
      "from-amber-400 to-orange-500"
    ][i % 5]
  }));

  useEffect(() => {
    // לוגיקה לבחירת קלף יחיד לכל יום
    const today = new Date();
    // יצירת "זרע" (Seed) ייחודי ליום הנוכחי: YYYYMMDD
    const dateSeed = today.getFullYear() * 10000 + (today.getMonth() + 1) * 100 + today.getDate();
    
    // שימוש במודולו (%) כדי לבחור מספר בין 0 ל-49 שתמיד יהיה זהה באותו תאריך
    const dailyIndex = dateSeed % 50;
    
    setCurrentCard(cardDeck[dailyIndex]);

    // בדיקה האם כבר הפכו את הקלף היום (נשמר בזיכרון הדפדפן)
    const storedDate = localStorage.getItem('lastCardFlipDate');
    const todayString = today.toDateString();

    if (storedDate === todayString) {
      setIsFlipped(true);
    }
  }, []);

  const handleCardClick = () => {
    if (!isFlipped) {
      setIsFlipped(true);
      localStorage.setItem('lastCardFlipDate', new Date().toDateString());
    }
  };

  const shareApp = () => {
    if (navigator.share) {
      navigator.share({
        title: 'הקלף היומי שלי',
        text: currentCard.content,
        url: window.location.href,
      }).catch(console.error);
    } else {
      // Fallback for browsers/views that don't support native share
      alert('המסר הועתק ללוח!');
      navigator.clipboard.writeText(`המסר היומי שלי: ${currentCard.content}`);
    }
  };

  if (!currentCard) return <div className="flex items-center justify-center h-screen bg-gray-900 text-white">טוען...</div>;

  return (
    <div className="min-h-screen bg-gray-900 flex flex-col items-center relative overflow-hidden font-sans" dir="rtl">
      
      {/* אלמנטים עיצוביים ברקע */}
      <div className="absolute top-0 left-0 w-full h-full overflow-hidden z-0 opacity-20 pointer-events-none">
        <div className="absolute top-[-10%] left-[-10%] w-64 h-64 bg-purple-600 rounded-full blur-[100px]"></div>
        <div className="absolute bottom-[-10%] right-[-10%] w-80 h-80 bg-blue-600 rounded-full blur-[100px]"></div>
      </div>

      {/* כותרת */}
      <header className="z-10 mt-8 mb-4 text-center">
        <h1 className="text-3xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-purple-200 to-pink-200 drop-shadow-lg">
          המסר היומי
        </h1>
        <p className="text-gray-400 text-sm mt-1">קלף חדש בכל יום</p>
      </header>

      {/* איזור הקלף */}
      <main className="flex-1 flex flex-col items-center justify-center w-full max-w-md px-6 z-10 mb-12 perspective-1000">
        
        {/* הקונטיינר של הקלף עם אפקט תלת מימד */}
        <div 
          className="relative w-full aspect-[2/3] cursor-pointer group perspective-1000"
          onClick={handleCardClick}
          style={{ perspective: '1000px' }}
        >
          <div 
            className={`w-full h-full transition-all duration-1000 preserve-3d relative ${isFlipped ? 'rotate-y-180' : ''}`}
            style={{ transformStyle: 'preserve-3d', transform: isFlipped ? 'rotateY(180deg)' : 'rotateY(0deg)' }}
          >
            
            {/* צד אחורי (הגב של הקלף) */}
            <div className="absolute w-full h-full backface-hidden rounded-2xl shadow-2xl border-2 border-white/10 bg-gradient-to-br from-indigo-900 to-purple-900 flex flex-col items-center justify-center">
               <div className="w-[90%] h-[90%] border border-white/20 rounded-xl flex items-center justify-center bg-white/5 backdrop-blur-sm">
                  <div className="text-center p-4">
                    <span className="text-6xl mb-4 block">✨</span>
                    <p className="text-white/80 font-medium">לחץ כדי לגלות</p>
                  </div>
               </div>
               {/* אפקט ברק */}
               <div className="absolute inset-0 bg-gradient-to-tr from-transparent via-white/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500 rounded-2xl"></div>
            </div>

            {/* צד קדמי (המסר/התמונה) */}
            <div 
              className="absolute w-full h-full backface-hidden rounded-2xl shadow-2xl overflow-hidden rotate-y-180 bg-white"
              style={{ transform: 'rotateY(180deg)', backfaceVisibility: 'hidden' }}
            >
              {currentCard.type === 'image' ? (
                <img 
                  src={currentCard.content} 
                  alt="Daily Card" 
                  className="w-full h-full object-cover"
                />
              ) : (
                <div className={`w-full h-full flex flex-col items-center justify-center p-8 text-center bg-gradient-to-br ${currentCard.bgColor} text-white`}>
                   <div className="w-full h-full border-2 border-white/30 rounded-xl flex items-center justify-center p-6 bg-black/10 backdrop-blur-sm">
                      <div>
                        <h2 className="text-2xl font-bold mb-4 drop-shadow-md leading-relaxed">
                          {currentCard.content}
                        </h2>
                        <div className="w-16 h-1 bg-white/50 mx-auto rounded-full mt-6"></div>
                      </div>
                   </div>
                </div>
              )}
            </div>
          </div>
        </div>

        {/* הנחיה למשתמש */}
        <div className={`mt-8 transition-opacity duration-500 ${isFlipped ? 'opacity-100' : 'opacity-0'}`}>
           <button 
             onClick={(e) => { e.stopPropagation(); shareApp(); }}
             className="flex items-center gap-2 px-6 py-3 bg-white/10 hover:bg-white/20 backdrop-blur-md rounded-full text-white transition-all active:scale-95"
           >
             <Share2 size={18} />
             <span>שתף את המסר</span>
           </button>
        </div>

      </main>

      {/* כפתור מידע */}
      <button 
        onClick={() => setShowInfo(true)}
        className="absolute top-6 left-6 text-white/50 hover:text-white transition-colors z-20"
      >
        <Info size={24} />
      </button>

      {/* מודל מידע */}
      {showInfo && (
        <div className="absolute inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-sm">
          <div className="bg-gray-800 p-6 rounded-2xl max-w-sm w-full text-white relative border border-white/10 shadow-2xl">
            <button 
              onClick={() => setShowInfo(false)}
              className="absolute top-4 left-4 text-gray-400 hover:text-white"
            >
              <X size={20} />
            </button>
            <h3 className="text-xl font-bold mb-2">אודות</h3>
            <p className="text-gray-300 text-sm leading-relaxed">
              אפליקציה זו בוחרת עבורך קלף מסר אחד מתוך 50 אפשרויות בכל יום. הקלף מתחלף באופן אוטומטי בחצות.
              <br /><br />
              פותח באהבה כדי לתת השראה יומית.
            </p>
          </div>
        </div>
      )}

    </div>
  );
};

export default DailyCardApp;
