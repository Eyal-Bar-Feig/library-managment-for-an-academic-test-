# library-managment-for-an-academic-test-

<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>פרויקט מערכת ניהול ספרייה - חקירה אינטראקטיבית</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Assistant:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Assistant', sans-serif; /* Unified font-family */
            background-color: #f7fafc; /* neutral-100 equivalent */
            color: #2d3748; /* neutral-800 equivalent */
        }
        .tab-active {
            border-color: #0d9488; /* teal-600 */
            color: #0d9488;
            background-color: #f0fdfa; /* teal-50 */
        }
        .tab-inactive {
            border-color: transparent;
            color: #52525b; /* zinc-600 */
        }
        .code-block {
            background-color: #18181b; /* zinc-900 */
            color: #e4e4e7; /* zinc-200 */
            padding: 1rem;
            border-radius: 0.5rem;
            font-family: monospace;
            white-space: pre-wrap;
            word-wrap: break-word;
            font-size: 0.875rem;
            line-height: 1.5;
            direction: ltr; /* Ensure code block is LTR */
            text-align: left; /* Ensure code block is left-aligned */
        }
        .code-keyword { color: #93c5fd; } /* blue-300 */
        .code-class { color: #6ee7b7; } /* emerald-300 */
        .code-string { color: #fde047; } /* yellow-300 */
        .code-comment { color: #a1a1aa; } /* zinc-400 */
        .code-annotation { color: #f9a8d4; } /* pink-300 */
        .code-function { color: #818cf8; } /* indigo-400 */ /* Added color for functions */
        .code-symbol { color: #e4e4e7; } /* zinc-200 */ /* Added color for symbols */

        .highlight-polymorphism { background-color: rgba(253, 224, 71, 0.2); border-left: 3px solid #fde047; padding-left: 5px; } /* Yellow for polymorphism */
        .highlight-inheritance { background-color: rgba(110, 231, 183, 0.2); border-left: 3px solid #6ee7b7; padding-left: 5px; } /* Green for inheritance */
        .highlight-datastructure { background-color: rgba(249, 115, 22, 0.2); border-left: 3px solid #f97316; padding-left: 5px; } /* Orange for data structures */
    </style>
</head>
<body class="bg-neutral-100 text-neutral-800">

    <div class="container mx-auto p-4 md:p-8">
        
        <header class="text-center mb-8">
            <h1 class="text-4xl md:text-5xl font-bold text-teal-700">פרויקט מערכת ניהול ספרייה</h1>
            <p class="text-lg text-neutral-600 mt-2">חקירה אינטראקטיבית של עקרונות תכנות ויישום</p>
        </header>

        <div class="mb-8 border-b border-neutral-300">
            <nav class="flex flex-wrap -mb-px" id="main-tabs">
                <button data-tab="overview" class="tab-active text-lg px-4 py-3 border-b-2 font-semibold transition-colors duration-200">סקירה כללית</button>
                <button data-tab="oop" class="tab-inactive text-lg px-4 py-3 border-b-2 font-semibold transition-colors duration-200">עקרונות OOP</button>
                <button data-tab="data-structures" class="tab-inactive text-lg px-4 py-3 border-b-2 font-semibold transition-colors duration-200">מבני נתונים</button>
                <button data-tab="explorer" class="tab-inactive text-lg px-4 py-3 border-b-2 font-semibold transition-colors duration-200">סייר המחלקות</button>
                <button data-tab="demo" class="tab-inactive text-lg px-4 py-3 border-b-2 font-semibold transition-colors duration-200">הדגמה אינטראקטיבית</button>
            </nav>
        </div>

        <main id="tab-content">
            
            <section id="overview-content" class="space-y-6">
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h2 class="text-2xl font-bold text-teal-600 mb-3">מטרת הפרויקט</h2>
                    <p class="text-lg leading-relaxed">פרויקט זה מדגים יישום בסיסי של מערכת לניהול ספרייה באמצעות עקרונות תכנות מונחה-עצמים (OOP) ושימוש במבני נתונים שונים בשפת Java. המטרה היא להציג כיצד מושגים תיאורטיים באים לידי ביטוי בקוד מעשי, וכיצד ניתן לבנות מערכת מודולרית וניתנת להרחבה.</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h3 class="text-xl font-bold text-neutral-700 mb-3">מה ניתן לחקור באפליקציה זו?</h3>
                    <ul class="list-disc list-inside space-y-2 text-lg">
                        <li><strong>עקרונות OOP:</strong> למד על כימוס, ירושה ופולימורפיזם דרך דוגמאות קוד והסברים ויזואליים.</li>
                        <li><strong>מבני נתונים:</strong> גלה מדוע נבחרו מבני נתונים ספציפיים (מערך, רשימה מקושרת, מפת גיבוב ותור) וכיצד הם פועלים.</li>
                        <li><strong>סייר המחלקות:</strong> צלול לקוד המקור של כל מחלקה בפרויקט.</li>
                        <li><strong>הדגמה אינטראקטיבית:</strong> הפעל סימולציה של המערכת כדי לראות את הלוגיקה בפעולה.</li>
                    </ul>
                </div>
            </section>

            <section id="oop-content" class="hidden space-y-8">
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h2 class="text-2xl font-bold text-teal-600 mb-4">ירושה ופולימורפיזם: היררכיית הספרים</h2>
                    <p class="text-lg mb-6">בלב הפרויקט עומד עקרון הירושה. מחלקת הבסיס `Book` מגדירה תכונות משותפות, ומחלקות הבת `EBook` ו-`AudioBook` יורשות ממנה ומוסיפות התנהגות ייחודית. זה מאפשר לנו להתייחס לכל סוגי הספרים כאל `Book` (פולימורפיזם), מה שמפשט את הקוד.</p>
                    <div class="flex justify-center">
                        <div class="text-center p-4">
                            <div class="bg-blue-100 border-2 border-blue-500 text-blue-800 font-bold p-4 rounded-lg shadow-md w-48">Book</div>
                            <div class="flex justify-center mt-4">
                                <div class="border-l-2 border-b-2 border-blue-500 h-8 w-1/2"></div>
                                <div class="border-r-2 border-b-2 border-blue-500 h-8 w-1/2"></div>
                            </div>
                            <div class="flex justify-around mt-4 space-x-4 rtl:space-x-reverse">
                                <div class="text-center">
                                    <div class="bg-emerald-100 border-2 border-emerald-500 text-emerald-800 font-bold p-4 rounded-lg shadow-md w-48">EBook</div>
                                </div>
                                <div class="text-center">
                                    <div class="bg-purple-100 border-2 border-purple-500 text-purple-800 font-bold p-4 rounded-lg shadow-md w-48">AudioBook</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h2 class="text-2xl font-bold text-teal-600 mb-4">כימוס (Encapsulation)</h2>
                    <p class="text-lg">כל התכונות במחלקות מוגדרות כ-`private`. זה אומר שלא ניתן לגשת אליהן ישירות מחוץ למחלקה. הגישה מתבצעת רק דרך מתודות `public` מסוג `get` (לקריאה) ו-`set` (לכתיבה). עיקרון זה מגן על הנתונים ומבטיח שהשינויים בהם נעשים בצורה מבוקרת.</p>
                </div>
            </section>

            <section id="data-structures-content" class="hidden grid md:grid-cols-2 gap-6">
                   <div class="bg-white p-6 rounded-lg shadow-sm">
                     <h3 class="text-xl font-bold text-neutral-700 mb-2">מערך (Array)</h3>
                     <p class="mb-4"><strong>שימוש:</strong> אחסון כל הספרים (`allBooksArray`).</p>
                     <p><strong>למה נבחר:</strong> מתאים לאוסף שגודלו המקסימלי ידוע מראש. מספק גישה מהירה לפי אינדקס ופשוט למימוש.</p>
                   </div>
                   <div class="bg-white p-6 rounded-lg shadow-sm">
                     <h3 class="text-xl font-bold text-neutral-700 mb-2">רשימה מקושרת (LinkedList)</h3>
                     <p class="mb-4"><strong>שימוש:</strong> ניהול השאלות פעילות (`activeLoans`).</p>
                     <p><strong>למה נבחר:</strong> יעיל מאוד להוספה והסרה של פריטים, פעולות שקורות בתדירות גבוהה במערכת השאלות והחזרות.</p>
                   </div>
                   <div class="bg-white p-6 rounded-lg shadow-sm">
                     <h3 class="text-xl font-bold text-neutral-700 mb-2">מפת גיבוב (HashMap)</h3>
                     <p class="mb-4"><strong>שימוש:</strong> אחסון הקוראים (`readersMap`).</p>
                     <p><strong>למה נבחר:</strong> מאפשר חיפוש מהיר ביותר (כמעט מיידי) של קורא לפי מזהה (ID), מה שחיוני לפעולות השאלה והחזרה.</p>
                   </div>
                   <div class="bg-white p-6 rounded-lg shadow-sm">
                     <h3 class="text-xl font-bold text-neutral-700 mb-2">תור (Queue)</h3>
                     <p class="mb-4"><strong>שימוש:</strong> ניהול רשימת המתנה לספרים (`bookRequestQueue`).</p>
                     <p><strong>למה נבחר:</strong> מבטיח טיפול הוגן בבקשות לפי סדר הגעתן (FIFO - First In, First Out), כך שהראשון שמבקש הוא הראשון שמקבל.</p>
                   </div>
            </section>

            <section id="explorer-content" class="hidden">
                   <div class="flex flex-col md:flex-row gap-6">
                       <div class="w-full md:w-1/4">
                           <div class="bg-white p-4 rounded-lg shadow-sm">
                               <h3 class="text-xl font-bold mb-4">בחר מחלקה:</h3>
                               <div id="class-selector" class="space-y-2">
                                   <button data-class="Book" class="w-full text-right p-2 rounded bg-neutral-200 text-neutral-800 font-semibold">Book.java</button>
                                   <button data-class="EBook" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">EBook.java</button>
                                   <button data-class="AudioBook" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">AudioBook.java</button>
                                   <button data-class="Reader" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">Reader.java</button>
                                   <button data-class="Loan" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">Loan.java</button>
                                   <button data-class="BookRequest" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">BookRequest.java</button>
                                   <button data-class="Library" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">Library.java</button>
                                   <button data-class="Main" class="w-full text-right p-2 rounded hover:bg-neutral-200 transition">Main.java</button>
                               </div>
                           </div>
                       </div>
                       <div class="w-full md:w-3/4">
                           <div class="bg-white p-6 rounded-lg shadow-sm">
                               <h2 id="class-title" class="text-2xl font-bold text-teal-600 mb-2">Book.java</h2>
                               <p id="class-description" class="text-lg mb-4"></p>
                               <div id="class-code" class="code-block"></div>
                           </div>
                       </div>
                   </div>
            </section>

            <section id="demo-content" class="hidden">
                <div class="grid lg:grid-cols-3 gap-6">
                    <div class="lg:col-span-1 bg-white p-6 rounded-lg shadow-sm">
                        <h2 class="text-2xl font-bold text-teal-600 mb-4">לוח בקרה</h2>
                        <div id="demo-controls" class="space-y-3">
                            <button data-action="init" class="w-full bg-teal-600 text-white font-bold py-2 px-4 rounded hover:bg-teal-700 transition">אתחול המערכת</button>
                            <button data-action="borrowGatsby" class="w-full bg-blue-500 text-white font-bold py-2 px-4 rounded hover:bg-blue-600 transition">השאל את 'גטסבי הגדול' (איתי)</button>
                            <button data-action="borrow1984" class="w-full bg-blue-500 text-white font-bold py-2 px-4 rounded hover:bg-blue-600 transition">השאל את '1984' (שרה)</button>
                            <button data-action="queue1984" class="w-full bg-yellow-500 text-white font-bold py-2 px-4 rounded hover:bg-yellow-600 transition">נסה להשאיל את '1984' (איתי)</button>
                            <button data-action="return1984" class="w-full bg-green-500 text-white font-bold py-2 px-4 rounded hover:bg-green-600 transition">החזר את '1984' (שרה)</button>
                            <button data-action="processQueue" class="w-full bg-purple-500 text-white font-bold py-2 px-4 rounded hover:bg-purple-600 transition">טפל בבקשות בתור</button>
                            <button data-action="reset" class="w-full bg-red-500 text-white font-bold py-2 px-4 rounded hover:bg-red-600 transition mt-6">איפוס הדגמה</button>
                        </div>
                    </div>
                    <div class="lg:col-span-2 bg-white p-6 rounded-lg shadow-sm">
                        <h2 class="text-2xl font-bold text-teal-600 mb-4">פלט המערכת (Console)</h2>
                        <div id="demo-console" class="h-64 bg-neutral-800 text-white font-mono text-sm p-4 rounded overflow-y-auto">
                            <p class="text-neutral-400">לחץ על "אתחול המערכת" כדי להתחיל...</p>
                        </div>
                    </div>
                </div>
                <div class="mt-6 bg-white p-6 rounded-lg shadow-sm">
                    <h2 class="text-2xl font-bold text-teal-600 mb-4">מצב מבני הנתונים</h2>
                    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-4 text-center">
                        <div>
                            <h3 class="font-bold mb-2">ספרים (Array)</h3>
                            <div id="demo-array" class="p-2 bg-neutral-100 rounded min-h-[100px] flex flex-col justify-start items-center"></div>
                        </div>
                        <div>
                            <h3 class="font-bold mb-2">השאלות פעילות (LinkedList)</h3>
                            <div id="demo-linkedlist" class="p-2 bg-neutral-100 rounded min-h-[100px] flex flex-col justify-start items-center"></div>
                        </div>
                        <div>
                            <h3 class="font-bold mb-2">קוראים (HashMap)</h3>
                            <div id="demo-hashmap" class="p-2 bg-neutral-100 rounded min-h-[100px] flex flex-col justify-start items-center"></div>
                        </div>
                        <div>
                            <h3 class="font-bold mb-2">תור בקשות (Queue)</h3>
                            <div id="demo-queue" class="p-2 bg-neutral-100 rounded min-h-[100px] flex flex-col justify-start items-center"></div>
                        </div>
                    </div>
                </div>
            </section>

        </main>

    </div>

    <script>
        // --- Main Tab Switching Logic ---
        document.getElementById('main-tabs').addEventListener('click', function(event) {
            if (event.target.tagName === 'BUTTON') {
                const tabId = event.target.dataset.tab;
                
                // Remove active class from all main tab buttons
                document.querySelectorAll('#main-tabs .tab-active').forEach(btn => {
                    btn.classList.remove('tab-active');
                    btn.classList.add('tab-inactive');
                });

                // Add active class to the clicked button
                event.target.classList.remove('tab-inactive');
                event.target.classList.add('tab-active');

                // Hide all content sections
                document.querySelectorAll('#tab-content section').forEach(section => {
                    section.classList.add('hidden');
                });

                // Show the selected content section
                document.getElementById(`${tabId}-content`).classList.remove('hidden');

                // If switching to explorer, ensure initial class is loaded
                if (tabId === 'explorer') {
                    const initialClass = 'Book';
                    const initialClassInfo = codeData[initialClass];
                    document.getElementById('class-title').innerText = initialClass + '.java';
                    document.getElementById('class-description').innerText = initialClassInfo.description;
                    document.getElementById('class-code').innerHTML = initialClassInfo.code;

                    document.querySelectorAll('#class-selector button').forEach(btn => {
                        btn.classList.remove('bg-neutral-200', 'text-neutral-800', 'font-semibold');
                        btn.classList.add('hover:bg-neutral-200', 'transition');
                    });
                    document.querySelector(`[data-class="${initialClass}"]`).classList.add('bg-neutral-200', 'text-neutral-800', 'font-semibold');
                    document.querySelector(`[data-class="${initialClass}"]`).classList.remove('hover:bg-neutral-200', 'transition');
                }
            }
        });

        // --- Class Explorer Data and Logic ---
        const codeData = {
            Book: {
                description: "מטרתה של מחלקת **Book** היא לייצג ספר פיזי בספרייה. היא משמשת כמחלקת בסיס ממנה יורשים סוגי ספרים ספציפיים יותר (כמו ספרים אלקטרוניים וספרי שמע). המחלקה מאחסנת מידע בסיסי על הספר כמו כותרת, מחבר, ISBN, שנת הוצאה ומספר עותקים זמינים וכוללניים. היא מבצעת פעולות כמו השאלת ספר (`borrowBook`) והחזרת ספר (`returnBook`), וכן מספקת מידע על זמינות הספר. היא מקבלת את פרטי הספר (כותרת, מחבר, ISBN, שנת הוצאה, מספר עותקים כולל) בקונסטרוקטור שלה.",
                code: `
<span class="code-comment">// Book.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">public class</span> <span class="code-class">Book</span> {
    <span class="code-comment">// Attributes</span>
    <span class="code-keyword">private</span> String title;
    <span class="code-keyword">private</span> String author;
    <span class="code-keyword">private</span> String isbn;
    <span class="code-keyword">private int</span> publicationYear;
    <span class="code-keyword">private int</span> totalCopies;
    <span class="code-keyword">private int</span> availableCopies;

    <span class="code-comment">// Constructor</span>
    <span class="code-keyword">public</span> <span class="code-class">Book</span>(String title, String author, String isbn, <span class="code-keyword">int</span> publicationYear, <span class="code-keyword">int</span> totalCopies) {
        <span class="code-keyword">this</span>.title = title;
        <span class="code-keyword">this</span>.author = author;
        <span class="code-keyword">this</span>.isbn = isbn;
        <span class="code-keyword">this</span>.publicationYear = publicationYear;
        <span class="code-keyword">this</span>.totalCopies = totalCopies;
        <span class="code-keyword">this</span>.availableCopies = totalCopies;
    }

    <span class="code-comment">// Getters</span>
    <span class="code-keyword">public</span> String <span class="code-function">getTitle</span>() { <span class="code-keyword">return this</span>.title; }
    <span class="code-keyword">public</span> String <span class="code-function">getAuthor</span>() { <span class="code-keyword">return this</span>.author; }
    <span class="code-keyword">public</span> String <span class="code-function">getIsbn</span>() { <span class="code-keyword">return this</span>.isbn; }
    <span class="code-keyword">public int</span> <span class="code-function">getPublicationYear</span>() { <span class="code-keyword">return this</span>.publicationYear; }
    <span class="code-keyword">public int</span> <span class="code-function">getTotalCopies</span>() { <span class="code-keyword">return this</span>.totalCopies; }
    <span class="code-keyword">public int</span> <span class="code-function">getAvailableCopies</span>() { <span class="code-keyword">return this</span>.availableCopies; }

    <span class="code-comment">// Setters</span>
    <span class="code-keyword">public void</span> <span class="code-function">setTitle</span>(String title) { <span class="code-keyword">this</span>.title = title; }
    <span class="code-keyword">public void</span> <span class="code-function">setAuthor</span>(String author) { <span class="code-keyword">this</span>.author = author; }
    <span class="code-keyword">public void</span> <span class="code-function">setIsbn</span>(String isbn) { <span class="code-keyword">this</span>.isbn = isbn; }
    <span class="code-keyword">public void</span> <span class="code-function">setPublicationYear</span>(<span class="code-keyword">int</span> publicationYear) { <span class="code-keyword">this</span>.publicationYear = publicationYear; }
    <span class="code-keyword">public void</span> <span class="code-function">setTotalCopies</span>(<span class="code-keyword">int</span> totalCopies) { <span class="code-keyword">this</span>.totalCopies = totalCopies; }
    <span class="code-keyword">public void</span> <span class="code-function">setAvailableCopies</span>(<span class="code-keyword">int</span> availableCopies) { <span class="code-keyword">this</span>.availableCopies = availableCopies; }

    <span class="code-keyword">public boolean</span> <span class="code-function">isAvailable</span>() {
        <span class="code-keyword">return</span> availableCopies > 0;
    }

    <span class="code-keyword">public boolean</span> <span class="code-function">borrowBook</span>() {
        <span class="code-keyword">if</span> (availableCopies > 0) {
            availableCopies--;
            <span class="code-keyword">return true</span>;
        } <span class="code-keyword">else</span> {
            <span class="code-keyword">return false</span>;
        }
    }

    <span class="code-keyword">public boolean</span> <span class="code-function">returnBook</span>() {
        <span class="code-keyword">if</span> (availableCopies < totalCopies) {
            availableCopies++;
            <span class="code-keyword">return true</span>;
        } <span class="code-keyword">else</span> {
            <span class="code-keyword">return false</span>;
        }
    }

    <span class="code-comment">// Method to display book information (for encapsulation demo)</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayBookInfo</span>() {
        System.out.println(<span class="code-string">"\\nBook Details:"</span>);
        System.out.println(<span class="code-string">"  Title: "</span> + title);
        System.out.println(<span class="code-string">"  Author: "</span> + author);
        System.out.println(<span class="code-string">"  ISBN: "</span> + isbn);
        System.out.println(<span class="code-string">"  Year: "</span> + publicationYear);
        System.out.println(<span class="code-string">"  Copies: "</span> + availableCopies + <span class="code-string">"/"</span> + totalCopies + <span class="code-string">" available"</span>);
    }

    <div class="highlight-polymorphism">
    <span class="code-comment">// Virtual function (for polymorphism demonstration)</span>
    <span class="code-keyword">public void</span> <span class="code-function">getLoanStatus</span>() {
        <span class="code-keyword">if</span> (<span class="code-function">isAvailable</span>()) {
            System.out.println(<span class="code-string">"Loan Status: Available for borrowing."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"Loan Status: Not available currently. All copies are borrowed."</span>);
        }
    }
    </div>
}
                `
            },
            EBook: {
                description: "מטרתה של מחלקת **EBook** היא לייצג ספר אלקטרוני. היא **יורשת** ממחלקת `Book` ומכילה את כל התכונות וההתנהגויות של ספר רגיל, בנוסף לתכונות ייחודיות כמו פורמט קובץ וקישור הורדה. היא מבצעת פעולות ספציפיות לספר אלקטרוני כמו `download()`. המחלקה מקבלת את פרטי הספר הבסיסיים (כותרת, מחבר, ISBN, שנת הוצאה) מהקונסטרוקטור של מחלקת האב (`super`), וכן את פורמט הקובץ וקישור ההורדה.",
                code: `
<span class="code-comment">// EBook.java</span>
<span class="code-keyword">package</span> library_management;

<div class="highlight-inheritance">
<span class="code-keyword">public class</span> <span class="code-class">EBook</span> <span class="code-keyword">extends</span> <span class="code-class">Book</span> {
</div>
    <span class="code-keyword">private</span> String fileFormat;
    <span class="code-keyword">private</span> String downloadLink;

    <span class="code-keyword">public</span> <span class="code-class">EBook</span>(String title, String author, String isbn, <span class="code-keyword">int</span> publicationYear, String fileFormat, String downloadLink) {
        <div class="highlight-inheritance">
        <span class="code-keyword">super</span>(title, author, isbn, publicationYear, 1); <span class="code-comment">// EBooks typically have 1 'copy' (license)</span>
        </div>
        <span class="code-keyword">this</span>.fileFormat = fileFormat;
        <span class="code-keyword">this</span>.downloadLink = downloadLink;
    }

    <span class="code-comment">// Getters for EBook specific attributes</span>
    <span class="code-keyword">public</span> String <span class="code-function">getFileFormat</span>() { <span class="code-keyword">return this</span>.fileFormat; }
    <span class="code-keyword">public</span> String <span class="code-function">getDownloadLink</span>() { <span class="code-keyword">return this</span>.downloadLink; }

    <span class="code-comment">// EBook-specific operation</span>
    <span class="code-keyword">public void</span> <span class="code-function">download</span>() {
        System.out.println(<span class="code-string">"Downloading eBook: "</span> + <span class="code-function">getTitle</span>() + <span class="code-string">" from "</span> + downloadLink);
    }
    
    <div class="highlight-polymorphism">
    <span class="code-comment">// Override displayBookInfo for EBook specific information</span>
    <span class="code-annotation">@Override</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayBookInfo</span>() {
        <span class="code-keyword">super</span>.<span class="code-function">displayBookInfo</span>();
        System.out.println(<span class="code-string">"  Type: EBook"</span>);
        System.out.println(<span class="code-string">"  File Format: "</span> + fileFormat);
        System.out.println(<span class="code-string">"  Download Link: "</span> + downloadLink);
    }
    </div>

    <div class="highlight-polymorphism">
    <span class="code-comment">// Override virtual function for EBook specific status</span>
    <span class="code-annotation">@Override</span>
    <span class="code-keyword">public void</span> <span class="code-function">getLoanStatus</span>() {
        <span class="code-keyword">if</span> (<span class="code-function">isAvailable</span>()) {
            System.out.println(<span class="code-string">"EBook Status: Available for instant download."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"EBook Status: All digital licenses are currently in use."</span>);
        }
    }
    </div>
}
                `
            },
            AudioBook: {
                description: "מטרתה של מחלקת **AudioBook** היא לייצג ספר שמע. היא **יורשת** ממחלקת `Book` ומוסיפה תכונות ייחודיות כמו שם הקריין ומשך ההשמעה. היא מבצעת פעולות ספציפיות לספר שמע כמו `listen()`. המחלקה מקבלת את פרטי הספר הבסיסיים (כותרת, מחבר, ISBN, שנת הוצאה) מהקונסטרוקטור של מחלקת האב (`super`), וכן את שם הקריין ומשך ההשמעה.",
                code: `
<span class="code-comment">// AudioBook.java</span>
<span class="code-keyword">package</span> library_management;

<div class="highlight-inheritance">
<span class="code-keyword">public class</span> <span class="code-class">AudioBook</span> <span class="code-keyword">extends</span> <span class="code-class">Book</span> {
</div>
    <span class="code-comment">// Additional attributes for AudioBook</span>
    <span class="code-keyword">private</span> String narrator;
    <span class="code-keyword">private double</span> durationInHours;

    <span class="code-comment">// Constructor for AudioBook</span>
    <span class="code-keyword">public</span> <span class="code-class">AudioBook</span>(String title, String author, String isbn, <span class="code-keyword">int</span> publicationYear, String narrator, <span class="code-keyword">double</span> durationInHours) {
        <div class="highlight-inheritance">
        <span class="code-keyword">super</span>(title, author, isbn, publicationYear, 1); <span class="code-comment">// AudioBooks typically have 1 'copy' (streaming access)</span>
        </div>
        <span class="code-keyword">this</span>.narrator = narrator;
        <span class="code-keyword">this</span>.durationInHours = durationInHours;
    }

    <span class="code-comment">// Getters for AudioBook specific attributes</span>
    <span class="code-keyword">public</span> String <span class="code-function">getNarrator</span>() {
        <span class="code-keyword">return</span> narrator;
    }

    <span class="code-keyword">public double</span> <span class="code-function">getDurationInHours</span>() {
        <span class="code-keyword">return</span> durationInHours;
    }

    <span class="code-comment">// AudioBook-specific operation</span>
    <span class="code-keyword">public void</span> <span class="code-function">listen</span>() {
        System.out.println(<span class="code-string">"Now listening to the audiobook '"</span> + <span class="code-function">getTitle</span>() + <span class="code-string">"' narrated by "</span> + narrator + <span class="code-string">"."</span>);
    }

    <div class="highlight-polymorphism">
    <span class="code-comment">// Override displayBookInfo to include AudioBook specific information</span>
    <span class="code-annotation">@Override</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayBookInfo</span>() {
        <span class="code-keyword">super</span>.<span class="code-function">displayBookInfo</span>();
        System.out.println(<span class="code-string">"  Type: AudioBook"</span>);
        System.out.println(<span class="code-string">"  Narrator: "</span> + narrator);
        System.out.println(<span class="code-string">"  Duration: "</span> + durationInHours + <span class="code-string">" hours"</span>);
    }
    </div>

    <div class="highlight-polymorphism">
    <span class="code-comment">// Override getLoanStatus for AudioBook specific loan status</span>
    <span class="code-annotation">@Override</span>
    <span class="code-keyword">public void</span> <span class="code-function">getLoanStatus</span>() {
        <span class="code-keyword">if</span> (<span class="code-function">isAvailable</span>()) {
            System.out.println(<span class="code-string">"AudioBook Status: Ready for streaming."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"AudioBook Status: All streaming slots are currently busy."</span>);
        }
    }
    </div>
}
                `
            },
            Reader: {
                description: "מטרתה של מחלקת **Reader** היא לייצג קורא בספרייה. כל קורא מזוהה באמצעות מזהה ייחודי (ID), שם פרטי, שם משפחה ופרטי קשר (אימייל, טלפון). המחלקה מאפשרת גישה ושינוי של פרטי הקורא, ומספקת פונקציה להצגת פרטיו.",
                code: `
<span class="code-comment">// Reader.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">public class</span> <span class="code-class">Reader</span> {
    <span class="code-comment">// Attributes</span>
    <span class="code-keyword">private</span> String readerId;
    <span class="code-keyword">private</span> String firstName;
    <span class="code-keyword">private</span> String lastName;
    <span class="code-keyword">private</span> String email;
    <span class="code-keyword">private</span> String phoneNumber;

    <span class="code-comment">// Constructor</span>
    <span class="code-keyword">public</span> <span class="code-class">Reader</span>(String readerId, String firstName, String lastName, String email, String phoneNumber) {
        <span class="code-keyword">this</span>.readerId = readerId;
        <span class="code-keyword">this</span>.firstName = firstName;
        <span class="code-keyword">this</span>.lastName = lastName;
        <span class="code-keyword">this</span>.email = email;
        <span class="code-keyword">this</span>.phoneNumber = phoneNumber;
    }

    <span class="code-comment">// Getters</span>
    <span class="code-keyword">public</span> String <span class="code-function">getReaderId</span>() { <span class="code-keyword">return this</span>.readerId; }
    <span class="code-keyword">public</span> String <span class="code-function">getFirstName</span>() { <span class="code-keyword">return this</span>.firstName; }
    <span class="code-keyword">public</span> String <span class="code-function">getLastName</span>() { <span class="code-keyword">return this</span>.lastName; }
    <span class="code-keyword">public</span> String <span class="code-function">getEmail</span>() { <span class="code-keyword">return this</span>.email; }
    <span class="code-keyword">public</span> String <span class="code-function">getPhoneNumber</span>() { <span class="code-keyword">return this</span>.phoneNumber; }

    <span class="code-comment">// Setters</span>
    <span class="code-keyword">public void</span> <span class="code-function">setFirstName</span>(String firstName) { <span class="code-keyword">this</span>.firstName = firstName; }
    <span class="code-keyword">public void</span> <span class="code-function">setLastName</span>(String lastName) { <span class="code-keyword">this</span>.lastName = lastName; }
    <span class="code-keyword">public void</span> <span class="code-function">setEmail</span>(String email) { <span class="code-keyword">this</span>.email = email; }
    <span class="code-keyword">public void</span> <span class="code-function">setPhoneNumber</span>(String phoneNumber) { <span class="code-keyword">this</span>.phoneNumber = phoneNumber; }

    <span class="code-comment">// Method to display reader information</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayReaderInfo</span>() {
        System.out.println(<span class="code-string">"\\nReader Details:"</span>);
        System.out.println(<span class="code-string">"  ID: "</span> + readerId);
        System.out.println(<span class="code-string">"  Name: "</span> + firstName + <span class="code-string">" "</span> + lastName);
        System.out.println(<span class="code-string">"  Email: "</span> + email);
        System.out.println(<span class="code-string">"  Phone: "</span> + phoneNumber);
    }
}
                `
            },
            Loan: {
                description: "מטרתה של מחלקת **Loan** היא לייצג השאלת ספר ספציפית על ידי קורא מסוים. היא מקשרת בין אובייקט `Book` לאובייקט `Reader`, ומכילה פרטים כמו תאריך ההשאלה ותאריך ההחזרה הצפוי. היא גם מאפשרת לסמן השאלה כשהסתיימה בפועל.",
                code: `
<span class="code-comment">// Loan.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">import</span> java.time.LocalDate;

<span class="code-keyword">public class</span> <span class="code-class">Loan</span> {
    <span class="code-comment">// Attributes</span>
    <span class="code-keyword">private</span> <span class="code-class">Book</span> book;
    <span class="code-keyword">private</span> <span class="code-class">Reader</span> reader;
    <span class="code-keyword">private</span> LocalDate loanDate;
    <span class="code-keyword">private</span> LocalDate dueDate;
    <span class="code-keyword">private boolean</span> returned;

    <span class="code-comment">// Constructor</span>
    <span class="code-keyword">public</span> <span class="code-class">Loan</span>(<span class="code-class">Book</span> book, <span class="code-class">Reader</span> reader, LocalDate loanDate, LocalDate dueDate) {
        <span class="code-keyword">this</span>.book = book;
        <span class="code-keyword">this</span>.reader = reader;
        <span class="code-keyword">this</span>.loanDate = loanDate;
        <span class="code-keyword">this</span>.dueDate = dueDate;
        <span class="code-keyword">this</span>.returned = <span class="code-keyword">false</span>;
    }

    <span class="code-comment">// Getters</span>
    <span class="code-keyword">public</span> <span class="code-class">Book</span> <span class="code-function">getBook</span>() { <span class="code-keyword">return this</span>.book; }
    <span class="code-keyword">public</span> <span class="code-class">Reader</span> <span class="code-function">getReader</span>() { <span class="code-keyword">return this</span>.reader; }
    <span class="code-keyword">public</span> LocalDate <span class="code-function">getLoanDate</span>() { <span class="code-keyword">return this</span>.loanDate; }
    <span class="code-keyword">public</span> LocalDate <span class="code-function">getDueDate</span>() { <span class="code-keyword">return this</span>.dueDate; }
    <span class="code-keyword">public boolean</span> <span class="code-function">isReturned</span>() { <span class="code-keyword">return this</span>.returned; }

    <span class="code-comment">// Setter for returned status</span>
    <span class="code-keyword">public void</span> <span class="code-function">markAsReturned</span>() {
        <span class="code-keyword">this</span>.returned = <span class="code-keyword">true</span>;
    }

    <span class="code-comment">// Method to display loan information</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayLoanInfo</span>() {
        System.out.println(<span class="code-string">"\\nLoan Details:"</span>);
        System.out.println(<span class="code-string">"  Book: "</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">" (ISBN: "</span> + book.<span class="code-function">getIsbn</span>() + <span class="code-string">")"</span>);
        System.out.println(<span class="code-string">"  Reader: "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">" "</span> + reader.<span class="code-function">getLastName</span>() + <span class="code-string">" (ID: "</span> + reader.<span class="code-function">getReaderId</span>() + <span class="code-string">")"</span>);
        System.out.println(<span class="code-string">"  Loan Date: "</span> + loanDate);
        System.out.println(<span class="code-string">"  Due Date: "</span> + dueDate);
        System.out.println(<span class="code-string">"  Returned: "</span> + (returned ? <span class="code-string">"Yes"</span> : <span class="code-string">"No"</span>));
    }
}
                `
            },
            BookRequest: {
                description: "מטרתה של מחלקת **BookRequest** היא לייצג בקשה של קורא לספר שאינו זמין כרגע. היא מכילה הפניה לספר המבוקש ולקורא שהגיש את הבקשה, וכן את תאריך הבקשה. המחלקה מסייעת לנהל רשימות המתנה בצורה הוגנת.",
                code: `
<span class="code-comment">// BookRequest.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">import</span> java.time.LocalDate;

<span class="code-keyword">public class</span> <span class="code-class">BookRequest</span> {
    <span class="code-comment">// Attributes</span>
    <span class="code-keyword">private</span> <span class="code-class">Book</span> requestedBook;
    <span class="code-keyword">private</span> <span class="code-class">Reader</span> requestingReader;
    <span class="code-keyword">private</span> LocalDate requestDate;

    <span class="code-comment">// Constructor</span>
    <span class="code-keyword">public</span> <span class="code-class">BookRequest</span>(<span class="code-class">Book</span> requestedBook, <span class="code-class">Reader</span> requestingReader, LocalDate requestDate) {
        <span class="code-keyword">this</span>.requestedBook = requestedBook;
        <span class="code-keyword">this</span>.requestingReader = requestingReader;
        <span class="code-keyword">this</span>.requestDate = requestDate;
    }

    <span class="code-comment">// Getters</span>
    <span class="code-keyword">public</span> <span class="code-class">Book</span> <span class="code-function">getRequestedBook</span>() { <span class="code-keyword">return this</span>.requestedBook; }
    <span class="code-keyword">public</span> <span class="code-class">Reader</span> <span class="code-function">getRequestingReader</span>() { <span class="code-keyword">return this</span>.requestingReader; }
    <span class="code-keyword">public</span> LocalDate <span class="code-function">getRequestDate</span>() { <span class="code-keyword">return this</span>.requestDate; }

    <span class="code-comment">// Method to display request information</span>
    <span class="code-keyword">public void</span> <span class="code-function">displayRequestInfo</span>() {
        System.out.println(<span class="code-string">"\\nBook Request Details:"</span>);
        System.out.println(<span class="code-string">"  Book: "</span> + requestedBook.<span class="code-function">getTitle</span>() + <span class="code-string">" (ISBN: "</span> + requestedBook.<span class="code-function">getIsbn</span>() + <span class="code-string">")"</span>);
        System.out.println(<span class="code-string">"  Requester: "</span> + requestingReader.<span class="code-function">getFirstName</span>() + <span class="code-string">" "</span> + requestingReader.<span class="code-function">getLastName</span>() + <span class="code-string">" (ID: "</span> + requestingReader.<span class="code-function">getReaderId</span>() + <span class="code-string">")"</span>);
        System.out.println(<span class="code-string">"  Request Date: "</span> + requestDate);
    }
}
                `
            },
            Library: {
                description: "מחלקת **Library** היא המחלקה המרכזית בפרויקט, המרכזת את הלוגיקה העסקית של ניהול הספרייה. היא משתמשת במבני נתונים שונים כדי לאחסן ולנהל ספרים, קוראים, השאלות ובקשות. המחלקה מספקת שיטות לביצוע פעולות ליבה כמו הוספה והסרת ספרים וקוראים, השאלה והחזרה של ספרים, ניהול תור בקשות והצגת דוחות שונים.",
                code: `
<span class="code-comment">// Library.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">import</span> java.time.LocalDate;
<span class="code-keyword">import</span> java.util.LinkedList;
<span class="code-keyword">import</span> java.util.HashMap;
<span class="code-keyword">import</span> java.util.Queue;

<span class="code-keyword">public class</span> <span class="code-class">Library</span> {
    <span class="code-comment">// Data structures for library management</span>
    <span class="highlight-datastructure">
    <span class="code-comment">// Array to store all books (fixed size for simplicity)</span>
    <span class="code-keyword">private</span> <span class="code-class">Book</span>[] allBooksArray;
    </span>
    <span class="highlight-datastructure">
    <span class="code-comment">// LinkedList to manage active loans (efficient for additions/removals)</span>
    <span class="code-keyword">private</span> LinkedList<<span class="code-class">Loan</span>> activeLoans;
    </span>
    <span class="highlight-datastructure">
    <span class="code-comment">// HashMap to store readers by their ID (fast lookup)</span>
    <span class="code-keyword">private</span> HashMap<String, <span class="code-class">Reader</span>> readersMap;
    </span>
    <span class="highlight-datastructure">
    <span class="code-comment">// Queue to manage book requests (FIFO order)</span>
    <span class="code-keyword">private</span> Queue<<span class="code-class">BookRequest</span>> bookRequestQueue;
    </span>

    <span class="code-keyword">private int</span> bookCount; <span class="code-comment">// To keep track of actual books in the array</span>

    <span class="code-comment">// Constructor</span>
    <span class="code-keyword">public</span> <span class="code-class">Library</span>(<span class="code-keyword">int</span> maxBooks) {
        <span class="code-keyword">this</span>.allBooksArray = <span class="code-keyword">new</span> <span class="code-class">Book</span>[maxBooks];
        <span class="code-keyword">this</span>.activeLoans = <span class="code-keyword">new</span> LinkedList<>();
        <span class="code-keyword">this</span>.readersMap = <span class="code-keyword">new</span> HashMap<>();
        <span class="code-keyword">this</span>.bookRequestQueue = <span class="code-keyword">new</span> LinkedList<>(); <span class="code-comment">// LinkedList implements Queue interface</span>
        <span class="code-keyword">this</span>.bookCount = 0;
    }

    <span class="code-comment">// Methods to manage books</span>
    <span class="code-keyword">public void</span> <span class="code-function">addBook</span>(<span class="code-class">Book</span> book) {
        <span class="code-keyword">if</span> (bookCount < allBooksArray.length) {
            allBooksArray[bookCount++] = book;
            System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' added successfully."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"Cannot add book. Library is full."</span>);
        }
    }

    <span class="code-keyword">public</span> <span class="code-class">Book</span> <span class="code-function">findBookByIsbn</span>(String isbn) {
        <span class="code-keyword">for</span> (<span class="code-keyword">int</span> i = 0; i < bookCount; i++) {
            <span class="code-keyword">if</span> (allBooksArray[i].<span class="code-function">getIsbn</span>().<span class="code-function">equals</span>(isbn)) {
                <span class="code-keyword">return</span> allBooksArray[i];
            }
        }
        <span class="code-keyword">return null</span>; <span class="code-comment">// Book not found</span>
    }

    <span class="code-keyword">public void</span> <span class="code-function">displayAllBooks</span>() {
        System.out.println(<span class="code-string">"\\n--- All Books in Library ---"</span>);
        <span class="code-keyword">if</span> (bookCount == 0) {
            System.out.println(<span class="code-string">"No books in the library."</span>);
            <span class="code-keyword">return</span>;
        }
        <span class="code-keyword">for</span> (<span class="code-keyword">int</span> i = 0; i < bookCount; i++) {
            allBooksArray[i].<span class="code-function">displayBookInfo</span>();
        }
        System.out.println(<span class="code-string">"----------------------------"</span>);
    }

    <span class="code-comment">// Methods to manage loans</span>
    <span class="code-keyword">public void</span> <span class="code-function">borrowBook</span>(String isbn, String readerId) {
        <span class="code-class">Book</span> book = <span class="code-function">findBookByIsbn</span>(isbn);
        <span class="code-class">Reader</span> reader = <span class="code-function">findReaderById</span>(readerId);

        <span class="code-keyword">if</span> (book == <span class="code-keyword">null</span>) {
            System.out.println(<span class="code-string">"Error: Book with ISBN "</span> + isbn + <span class="code-string">" not found."</span>);
            <span class="code-keyword">return</span>;
        }
        <span class="code-keyword">if</span> (reader == <span class="code-keyword">null</span>) {
            System.out.println(<span class="code-string">"Error: Reader with ID "</span> + readerId + <span class="code-string">" not found."</span>);
            <span class="code-keyword">return</span>;
        }

        <span class="code-keyword">if</span> (book.<span class="code-function">borrowBook</span>()) {
            LocalDate loanDate = LocalDate.<span class="code-function">now</span>();
            LocalDate dueDate = loanDate.<span class="code-function">plusWeeks</span>(2); <span class="code-comment">// Due in 2 weeks</span>
            <span class="code-class">Loan</span> newLoan = <span class="code-keyword">new</span> <span class="code-class">Loan</span>(book, reader, loanDate, dueDate);
            activeLoans.<span class="code-function">add</span>(newLoan);
            System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' borrowed by "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">". Due date: "</span> + dueDate);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' is currently not available for borrowing."</span>);
        }
    }

    <span class="code-keyword">public void</span> <span class="code-function">returnBook</span>(String isbn, String readerId) {
        <span class="code-class">Book</span> book = <span class="code-function">findBookByIsbn</span>(isbn);
        <span class="code-class">Reader</span> reader = <span class="code-function">findReaderById</span>(readerId);

        <span class="code-keyword">if</span> (book == <span class="code-keyword">null</span> || reader == <span class="code-keyword">null</span>) {
            System.out.println(<span class="code-string">"Error: Book or Reader not found for return."</span>);
            <span class="code-keyword">return</span>;
        }

        <span class="code-class">Loan</span> loanToRemove = <span class="code-keyword">null</span>;
        <span class="code-keyword">for</span> (<span class="code-class">Loan</span> loan : activeLoans) {
            <span class="code-keyword">if</span> (loan.<span class="code-function">getBook</span>().<span class="code-function">getIsbn</span>().<span class="code-function">equals</span>(isbn) && loan.<span class="code-function">getReader</span>().<span class="code-function">getReaderId</span>().<span class="code-function">equals</span>(readerId) && !loan.<span class="code-function">isReturned</span>()) {
                loanToRemove = loan;
                <span class="code-keyword">break</span>;
            }
        }

        <span class="code-keyword">if</span> (loanToRemove != <span class="code-keyword">null</span>) {
            loanToRemove.<span class="code-function">markAsReturned</span>();
            book.<span class="code-function">returnBook</span>();
            activeLoans.<span class="code-function">remove</span>(loanToRemove); <span class="code-comment">// Remove from active loans list</span>
            System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' returned by "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">" successfully."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"Error: Loan for book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' by "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">" not found or already returned."</span>);
        }
    }

    <span class="code-comment">// Method to remove a book (demonstrates array manipulation)</span>
    <span class="code-keyword">public void</span> <span class="code-function">removeBook</span>(String isbn) {
        <span class="code-keyword">for</span> (<span class="code-keyword">int</span> i = 0; i < bookCount; i++) {
            <span class="code-keyword">if</span> (allBooksArray[i].<span class="code-function">getIsbn</span>().<span class="code-function">equals</span>(isbn)) {
                <span class="code-comment">// Shift elements to the left to fill the gap</span>
                <span class="code-keyword">for</span> (<span class="code-keyword">int</span> j = i; j < bookCount - 1; j++) {
                    allBooksArray[j] = allBooksArray[j + 1];
                }
                allBooksArray[bookCount - 1] = <span class="code-keyword">null</span>; <span class="code-comment">// Nullify the last element</span>
                bookCount--;
                System.out.println(<span class="code-string">"Book with ISBN "</span> + isbn + <span class="code-string">" removed successfully."</span>);
                <span class="code-keyword">return</span>;
            }
        }
        System.out.println(<span class="code-string">"Book with ISBN "</span> + isbn + <span class="code-string">" not found."</span>);
    }

    <span class="code-keyword">public void</span> <span class="code-function">displayActiveLoans</span>() {
        System.out.println(<span class="code-string">"\\n--- Active Loans ---"</span>);
        <span class="code-keyword">if</span> (activeLoans.<span class="code-function">isEmpty</span>()) {
            System.out.println(<span class="code-string">"No active loans."</span>);
            <span class="code-keyword">return</span>;
        }
        <span class="code-keyword">for</span> (<span class="code-class">Loan</span> loan : activeLoans) {
            loan.<span class="code-function">displayLoanInfo</span>();
        }
        System.out.println(<span class="code-string">"----------------------"</span>);
    }

    <span class="code-comment">// Methods to manage readers</span>
    <span class="code-keyword">public void</span> <span class="code-function">addReader</span>(<span class="code-class">Reader</span> reader) {
        <span class="code-keyword">if</span> (readersMap.<span class="code-function">containsKey</span>(reader.<span class="code-function">getReaderId</span>())) {
            System.out.println(<span class="code-string">"Error: Reader with ID "</span> + reader.<span class="code-function">getReaderId</span>() + <span class="code-string">" already exists."</span>);
        } <span class="code-keyword">else</span> {
            readersMap.<span class="code-function">put</span>(reader.<span class="code-function">getReaderId</span>(), reader);
            System.out.println(<span class="code-string">"Reader '"</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">" "</span> + reader.<span class="code-function">getLastName</span>() + <span class="code-string">"' added successfully."</span>);
        }
    }

    <span class="code-keyword">public</span> <span class="code-class">Reader</span> <span class="code-function">findReaderById</span>(String readerId) {
        <span class="code-keyword">return</span> readersMap.<span class="code-function">get</span>(readerId);
    }

    <span class="code-keyword">public void</span> <span class="code-function">displayAllReaders</span>() {
        System.out.println(<span class="code-string">"\\n--- All Readers ---"</span>);
        <span class="code-keyword">if</span> (readersMap.<span class="code-function">isEmpty</span>()) {
            System.out.println(<span class="code-string">"No readers registered."</span>);
            <span class="code-keyword">return</span>;
        }
        <span class="code-keyword">for</span> (<span class="code-class">Reader</span> reader : readersMap.<span class="code-function">values</span>()) {
            reader.<span class="code-function">displayReaderInfo</span>();
        }
        System.out.println(<span class="code-string">"---------------------"</span>);
    }

    <span class="code-comment">// Methods to manage book requests (Queue)</span>
    <span class="code-keyword">public void</span> <span class="code-function">requestBook</span>(<span class="code-class">Book</span> book, <span class="code-class">Reader</span> reader) {
        <span class="code-keyword">if</span> (book != <span class="code-keyword">null</span> && reader != <span class="code-keyword">null</span>) {
            <span class="code-class">BookRequest</span> request = <span class="code-keyword">new</span> <span class="code-class">BookRequest</span>(book, reader, LocalDate.<span class="code-function">now</span>());
            bookRequestQueue.<span class="code-function">offer</span>(request); <span class="code-comment">// Add to the end of the queue</span>
            System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' requested by "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">". Added to queue."</span>);
        } <span class="code-keyword">else</span> {
            System.out.println(<span class="code-string">"Error: Cannot request book. Book or Reader is null."</span>);
        }
    }

    <span class="code-keyword">public void</span> <span class="code-function">processBookRequests</span>() {
        System.out.println(<span class="code-string">"\\n--- Processing Book Requests ---"</span>);
        <span class="code-keyword">if</span> (bookRequestQueue.<span class="code-function">isEmpty</span>()) {
            System.out.println(<span class="code-string">"No pending book requests."</span>);
            <span class="code-keyword">return</span>;
        }

        <span class="code-keyword">while</span> (!bookRequestQueue.<span class="code-function">isEmpty</span>()) {
            <span class="code-class">BookRequest</span> request = bookRequestQueue.<span class="code-function">poll</span>(); <span class="code-comment">// Get and remove the head of the queue</span>
            <span class="code-class">Book</span> book = request.<span class="code-function">getRequestedBook</span>();
            <span class="code-class">Reader</span> reader = request.<span class="code-function">getRequestingReader</span>();

            System.out.println(<span class="code-string">"Processing request for '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' by "</span> + reader.<span class="code-function">getFirstName</span>() + <span class="code-string">"."</span>);
            <span class="code-keyword">if</span> (book.<span class="code-function">isAvailable</span>()) {
                <span class="code-function">borrowBook</span>(book.<span class="code-function">getIsbn</span>(), reader.<span class="code-function">getReaderId</span>());
            } <span class="code-keyword">else</span> {
                System.out.println(<span class="code-string">"Book '"</span> + book.<span class="code-function">getTitle</span>() + <span class="code-string">"' is still not available. Request remains pending for future processing (or could be re-added)."</span>);
                <span class="code-comment">// Optionally, re-add to queue or handle differently</span>
            }
        }
        System.out.println(<span class="code-string">"--------------------------------"</span>);
    }

    <span class="code-keyword">public void</span> <span class="code-function">displayBookRequests</span>() {
        System.out.println(<span class="code-string">"\\n--- Pending Book Requests ---"</span>);
        <span class="code-keyword">if</span> (bookRequestQueue.<span class="code-function">isEmpty</span>()) {
            System.out.println(<span class="code-string">"No pending book requests."</span>);
            <span class="code-keyword">return</span>;
        }
        <span class="code-keyword">for</span> (<span class="code-class">BookRequest</span> request : bookRequestQueue) {
            request.<span class="code-function">displayRequestInfo</span>();
        }
        System.out.println(<span class="code-string">"-------------------------------"</span>);
    }
}
                `
            },
            Main: {
                description: "מחלקת **Main** היא נקודת הכניסה לאפליקציה. היא מדגימה את אופן השימוש במחלקת `Library` ובמחלקות נוספות על ידי יצירת אובייקטים, הוספת נתונים וביצוע פעולות שונות כגון השאלת ספרים, החזרתם, וניהול בקשות, כדי להדגים את הפונקציונליות המלאה של מערכת הספרייה.",
                code: `
<span class="code-comment">// Main.java</span>
<span class="code-keyword">package</span> library_management;

<span class="code-keyword">import</span> java.time.LocalDate;

<span class="code-keyword">public class</span> <span class="code-class">Main</span> {
    <span class="code-keyword">public static void</span> <span class="code-function">main</span>(String[] args) {
        System.out.println(<span class="code-string">"--- Library Management System Demo ---"</span>);

        <span class="code-comment">// 1. Initialize Library</span>
        <span class="code-class">Library</span> myLibrary = <span class="code-keyword">new</span> <span class="code-class">Library</span>(10); <span class="code-comment">// Max 10 books</span>

        <span class="code-comment">// 2. Create Books (Polymorphism in action)</span>
        <span class="code-class">Book</span> book1 = <span class="code-keyword">new</span> <span class="code-class">Book</span>(<span class="code-string">"The Great Gatsby"</span>, <span class="code-string">"F. Scott Fitzgerald"</span>, <span class="code-string">"978-0743273565"</span>, 1925, 2);
        <span class="code-class">Book</span> book2 = <span class="code-keyword">new</span> <span class="code-class">EBook</span>(<span class="code-string">"1984"</span>, <span class="code-string">"George Orwell"</span>, <span class="code-string">"978-0451524935"</span>, 1949, <span class="code-string">"PDF"</span>, <span class="code-string">"http://example.com/1984.pdf"</span>);
        <span class="code-class">Book</span> book3 = <span class="code-keyword">new</span> <span class="code-class">AudioBook</span>(<span class="code-string">"To Kill a Mockingbird"</span>, <span class="code-string">"Harper Lee"</span>, <span class="code-string">"978-0061120084"</span>, 1960, <span class="code-string">"Sissy Spacek"</span>, 12.5);

        <span class="code-comment">// Demonstrate Polymorphism: Calling common method on different book types</span>
        book1.<span class="code-function">displayBookInfo</span>();
        book2.<span class="code-function">displayBookInfo</span>();
        book3.<span class="code-function">displayBookInfo</span>();

        <span class="code-comment">// 3. Add Books to Library (Array)</span>
        myLibrary.<span class="code-function">addBook</span>(book1);
        myLibrary.<span class="code-function">addBook</span>(book2);
        myLibrary.<span class="code-function">addBook</span>(book3);
        myLibrary.<span class="code-function">displayAllBooks</span>();

        <span class="code-comment">// 4. Create Readers (HashMap)</span>
        <span class="code-class">Reader</span> reader1 = <span class="code-keyword">new</span> <span class="code-class">Reader</span>(<span class="code-string">"R001"</span>, <span class="code-string">"איתי"</span>, <span class="code-string">"ישראלי"</span>, <span class="code-string">"itay@example.com"</span>, <span class="code-string">"050-1234567"</span>);
        <span class="code-class">Reader</span> reader2 = <span class="code-keyword">new</span> <span class="code-class">Reader</span>(<span class="code-string">"R002"</span>, <span class="code-string">"שרה"</span>, <span class="code-string">"כהן"</span>, <span class="code-string">"sara@example.com"</span>, <span class="code-string">"052-9876543"</span>);
        myLibrary.<span class="code-function">addReader</span>(reader1);
        myLibrary.<span class="code-function">addReader</span>(reader2);
        myLibrary.<span class="code-function">displayAllReaders</span>();

        <span class="code-comment">// 5. Borrow Books (LinkedList for active loans)</span>
        System.out.println(<span class="code-string">"\\n--- Borrowing Books ---"</span>);
        myLibrary.<span class="code-function">borrowBook</span>(<span class="code-string">"978-0743273565"</span>, <span class="code-string">"R001"</span>); <span class="code-comment">// Itay borrows Gatsby</span>
        myLibrary.<span class="code-function">borrowBook</span>(<span class="code-string">"978-0451524935"</span>, <span class="code-string">"R002"</span>); <span class="code-comment">// Sara borrows 1984</span>
        myLibrary.<span class="code-function">displayActiveLoans</span>();
        book1.<span class="code-function">getLoanStatus</span>(); <span class="code-comment">// Check status after borrowing</span>
        book2.<span class="code-function">getLoanStatus</span>();
        
        <span class="code-comment">// 6. Try to borrow an unavailable book (Queue for requests)</span>
        System.out.println(<span class="code-string">"\\n--- Attempt to borrow unavailable book ---"</span>);
        myLibrary.<span class="code-function">borrowBook</span>(<span class="code-string">"978-0451524935"</span>, <span class="code-string">"R001"</span>); <span class="code-comment">// Itay tries to borrow 1984 (unavailable)</span>
        myLibrary.<span class="code-function">requestBook</span>(book2, reader1); <span class="code-comment">// Itay requests 1984</span>
        myLibrary.<span class="code-function">displayBookRequests</span>();

        <span class="code-comment">// 7. Return a Book</span>
        System.out.println(<span class="code-string">"\\n--- Returning a Book ---"</span>);
        myLibrary.<span class="code-function">returnBook</span>(<span class="code-string">"978-0451524935"</span>, <span class="code-string">"R002"</span>); <span class="code-comment">// Sara returns 1984</span>
        myLibrary.<span class="code-function">displayActiveLoans</span>();
        book2.<span class="code-function">getLoanStatus</span>(); <span class="code-comment">// Check status after returning</span>

        <span class="code-comment">// 8. Process Book Requests</span>
        myLibrary.<span class="code-function">processBookRequests</span>();
        myLibrary.<span class="code-function">displayActiveLoans</span>(); <span class="code-comment">// 1984 should now be borrowed by Itay</span>
        myLibrary.<span class="code-function">displayBookRequests</span>(); <span class="code-comment">// Queue should be empty</span>

        System.out.println(<span class="code-string">"\\n--- Demo Complete ---"</span>);
    }
}
                `
            }
        };

        document.getElementById('class-selector').addEventListener('click', function(event) {
            if (event.target.tagName === 'BUTTON') {
                const className = event.target.dataset.class;
                const classInfo = codeData[className];
                document.getElementById('class-title').innerText = className + '.java';
                document.getElementById('class-description').innerText = classInfo.description;
                document.getElementById('class-code').innerHTML = classInfo.code;

                // Update active button styling
                document.querySelectorAll('#class-selector button').forEach(btn => {
                    btn.classList.remove('bg-neutral-200', 'text-neutral-800', 'font-semibold');
                    btn.classList.add('hover:bg-neutral-200', 'transition');
                });
                event.target.classList.add('bg-neutral-200', 'text-neutral-800', 'font-semibold');
                event.target.classList.remove('hover:bg-neutral-200', 'transition');
            }
        });

        // Initial load for explorer tab
        document.addEventListener('DOMContentLoaded', () => {
            const initialClass = 'Book'; // Default class to show on load
            const initialClassInfo = codeData[initialClass];
            if (initialClassInfo) {
                document.getElementById('class-title').innerText = initialClass + '.java';
                document.getElementById('class-description').innerText = initialClassInfo.description;
                document.getElementById('class-code').innerHTML = initialClassInfo.code;
            }
            // Ensure the initial tab is active
            document.querySelector('[data-tab="overview"]').click();
        });


        // --- Interactive Demo Logic ---
        let currentLibrary; // Global variable to hold the Library instance

        const demoConsole = document.getElementById('demo-console');
        const demoArray = document.getElementById('demo-array');
        const demoLinkedList = document.getElementById('demo-linkedlist');
        const demoHashMap = document.getElementById('demo-hashmap');
        const demoQueue = document.getElementById('demo-queue');

        function appendToConsole(message) {
            const p = document.createElement('p');
            p.textContent = message;
            demoConsole.appendChild(p);
            demoConsole.scrollTop = demoConsole.scrollHeight; // Auto-scroll to bottom
        }

        function updateDataStructuresDisplay() {
            // Clear previous content
            demoArray.innerHTML = '';
            demoLinkedList.innerHTML = '';
            demoHashMap.innerHTML = '';
            demoQueue.innerHTML = '';

            if (!currentLibrary) {
                demoArray.textContent = 'לא מאותחל';
                demoLinkedList.textContent = 'לא מאותחל';
                demoHashMap.textContent = 'לא מאותחל';
                demoQueue.textContent = 'לא מאותחל';
                return;
            }

            // Display Array (Books)
            if (currentLibrary.allBooksArray) {
                const books = Array.from(currentLibrary.allBooksArray).filter(b => b != null);
                if (books.length > 0) {
                    books.forEach((book, index) => {
                        const div = document.createElement('div');
                        div.className = 'text-xs bg-teal-100 text-teal-800 p-1 rounded my-0.5 w-full text-center';
                        div.textContent = `${index}: ${book.title} (${book.availableCopies}/${book.totalCopies})`;
                        demoArray.appendChild(div);
                    });
                } else {
                    demoArray.textContent = 'אין ספרים';
                }
            }

            // Display LinkedList (Active Loans)
            if (currentLibrary.activeLoans) {
                if (currentLibrary.activeLoans.length > 0) {
                    currentLibrary.activeLoans.forEach(loan => {
                        const div = document.createElement('div');
                        div.className = 'text-xs bg-blue-100 text-blue-800 p-1 rounded my-0.5 w-full text-center';
                        div.textContent = `${loan.book.title} -> ${loan.reader.firstName}`;
                        demoLinkedList.appendChild(div);
                    });
                } else {
                    demoLinkedList.textContent = 'אין השאלות פעילות';
                }
            }

            // Display HashMap (Readers)
            if (currentLibrary.readersMap) {
                const readers = Object.values(currentLibrary.readersMap);
                if (readers.length > 0) {
                    readers.forEach(reader => {
                        const div = document.createElement('div');
                        div.className = 'text-xs bg-purple-100 text-purple-800 p-1 rounded my-0.5 w-full text-center';
                        div.textContent = `${reader.readerId}: ${reader.firstName} ${reader.lastName}`;
                        demoHashMap.appendChild(div);
                    });
                } else {
                    demoHashMap.textContent = 'אין קוראים רשומים';
                }
            }

            // Display Queue (Book Requests)
            if (currentLibrary.bookRequestQueue) {
                if (currentLibrary.bookRequestQueue.length > 0) {
                    currentLibrary.bookRequestQueue.forEach(request => {
                        const div = document.createElement('div');
                        div.className = 'text-xs bg-yellow-100 text-yellow-800 p-1 rounded my-0.5 w-full text-center';
                        div.textContent = `${request.requestingReader.firstName} -> ${request.requestedBook.title}`;
                        demoQueue.appendChild(div);
                    });
                } else {
                    demoQueue.textContent = 'אין בקשות ממתינות';
                }
            }
        }


        // Simplified Java-like classes for the demo environment
        class Book {
            constructor(title, author, isbn, publicationYear, totalCopies) {
                this.title = title;
                this.author = author;
                this.isbn = isbn;
                this.publicationYear = publicationYear;
                this.totalCopies = totalCopies;
                this.availableCopies = totalCopies;
            }
            getTitle() { return this.title; }
            getAuthor() { return this.author; }
            getIsbn() { return this.isbn; }
            getPublicationYear() { return this.publicationYear; }
            getTotalCopies() { return this.totalCopies; }
            getAvailableCopies() { return this.availableCopies; }
            isAvailable() { return this.availableCopies > 0; }
            borrowBook() {
                if (this.availableCopies > 0) {
                    this.availableCopies--;
                    return true;
                }
                return false;
            }
            returnBook() {
                if (this.availableCopies < this.totalCopies) {
                    this.availableCopies++;
                    return true;
                }
                return false;
            }
            displayBookInfo() {
                // Not used in console output for demo, but good for completeness
            }
            getLoanStatus() {
                // Not used in console output for demo, but good for completeness
            }
        }

        class EBook extends Book {
            constructor(title, author, isbn, publicationYear, fileFormat, downloadLink) {
                super(title, author, isbn, publicationYear, 1);
                this.fileFormat = fileFormat;
                this.downloadLink = downloadLink;
            }
        }

        class AudioBook extends Book {
            constructor(title, author, isbn, publicationYear, narrator, durationInHours) {
                super(title, author, isbn, publicationYear, 1);
                this.narrator = narrator;
                this.durationInHours = durationInHours;
            }
        }

        class Reader {
            constructor(readerId, firstName, lastName, email, phoneNumber) {
                this.readerId = readerId;
                this.firstName = firstName;
                this.lastName = lastName;
                this.email = email;
                this.phoneNumber = phoneNumber;
            }
            getReaderId() { return this.readerId; }
            getFirstName() { return this.firstName; }
            getLastName() { return this.lastName; }
        }

        class Loan {
            constructor(book, reader, loanDate, dueDate) {
                this.book = book;
                this.reader = reader;
                this.loanDate = loanDate;
                this.dueDate = dueDate;
                this.returned = false;
            }
            getBook() { return this.book; }
            getReader() { return this.reader; }
            isReturned() { return this.returned; }
            markAsReturned() { this.returned = true; }
        }

        class BookRequest {
            constructor(requestedBook, requestingReader, requestDate) {
                this.requestedBook = requestedBook;
                this.requestingReader = requestingReader;
                this.requestDate = requestDate;
            }
            getRequestedBook() { return this.requestedBook; }
            getRequestingReader() { return this.requestingReader; }
        }


        class Library {
            constructor(maxBooks) {
                // Data structures for library management
                this.allBooksArray = new Array(maxBooks).fill(null);
                this.activeLoans = []; // Using JS Array as LinkedList substitute for demo
                this.readersMap = {}; // Using JS Object as HashMap substitute for demo
                this.bookRequestQueue = []; // Using JS Array as Queue substitute for demo

                this.bookCount = 0; // To keep track of actual books in the array
            }

            addBook(book) {
                if (this.bookCount < this.allBooksArray.length) {
                    this.allBooksArray[this.bookCount++] = book;
                    appendToConsole(`Book '${book.getTitle()}' added successfully.`);
                } else {
                    appendToConsole(`Cannot add book. Library is full.`);
                }
            }

            findBookByIsbn(isbn) {
                for (let i = 0; i < this.bookCount; i++) {
                    if (this.allBooksArray[i] && this.allBooksArray[i].getIsbn() === isbn) {
                        return this.allBooksArray[i];
                    }
                }
                return null; // Book not found
            }

            addReader(reader) {
                if (this.readersMap[reader.getReaderId()]) {
                    appendToConsole(`Error: Reader with ID ${reader.getReaderId()} already exists.`);
                } else {
                    this.readersMap[reader.getReaderId()] = reader;
                    appendToConsole(`Reader '${reader.getFirstName()} ${reader.getLastName()}' added successfully.`);
                }
            }

            findReaderById(readerId) {
                return this.readersMap[readerId] || null;
            }

            borrowBook(isbn, readerId) {
                const book = this.findBookByIsbn(isbn);
                const reader = this.findReaderById(readerId);

                if (!book) {
                    appendToConsole(`Error: Book with ISBN ${isbn} not found.`);
                    return;
                }
                if (!reader) {
                    appendToConsole(`Error: Reader with ID ${readerId} not found.`);
                    return;
                }

                if (book.borrowBook()) {
                    const loanDate = new Date();
                    const dueDate = new Date();
                    dueDate.setDate(loanDate.getDate() + 14); // Due in 2 weeks
                    const newLoan = new Loan(book, reader, loanDate.toLocaleDateString('he-IL'), dueDate.toLocaleDateString('he-IL'));
                    this.activeLoans.push(newLoan); // Add to active loans
                    appendToConsole(`Book '${book.getTitle()}' borrowed by ${reader.getFirstName()}. Due date: ${dueDate.toLocaleDateString('he-IL')}`);
                } else {
                    appendToConsole(`Book '${book.getTitle()}' is currently not available for borrowing.`);
                }
            }

            returnBook(isbn, readerId) {
                const book = this.findBookByIsbn(isbn);
                const reader = this.findReaderById(readerId);

                if (!book || !reader) {
                    appendToConsole(`Error: Book or Reader not found for return.`);
                    return;
                }

                let loanIndexToRemove = -1;
                for (let i = 0; i < this.activeLoans.length; i++) {
                    const loan = this.activeLoans[i];
                    if (loan.getBook().getIsbn() === isbn && loan.getReader().getReaderId() === readerId && !loan.isReturned()) {
                        loanIndexToRemove = i;
                        break;
                    }
                }

                if (loanIndexToRemove !== -1) {
                    this.activeLoans[loanIndexToRemove].markAsReturned();
                    book.returnBook();
                    this.activeLoans.splice(loanIndexToRemove, 1); // Remove from active loans list
                    appendToConsole(`Book '${book.getTitle()}' returned by ${reader.getFirstName()} successfully.`);
                } else {
                    appendToConsole(`Error: Loan for book '${book.getTitle()}' by ${reader.getFirstName()} not found or already returned.`);
                }
            }

            requestBook(book, reader) {
                if (book && reader) {
                    const request = new BookRequest(book, reader, new Date().toLocaleDateString('he-IL'));
                    this.bookRequestQueue.push(request); // Add to the end of the queue
                    appendToConsole(`Book '${book.getTitle()}' requested by ${reader.getFirstName()}. Added to queue.`);
                } else {
                    appendToConsole(`Error: Cannot request book. Book or Reader is null.`);
                }
            }

            processBookRequests() {
                appendToConsole(`\n--- Processing Book Requests ---`);
                if (this.bookRequestQueue.length === 0) {
                    appendToConsole(`No pending book requests.`);
                    return;
                }

                while (this.bookRequestQueue.length > 0) {
                    const request = this.bookRequestQueue.shift(); // Get and remove the head of the queue
                    const book = request.getRequestedBook();
                    const reader = request.getRequestingReader();

                    appendToConsole(`Processing request for '${book.getTitle()}' by ${reader.getFirstName()}.`);
                    if (book.isAvailable()) {
                        this.borrowBook(book.getIsbn(), reader.getReaderId());
                    } else {
                        appendToConsole(`Book '${book.getTitle()}' is still not available. Request remains pending for future processing (or could be re-added).`);
                        // Optionally, re-add to queue or handle differently
                    }
                }
                appendToConsole(`--------------------------------`);
            }
        }


        document.getElementById('demo-controls').addEventListener('click', function(event) {
            const action = event.target.dataset.action;
            demoConsole.innerHTML = ''; // Clear console for each action

            if (action === 'init') {
                currentLibrary = new Library(5); // Initialize with max 5 books
                currentLibrary.addBook(new Book("The Great Gatsby", "F. Scott Fitzgerald", "978-0743273565", 1925, 2));
                currentLibrary.addBook(new EBook("1984", "George Orwell", "978-0451524935", 1949, "PDF", "http://example.com/1984.pdf"));
                currentLibrary.addBook(new AudioBook("To Kill a Mockingbird", "Harper Lee", "978-0061120084", 1960, "Sissy Spacek", 12.5));
                currentLibrary.addReader(new Reader("R001", "איתי", "ישראלי", "itay@example.com", "050-1234567"));
                currentLibrary.addReader(new Reader("R002", "שרה", "כהן", "sara@example.com", "052-9876543"));
                appendToConsole("מערכת הספרייה אותחלה עם ספרים וקוראים לדוגמה.");
            } else if (currentLibrary) { // Ensure library is initialized for other actions
                if (action === 'borrowGatsby') {
                    currentLibrary.borrowBook("978-0743273565", "R001");
                } else if (action === 'borrow1984') {
                    currentLibrary.borrowBook("978-0451524935", "R002");
                } else if (action === 'queue1984') {
                    const book1984 = currentLibrary.findBookByIsbn("978-0451524935");
                    const readerItay = currentLibrary.findReaderById("R001");
                    if (!book1984.isAvailable()) {
                         currentLibrary.requestBook(book1984, readerItay);
                    } else {
                        appendToConsole("הספר '1984' זמין כרגע, אין צורך בתור.");
                    }
                } else if (action === 'return1984') {
                    currentLibrary.returnBook("978-0451524935", "R002");
                } else if (action === 'processQueue') {
                    currentLibrary.processBookRequests();
                } else if (action === 'reset') {
                    currentLibrary = null;
                    appendToConsole("הדגמה אותחלה מחדש.");
                }
            } else {
                appendToConsole("יש לאתחל את המערכת תחילה (לחץ על 'אתחול המערכת').");
            }
            updateDataStructuresDisplay(); // Update display after each action
        });

        // Initial state display
        updateDataStructuresDisplay();
    </script>
</body>
</html>
