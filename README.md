
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مكتبة الكتب الإلكترونية - المكتبة الضخمة</title>
    <style>
        /* CSS للتصميم الجذاب */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }
        header {
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        #search-container {
            margin: 20px auto;
            max-width: 800px;
            text-align: center;
        }
        #search-bar {
            width: 70%;
            padding: 10px;
            font-size: 1em;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        #filter-select {
            padding: 10px;
            font-size: 1em;
            margin-left: 10px;
            border-radius: 5px;
        }
        #books-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 20px auto;
            padding: 0 20px;
        }
        .book-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            padding: 15px;
            text-align: center;
            transition: transform 0.3s;
        }
        .book-card:hover {
            transform: scale(1.05);
        }
        .book-card img {
            width: 150px;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        .book-card h2 {
            font-size: 1.5em;
            margin: 10px 0;
            color: #2c3e50;
        }
        .book-card p {
            font-size: 1em;
            color: #666;
            margin-bottom: 15px;
        }
        .download-btn {
            background-color: #3498db;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        .download-btn:hover {
            background-color: #2980b9;
        }
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
        }
        /* Responsive للشاشات الصغيرة */
        @media (max-width: 600px) {
            #books-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>مرحباً بك في المكتبة الإلكترونية الضخمة</h1>
        <p>اكتشف آلاف الكتب ونزلها مجاناً!</p>
    </header>

    <div id="search-container">
        <input type="text" id="search-bar" placeholder="ابحث عن كتاب (بالعنوان أو الفئة)...">
        <select id="filter-select">
            <option value="all">جميع الفئات</option>
            <option value="روايات">روايات</option>
            <option value="علوم">علوم</option>
            <option value="تاريخ">تاريخ</option>
            <option value="تطوير ذاتي">تطوير ذاتي</option>
        </select>
    </div>

    <div id="books-container">
        <!-- الكتب هتضاف هنا بواسطة JS -->
    </div>

    <footer>
        <p>&copy; 2026 المكتبة الضخمة. جميع الحقوق محفوظة.</p>
    </footer>

    <script>
        // JavaScript للتفاعل والكتب
        const books = [
            {
                title: "رواية 1984",
                description: "رواية ديستوبية كلاسيكية عن المراقبة والسلطة.",
                category: "روايات",
                image: "https://via.placeholder.com/150x200?text=1984", // غيرها بصورة حقيقية
                downloadLink: "books/1984.pdf" // غيرها بملف PDF حقيقي
            },
            {
                title: "فيزياء الكم",
                description: "كتاب علمي عن أساسيات الفيزياء الكمية.",
                category: "علوم",
                image: "https://via.placeholder.com/150x200?text=Quantum+Physics",
                downloadLink: "books/quantum.pdf"
            },
            {
                title: "تاريخ العالم",
                description: "نظرة شاملة على تاريخ البشرية.",
                category: "تاريخ",
                image: "https://via.placeholder.com/150x200?text=World+History",
                downloadLink: "books/history.pdf"
            },
            {
                title: "قوة العادات",
                description: "كتاب تطوير ذاتي عن بناء عادات ناجحة.",
                category: "تطوير ذاتي",
                image: "https://via.placeholder.com/150x200?text=Atomic+Habits",
                downloadLink: "books/habits.pdf"
            },
            {
                title: "رواية هاري بوتر",
                description: "الجزء الأول من سلسلة السحر والمغامرات.",
                category: "روايات",
                image: "https://via.placeholder.com/150x200?text=Harry+Potter",
                downloadLink: "books/harry.pdf"
            },
            {
                title: "علم البيانات",
                description: "دليل للمبتدئين في علم البيانات.",
                category: "علوم",
                image: "https://via.placeholder.com/150x200?text=Data+Science",
                downloadLink: "books/data.pdf"
            },
            {
                title: "تاريخ الإمبراطورية الرومانية",
                description: "قصة صعود وسقوط الإمبراطورية.",
                category: "تاريخ",
                image: "https://via.placeholder.com/150x200?text=Roman+Empire",
                downloadLink: "books/roman.pdf"
            },
            {
                title: "كيف تفوز الأصدقاء",
                description: "كتاب كلاسيكي في التطوير الشخصي.",
                category: "تطوير ذاتي",
                image: "https://via.placeholder.com/150x200?text=Win+Friends",
                downloadLink: "books/friends.pdf"
            },
            {
                title: "رواية غاتسبي العظيم",
                description: "رواية عن الحلم الأمريكي.",
                category: "روايات",
                image: "https://via.placeholder.com/150x200?text=Great+Gatsby",
                downloadLink: "books/gatsby.pdf"
            },
            {
                title: "بيولوجيا الخلية",
                description: "كتاب علمي عن علم الأحياء.",
                category: "علوم",
                image: "https://via.placeholder.com/150x200?text=Cell+Biology",
                downloadLink: "books/biology.pdf"
            }
            // أضف المزيد من الكتب هنا لجعله أضخم (يمكن آلاف إذا استخدمت قاعدة بيانات)
        ];

        const booksContainer = document.getElementById('books-container');
        const searchBar = document.getElementById('search-bar');
        const filterSelect = document.getElementById('filter-select');

        // دالة لعرض الكتب
        function displayBooks(filteredBooks) {
            booksContainer.innerHTML = ''; // مسح القديم
            filteredBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.classList.add('book-card');
                bookCard.innerHTML = `
                    <img src="\( {book.image}" alt=" \){book.title}">
                    <h2>${book.title}</h2>
                    <p>${book.description}</p>
                    <a href="${book.downloadLink}" class="download-btn" download>تنزيل الكتاب</a>
                `;
                booksContainer.appendChild(bookCard);
            });
        }

        // فلترة والبحث
        function filterBooks() {
            const searchText = searchBar.value.toLowerCase();
            const selectedCategory = filterSelect.value;

            const filtered = books.filter(book => {
                const matchesSearch = book.title.toLowerCase().includes(searchText) || book.description.toLowerCase().includes(searchText) || book.category.toLowerCase().includes(searchText);
                const matchesCategory = selectedCategory === 'all' || book.category === selectedCategory;
                return matchesSearch && matchesCategory;
            });

            displayBooks(filtered);
        }

        // عرض الكتب الأولي
        displayBooks(books);

        // حدث البحث والتصفية
        searchBar.addEventListener('input', filterBooks);
        filterSelect.addEventListener('change', filterBooks);
    </script>
</body>
</html>
