<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfume Personality Quiz | FragranceNisheFinds</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <div id="quiz">
        <div id="start-screen">
            <h1>Find Your Scent and Discover Yourself!</h1>
            <p>Answer 10 simple questions, and we’ll match you with the perfect fragrance from FragranceNisheFinds that reflects your unique vibe. Plus, uncover your style, personality, and maybe even something new about yourself. Ready to dive in? Let’s go!</p>
            <button id="start-btn">Start Now</button>
        </div>
        <div id="quiz-content" style="display: none;">
            <div id="progress-bar">
                <div id="progress"></div>
            </div>
            <div id="question-0" class="question">
                <h3>1. Are you a man or a woman?</h3>
                <button onclick="saveAnswer(0, 'Man')">Man</button>
                <button onclick="saveAnswer(0, 'Woman')">Woman</button>
            </div>
            <div id="question-1" class="question">
                <h3>2. What’s your age?</h3>
                <button onclick="saveAnswer(1, '18–25')">18–25</button>
                <button onclick="saveAnswer(1, '26–35')">26–35</button>
                <button onclick="saveAnswer(1, '36–45')">36–45</button>
                <button onclick="saveAnswer(1, '46+')">46+</button>
                <button class="back-btn" onclick="goBack(1)">Back</button>
            </div>
            <div id="question-2" class="question">
                <h3>3. You’re planning a date night. What’s your pick?</h3>
                <button onclick="saveAnswer(2, 'Romantic')">A cozy dinner at a romantic restaurant</button>
                <button onclick="saveAnswer(2, 'Energetic')">Skydiving or bungee jumping</button>
                <button onclick="saveAnswer(2, 'Sophisticated')">A night at the opera or an art gallery opening</button>
                <button onclick="saveAnswer(2, 'Mysterious')">A mysterious dinner or magic show</button>
                <button onclick="saveAnswer(2, 'Social')">A lively party with friends and dancing</button>
                <button onclick="saveAnswer(2, 'Calm')">A quiet park stroll or meditation</button>
                <button class="back-btn" onclick="goBack(2)">Back</button>
            </div>
            <div id="question-3" class="question">
                <h3>4. What scent vibe do you gravitate toward?</h3>
                <button onclick="saveAnswer(3, 'Romantic')">Soft florals with a hint of sweetness</button>
                <button onclick="saveAnswer(3, 'Energetic')">Bold citrus with a zesty kick</button>
                <button onclick="saveAnswer(3, 'Sophisticated')">Deep woody or powdery notes</button>
                <button onclick="saveAnswer(3, 'Mysterious')">Mysterious spicy or smoky tones</button>
                <button onclick="saveAnswer(3, 'Social')">Fresh and light fruity vibes</button>
                <button onclick="saveAnswer(3, 'Calm')">Gentle herbal or oceanic notes</button>
                <button class="back-btn" onclick="goBack(3)">Back</button>
            </div>
            <div id="question-4" class="question">
                <h3>5. What inspires you most?</h3>
                <button onclick="saveAnswer(4, 'Romantic')">Love and close relationships</button>
                <button onclick="saveAnswer(4, 'Energetic')">New adventures and adrenaline</button>
                <button onclick="saveAnswer(4, 'Sophisticated')">Art and aesthetics</button>
                <button onclick="saveAnswer(4, 'Mysterious')">Mysteries and the unknown</button>
                <button onclick="saveAnswer(4, 'Social')">Hanging out and having fun with people</button>
                <button onclick="saveAnswer(4, 'Calm')">Peace and nature</button>
                <button class="back-btn" onclick="goBack(4)">Back</button>
            </div>
            <div id="question-5" class="question">
                <h3>6. How do you handle stress?</h3>
                <button onclick="saveAnswer(5, 'I lean on loved ones or treat myself to something sweet')">I lean on loved ones or treat myself to something sweet</button>
                <button onclick="saveAnswer(5, 'I hit the gym or chase a new challenge')">I hit the gym or chase a new challenge</button>
                <button onclick="saveAnswer(5, 'I dive into books or puzzles')">I dive into books or puzzles</button>
                <button onclick="saveAnswer(5, 'Stress? It doesn’t faze me')">Stress? It doesn’t faze me</button>
                <button class="back-btn" onclick="goBack(5)">Back</button>
            </div>
            <div id="question-6" class="question">
                <h3>7. How would you describe your style?</h3>
                <button onclick="saveAnswer(6, 'Romantic')">Soft and romantic</button>
                <button onclick="saveAnswer(6, 'Energetic')">Bold and dynamic</button>
                <button onclick="saveAnswer(6, 'Sophisticated')">Elegant and understated</button>
                <button onclick="saveAnswer(6, 'Mysterious')">Unique and intriguing</button>
                <button onclick="saveAnswer(6, 'Social')">Casual and friendly</button>
                <button onclick="saveAnswer(6, 'Calm')">Simple and comfy</button>
                <button class="back-btn" onclick="goBack(6)">Back</button>
            </div>
            <div id="question-7" class="question">
                <h3>8. What’s your favorite cuisine?</h3>
                <button onclick="saveAnswer(7, 'Italian or French')">Italian or French</button>
                <button onclick="saveAnswer(7, 'Mexican or Indian')">Mexican or Indian</button>
                <button onclick="saveAnswer(7, 'Japanese or sushi')">Japanese or sushi</button>
                <button onclick="saveAnswer(7, 'Comfort food like pizza or burgers')">Comfort food like pizza or burgers</button>
                <button onclick="saveAnswer(7, 'Salads or light dishes')">Salads or light dishes</button>
                <button class="back-btn" onclick="goBack(7)">Back</button>
            </div>
            <div id="question-8" class="question">
                <h3>9. What’s your favorite time of day?</h3>
                <button onclick="saveAnswer(8, 'Morning')">Morning</button>
                <button onclick="saveAnswer(8, 'Afternoon')">Afternoon</button>
                <button onclick="saveAnswer(8, 'Evening')">Evening</button>
                <button onclick="saveAnswer(8, 'Night')">Night</button>
                <button class="back-btn" onclick="goBack(8)">Back</button>
            </div>
            <div id="question-9" class="question">
                <h3>10. How do you spend your free time?</h3>
                <button onclick="saveAnswer(9, 'Reading books or watching movies')">Reading books or watching movies</button>
                <button onclick="saveAnswer(9, 'Working out or traveling')">Working out or traveling</button>
                <button onclick="saveAnswer(9, 'Hanging with friends')">Hanging with friends</button>
                <button onclick="saveAnswer(9, 'Relaxing at home or in nature')">Relaxing at home or in nature</button>
                <button class="back-btn" onclick="goBack(9)">Back</button>
            </div>
            <div id="result"></div>
        </div>
    </div>

    <style>
        body {
            font-family: 'Roboto', Arial, sans-serif;
            text-align: center;
            padding: 20px;
            background-color: #ffffff;
            color: #333;
        }
        #quiz {
            max-width: 800px;
            margin: 0 auto;
        }
        h1 {
            font-size: 28px;
            color: #1a1a1a;
            margin-bottom: 20px;
        }
        #start-btn {
            padding: 15px 40px;
            background-color: #d4af37;
            color: #fff;
            border: none;
            border-radius: 25px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.2s;
        }
        #start-btn:hover {
            background-color: #b8962e;
            transform: scale(1.05);
        }
        #progress-bar {
            width: 100%;
            background-color: #ddd;
            height: 10px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        #progress {
            width: 0%;
            height: 100%;
            background-color: #d4af37;
            border-radius: 5px;
            transition: width 0.3s ease;
        }
        .question {
            display: none;
            margin: 20px 0;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
        .question.active {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }
        button {
            margin: 5px;
            padding: 12px 25px;
            cursor: pointer;
            background-color: #d4af37;
            color: #fff;
            border: none;
            border-radius: 25px;
            font-size: 16px;
            transition: background-color 0.3s, transform 0.2s;
        }
        button:hover {
            background-color: #b8962e;
            transform: scale(1.05);
        }
        .back-btn {
            background-color: #666;
            color: #fff;
        }
        .back-btn:hover {
            background-color: #555;
        }
        #result {
            margin-top: 20px;
            background-color: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            text-align: left;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
        #result.active {
            opacity: 1;
            transform: translateY(0);
        }
        #result img {
            max-width: 200px;
            height: auto;
            margin: 10px 0;
            border-radius: 5px;
        }
        h2 {
            color: #d4af37;
            font-size: 24px;
            margin-bottom: 15px;
        }
        h3 {
            font-size: 20px;
            margin-bottom: 15px;
            color: #1a1a1a;
        }
        p {
            font-size: 16px;
            line-height: 1.5;
            color: #666;
        }
        .buy-btn {
            display: inline-block;
            margin-top: 15px;
            background-color: #1a1a1a;
            color: #d4af37;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 25px;
            font-size: 16px;
            transition: background-color 0.3s, color 0.3s;
        }
        .buy-btn:hover {
            background-color: #d4af37;
            color: #1a1a1a;
        }
    </style>

    <script>
        let currentQuestion = 0;
        const totalQuestions = 10;
        const userData = {
            gender: "",
            age: "",
            scores: {
                "Romantic": 0,
                "Energetic": 0,
                "Sophisticated": 0,
                "Mysterious": 0,
                "Social": 0,
                "Calm": 0
            },
            psychopathyIndicator: ""
        };

        const perfumes = [
            { name: "Baccara Rose Extrait", gender: "Unisex", personality: "Romantic", description: "A luxurious and deep scent that wraps you in warmth and coziness. Its complex composition reveals your tender soul, leaving a trail of elegance and love.", notes: "Rose, oud, amber", image: "https://i.etsystatic.com/56242195/r/il/e66b01/6463609540/il_600x600.6463609540_r5rb.jpg", url: "https://www.etsy.com/listing/1833163991/unisex-perfume-baccara-rose-extrait?click_key=df47f8a535a876ff1855dcb0323f1029237fb497%3A1833163991&click_sum=b8ab1213&ref=shop_home_active_16" },
            { name: "Bronze Fluidity", gender: "Men", personality: "Sophisticated", description: "An elegant and refined fragrance, like a tailored suit that highlights your style. It showcases your sophistication and confidence with a trail of understated luxury.", notes: "Almond, vanilla, vetiver", image: "https://i.etsystatic.com/56242195/r/il/ce4a7b/6480368412/il_600x600.6480368412_mpp4.jpg", url: "https://www.etsy.com/listing/1822815604/mens-perfume-bronze-fluidity-by-fantasy?click_key=740e80a1e1f49c1e3f9177e521fa61ff73186122%3A1822815604&click_sum=b642950d&ref=shop_home_active_7" },
            { name: "Chill Dr. Bro", gender: "Unisex", personality: "Calm", description: "A fresh and relaxing scent that brings harmony and peace. Its lightness perfectly mirrors your balanced nature, letting you savor every moment.", notes: "Hemp, bergamot, patchouli", image: "https://i.etsystatic.com/56242195/r/il/77bda7/6533274833/il_600x600.6533274833_7qer.jpg", url: "https://www.etsy.com/listing/1822819106/unisex-perfume-cill-dr-bro-extrait?click_key=65fb7d7ac4ae9dc72fbe0bcde003f7e063105ca3%3A1822819106&click_sum=28ad812e&ref=shop_home_active_6" },
            { name: "El Diablo", gender: "Unisex", personality: "Mysterious", description: "A bold and warm fragrance for those who live by their own rules. Its deep notes create an intriguing trail that highlights your mysterious and magnetic energy.", notes: "Coffee, rum, wood", image: "https://i.etsystatic.com/56242195/r/il/1a8fa7/6528519099/il_600x600.6528519099_4kik.jpg", url: "https://www.etsy.com/listing/1822825320/unisex-perfume-el-diablo-by-fantasy?click_key=c60602c1fcb81fd3425aaf8363329da83ea35d2f%3A1822825320&click_sum=91ba1c64&ref=shop_home_active_5" },
            { name: "Lime Crush", gender: "Unisex", personality: "Energetic", description: "A vibrant and uplifting scent that energizes your day. Its fresh and warm accords match your active, dynamic lifestyle perfectly.", notes: "Lime, mandarin, amber", image: "[ETSYS_IMAGE_URL]", url: "[ETSYS_URL]" },
            { name: "Mystical Blue Pepper", gender: "Men", personality: "Energetic", description: "A burst of energy that underscores your boldness and drive. This scent is your perfect companion for any adventure, offering freshness and strength.", notes: "Bergamot, pepper, cedar", image: "https://i.etsystatic.com/56242195/r/il/8a7fec/6463516158/il_600x600.6463516158_hxe4.jpg", url: "https://www.etsy.com/listing/1833153155/mystical-blue-pepper-extrait-bergamot?click_key=3451aff9315f90193cbcd31498d5395f8f991655%3A1833153155&click_sum=56b6b689&ref=shop_home_active_18" },
            { name: "Oasis", gender: "Unisex", personality: "Social", description: "An exotic and light fragrance that fills every day with joy. Its fresh notes reflect your sociable nature and love for connection.", notes: "Vetiver, flowers, citrus", image: "https://i.etsystatic.com/56242195/r/il/94d3fc/6511728901/il_600x600.6511728901_86f1.jpg", url: "https://www.etsy.com/listing/1833167355/unisex-perfume-oasis-by-fantasy?click_key=0d6c5e08cf2044e67989c23e3c0924e1e305e7eb%3A1833167355&click_sum=4ee0ddba&ref=shop_home_active_15" },
            { name: "Spicy Cherry Shike", gender: "Women", personality: "Mysterious", description: "A vibrant and seductive scent that draws people in with its depth. It perfectly highlights your mysterious allure, leaving a lasting impression.", notes: "Cherry, spices, amber", image: "https://i.etsystatic.com/56242195/r/il/e77c05/6526092843/il_600x600.6526092843_o6eo.jpg", url: "https://www.etsy.com/listing/1822228512/unisex-perfume-spicy-cherry-shake-by?click_key=ebe5883739e307ac67ae1d9d8b5b572a7a68e25a%3A1822228512&click_sum=e47d2fa5&ref=shop_home_active_28" },
            { name: "Spicy Spices", gender: "Unisex", personality: "Mysterious", description: "A warm and enigmatic scent that captivates with its depth. It’s made for those who love to intrigue and leave a memorable mark.", notes: "Tobacco, vanilla, spices", image: "https://i.etsystatic.com/56242195/r/il/757eb9/6526114663/il_600x600.6526114663_hw77.jpg", url: "https://www.etsy.com/listing/1822233828/unisex-perfume-spicy-spices-by-fantasy?click_key=0f17289146c64068594ea3e8973a2cb6c1b6daa2%3A1822233828&click_sum=1c0a7f3f&ref=shop_home_active_9" },
            { name: "Condensed Milk & Nutty Cookie", gender: "Women", personality: "Romantic", description: "A cozy and sweet scent that envelops you in warmth and tenderness. It mirrors your romantic soul with a touch of homey comfort.", notes: "Condensed milk, nuts, vanilla", image: "https://i.etsystatic.com/56242195/r/il/b32183/6477935754/il_600x600.6477935754_e1fb.jpg", url: "https://www.etsy.com/listing/1834176177/womens-perfume-condensed-milk-nutty?click_key=cf6e604fb4f1b18ac614407f06d6dbc864bd78ea%3A1834176177&click_sum=157560f1&ref=shop_home_active_14&crt=1" },
            { name: "Apricot Whisper Peony & Almond", gender: "Women", personality: "Romantic", description: "A romantic and elegant fragrance that highlights your softness. Its gentle notes create a trail filled with love and harmony.", notes: "Apricot, peony, almond", image: "https://i.etsystatic.com/56242195/r/il/5b5d77/6526039451/il_600x600.6526039451_hynn.jpg", url: "https://www.etsy.com/listing/1836414917/unisex-perfume-apricot-whisper-peony?click_key=b0883e056a04516f701e3c53b131768d4419e44d%3A1836414917&click_sum=d8121b26&ref=shop_home_active_13" },
            { name: "Citrus Breeze & Dark Rum", gender: "Men", personality: "Energetic", description: "A fresh and daring scent that boosts your energy. It’s perfect for your bold and dynamic spirit.", notes: "Citrus, rum, spices", image: "https://i.etsystatic.com/56242195/r/il/415779/6526052009/il_600x600.6526052009_1po5.jpg", url: "https://www.etsy.com/listing/1822218066/unisex-perfume-citrus-breeze-dark-rum?click_key=bda1e1a0dc9f5a1d9c576bb9ee7f31cf2a7519db%3A1822218066&click_sum=cbaf2b64&ref=shop_home_active_12" },
            { name: "Vanilla Sip & Sweet Caramel", gender: "Women", personality: "Romantic", description: "A warm and sweet scent that wraps you in tenderness. It highlights your sensitivity and love for cozy moments.", notes: "Vanilla, caramel, cream", image: "https://i.etsystatic.com/56242195/r/il/4d9d90/6477949832/il_600x600.6477949832_3zfx.jpg", url: "https://www.etsy.com/listing/1822219488/unisex-vanilla-sip-sweet-caramel-unisex?click_key=47affc00cea26bd22608247ba47a812b154afebd%3A1822219488&click_sum=5483fb84&ref=shop_home_active_11" },
            { name: "Frosty Berry & Bliss Cake", gender: "Women", personality: "Social", description: "A sweet and fresh scent that brings joy to every day. It perfectly reflects your fun and outgoing personality.", notes: "Berries, cake, amber", image: "https://i.etsystatic.com/56242195/r/il/bd8d7b/6526043177/il_600x600.6526043177_qtkh.jpg", url: "https://www.etsy.com/listing/1836415453/unisex-perfume-frosty-berry-bliss-cake?click_key=ebdd00dd4df4693ffcd2e97ac3af8bc69cb3e34d%3A1836415453&click_sum=70325c43&ref=shop_home_active_10" },
            { name: "Mango Milk Shake", gender: "Women", personality: "Social", description: "A bright and tender scent that radiates joy and warmth. It underscores your love for connection and ease in everything.", notes: "Mango, flowers, milk", image: "https://i.etsystatic.com/56242195/r/il/270d25/6526135127/il_600x600.6526135127_oq0p.jpg", url: "https://www.etsy.com/listing/1822238640/unisex-perfume-mango-milk-shake-by?click_key=fe800c7b522f2bf26239d519f5b5902ecbe3e2b8%3A1822238640&click_sum=8cf03f99&ref=shop_home_active_8" },
            { name: "Cola Honey Shake", gender: "Unisex", personality: "Social", description: "A warm and playful scent that brings happiness. It’s perfect for your friendly and open nature.", notes: "Cola, honey, spices", image: "https://i.etsystatic.com/56242195/r/il/d74ef4/6461246294/il_600x600.6461246294_rgoe.jpg", url: "https://www.etsy.com/listing/1818435472/unisex-perfume-cola-honey-shake-extrait?click_key=654cc3cdef0da99bdbe23acc7a49fc952f870b98%3A1818435472&click_sum=24ff3135&ref=shop_home_active_22" },
            { name: "Long Island", gender: "Women", personality: "Energetic", description: "A light and sweet scent that energizes you. It’s made for your active and joyful spirit.", notes: "Apple, vanilla, citrus", image: "https://i.etsystatic.com/56242195/r/il/87e031/6533270475/il_600x600.6533270475_eaxd.jpg", url: "https://www.etsy.com/listing/1822874228/unisex-perfume-long-island-by-fantasy?click_key=017b42d25b06759751af903da2af1c34047ec583%3A1822874228&click_sum=ccf1ccb6&ref=shop_home_active_21" },
            { name: "Tropical Ecstasy", gender: "Women", personality: "Social", description: "A fresh and warm scent that transports you to a tropical paradise. It highlights your love for fun and connection.", notes: "Tropical fruits, flowers, musk", image: "[ETSYS_IMAGE_URL]", url: "[ETSYS_URL]" },
            { name: "Watermelon Explosion", gender: "Women", personality: "Energetic", description: "A juicy and fresh scent that sparks positivity. It perfectly captures your energy and love for vibrant moments.", notes: "Watermelon, melon, citrus", image: "https://i.etsystatic.com/56242195/r/il/6f0e07/6485162620/il_600x600.6485162620_r0jm.jpg", url: "https://www.etsy.com/listing/1837070409/womens-perfume-watermelon-explosion-by?click_key=cfdb2d3d75743709766cd7424ea3d98d82aac19b%3A1837070409&click_sum=c938068b&ref=shop_home_active_1" },
            { name: "Cool Cucumber Shake", gender: "Unisex", personality: "Energetic", description: "A fresh and refined scent that invigorates and inspires. It highlights your activity and ease in every move.", notes: "Cucumber, cedar, mint", image: "https://i.etsystatic.com/56242195/r/il/15363b/6463590806/il_600x600.6463590806_3o8h.jpg", url: "https://www.etsy.com/listing/1818963768/unisex-perfume-cool-cucumber-shake?click_key=3d10f7688f11ca49b633c93e45241162be43d3eb%3A1818963768&click_sum=cd8e4dba&ref=shop_home_active_17" },
            { name: "Mandarino Verde", gender: "Men", personality: "Energetic", description: "A clean and fresh scent that delivers vitality and strength. It’s perfect for your energetic and bold personality.", notes: "Mandarin, tea, musk", image: "https://i.etsystatic.com/56242195/r/il/5eaad9/6528686059/il_600x600.6528686059_i78f.jpg", url: "https://www.etsy.com/listing/1837062879/unisex-perfume-mandarino-verde-by?click_key=301b787274394db7027badcb4121730a73105650%3A1837062879&click_sum=84bd6fea&ref=shop_home_active_3" },
            { name: "Pink Brut", gender: "Women", personality: "Social", description: "A bubbly and sweet scent that fills you with joy. It underscores your friendliness and love for lively moments.", notes: "Champagne, apricot, musk", image: "https://i.etsystatic.com/56242195/r/il/1c951d/6680114970/il_600x600.6680114970_aps5.jpg", url: "https://www.etsy.com/listing/1837067493/womens-perfume-pink-brut-by-fantasy?click_key=7b404ce827dcc329b57a8b8a4711c7cf93aef326%3A1837067493&click_sum=7e74a74d&ref=shop_home_active_2" },
            { name: "Confetteria", gender: "Women", personality: "Social", description: "A soft and sweet scent that brings warmth and happiness. It perfectly reflects your friendly and open nature.", notes: "Flowers, cream, sugar", image: "https://i.etsystatic.com/56242195/r/il/95f091/6463502254/il_600x600.6463502254_f4ci.jpg", url: "https://www.etsy.com/listing/1818946824/unisex-perfume-confettrria-by-fantasy?click_key=c11be0388736121792846075261fd9d4927f7864%3A1818946824&click_sum=be78d5ad&ref=shop_home_active_19" },
            { name: "Earl Grey", gender: "Unisex", personality: "Calm", description: "A fresh and refined scent that brings harmony. It’s perfect for your calm and balanced soul.", notes: "Bergamot, tea, cedar", image: "https://i.etsystatic.com/56242195/r/il/ae85c6/6485164624/il_600x600.6485164624_eqfh.jpg", url: "https://www.etsy.com/listing/1822832878/unisex-perfume-earl-gray-30ml-black-tea?click_key=1436c03f1648a8158b227ec5f6f1cb3b3dba8f5c%3A1822832878&click_sum=442c3af6&ref=shop_home_active_25" },
            { name: "Mad Jam", gender: "Women", personality: "Romantic", description: "The essence of romance and elegance, crafted for a tender soul. Its floral and warm trail highlights your sensitivity and natural charm.", notes: "Jasmine, amber, vanilla", image: "https://i.etsystatic.com/56242195/r/il/c3e47d/6480428210/il_600x600.6480428210_1iqh.jpg", url: "https://www.etsy.com/listing/1837027833/womens-perfume-mad-jam-by-fantasy?click_key=59712c7378ce724edcd0fc75edaa48a53db7c1b4%3A1837027833&click_sum=f7a63781&ref=shop_home_active_4" }
        ];

        const personalityDescriptions = {
            "Romantic": {
                female: "You’re a dreamer with a soft, tender heart. Your world is filled with love, comfort, and subtle emotions. You notice beauty in the little things—like flowers on the table or a warm glance from someone special. Your scent should be as gentle and enveloping as your soul.",
                male: "You’re a dreamer with a soft, tender heart. Your world is filled with love, comfort, and subtle emotions. You notice beauty in the little things—like flowers on the table or a warm glance from someone special. Your scent should be as gentle and enveloping as your soul."
            },
            "Energetic": {
                female: "You’re a force of nature, bursting with energy and a zest for life. Sitting still isn’t your thing—you’re always on the move, chasing adventures and shaking up the everyday. You need a scent that matches your drive and electrifies everyone around you.",
                male: "You’re a force of nature, bursting with energy and a zest for life. Sitting still isn’t your thing—you’re always on the move, chasing adventures and shaking up the everyday. You need a scent that matches your drive and electrifies everyone around you."
            },
            "Sophisticated": {
                female: "You’re the picture of elegance and taste. Your style is flawless, and your presence turns heads. You value art, harmony, and anything with depth. Your fragrance is a work of art that complements your refined vibe.",
                male: "You’re the picture of elegance and taste. Your style is flawless, and your presence turns heads. You value art, harmony, and anything with depth. Your fragrance is a work of art that complements your refined vibe."
            },
            "Mysterious": {
                female: "You’re an enigma worth unraveling. There’s something magnetic about you that draws eyes and sparks curiosity. You love a little intrigue and never show all your cards at once. Your scent is a mystery in every note.",
                male: "You’re an enigma worth unraveling. There’s something magnetic about you that draws eyes and sparks curiosity. You love a little intrigue and never show all your cards at once. Your scent is a mystery in every note."
            },
            "Social": {
                female: "You’re the life of the party, the one who lights up the room and makes every moment unforgettable. Friends are your element, and connecting is your art. Your fragrance should be light yet memorable to everyone around you.",
                male: "You’re the life of the party, the one who lights up the room and makes every moment unforgettable. Friends are your element, and connecting is your art. Your fragrance should be light yet memorable to everyone around you."
            },
            "Calm": {
                female: "You’re an oasis of peace and balance in a crazy world. You find joy in quiet moments, nature, and the simple things. Serenity and harmony are your vibe, and your scent is a soft breath of calm.",
                male: "You’re an oasis of peace and balance in a crazy world. You find joy in quiet moments, nature, and the simple things. Serenity and harmony are your vibe, and your scent is a soft breath of calm."
            }
        };

        document.getElementById("start-btn").addEventListener("click", function() {
            document.getElementById("start-screen").style.display = "none";
            document.getElementById("quiz-content").style.display = "block";
            showQuestion(0);
            updateProgress();
        });

        function saveAnswer(questionIndex, answer) {
            if (questionIndex === 0) userData.gender = answer;
            else if (questionIndex === 1) userData.age = answer;
            else if ((questionIndex >= 2 && questionIndex <= 4) || questionIndex === 6) userData.scores[answer] = (userData.scores[answer] || 0) + 1;
            else if (questionIndex === 5) userData.psychopathyIndicator = answer;

            document.getElementById(`question-${questionIndex}`).classList.remove("active");
            currentQuestion++;
            if (currentQuestion < totalQuestions) {
                showQuestion(currentQuestion);
            } else {
                showResult();
            }
            updateProgress();
        }

        function goBack(questionIndex) {
            document.getElementById(`question-${questionIndex}`).classList.remove("active");
            currentQuestion--;
            showQuestion(currentQuestion);
            updateProgress();
        }

        function showQuestion(index) {
            const question = document.getElementById(`question-${index}`);
            if (question) question.classList.add("active");
        }

        function updateProgress() {
            const progress = (currentQuestion / totalQuestions) * 100;
            document.getElementById("progress").style.width = `${progress}%`;
        }

        function showResult() {
            let resultPerfume, topTrait;
            let selfDiscoveryNote = "";
            let styleNote = "";
            let matchingPerfumes = [];

            if (userData.psychopathyIndicator === "Stress? It doesn’t faze me") {
                selfDiscoveryNote = userData.gender === "Man" 
                    ? "Your ability to shrug off stress is a real superpower! Maybe there’s a hidden strength in you that you haven’t fully tapped into yet." 
                    : "Your ability to shrug off stress is a real superpower! Maybe there’s a hidden strength in you that you haven’t fully tapped into yet.";
                matchingPerfumes = userData.gender === "Man" 
                    ? perfumes.filter(p => ["Mystical Blue Pepper", "El Diablo"].includes(p.name)) 
                    : perfumes.filter(p => ["El Diablo", "Spicy Cherry Shike", "Mad Jam"].includes(p.name));
                topTrait = "Mysterious";
            } else {
                topTrait = Object.keys(userData.scores).reduce((a, b) => userData.scores[a] > userData.scores[b] ? a : b);
                matchingPerfumes = perfumes.filter(p => 
                    (p.gender === userData.gender || p.gender === "Unisex") && 
                    p.personality === topTrait &&
                    (userData.gender === "Man" ? (p.name !== "Baccara Rose Extrait" && p.name !== "Oasis") : true)
                );
                selfDiscoveryNote = userData.gender === "Man" 
                    ? "Your soul shines through the little details. Have you noticed how effortlessly you create a vibe wherever you go?" 
                    : "Your soul shines through the little details. Have you noticed how effortlessly you create a vibe wherever you go?";
            }

            if (matchingPerfumes.length === 0) {
                matchingPerfumes = perfumes.filter(p => 
                    (userData.gender === "Man" ? (p.gender === "Men" || p.gender === "Unisex") : (p.gender === "Women" || p.gender === "Unisex")) &&
                    (userData.gender === "Man" ? (p.name !== "Baccara Rose Extrait" && p.name !== "Oasis") : true)
                );
            }

            if (matchingPerfumes.length === 0) {
                matchingPerfumes = perfumes;
            }

            resultPerfume = matchingPerfumes[Math.floor(Math.random() * matchingPerfumes.length)];

            const styleDescriptions = {
                "Romantic": {
                    female: "Your style is all about softness and romance: pastel tones, flowy fabrics, and accessories that highlight your sensitivity.",
                    male: "Your style is all about softness and romance: pastel tones, flowy fabrics, and accessories that highlight your sensitivity."
                },
                "Energetic": {
                    female: "Your style is a burst of color and bold combos: vibrant accents, sporty chic, and confidence in every step.",
                    male: "Your style is a burst of color and bold combos: vibrant accents, sporty chic, and confidence in every step."
                },
                "Sophisticated": {
                    female: "Your style is elegance and restraint: classic silhouettes, quality materials, and a keen eye for detail.",
                    male: "Your style is elegance and restraint: classic silhouettes, quality materials, and a keen eye for detail."
                },
                "Mysterious": {
                    female: "Your style is intrigue and depth: dark hues, unique textures, and accessories that turn heads.",
                    male: "Your style is intrigue and depth: dark hues, unique textures, and accessories that turn heads."
                },
                "Social": {
                    female: "Your style is freedom and playfulness: casual with a trendy twist, bright details, and comfort all the way.",
                    male: "Your style is freedom and playfulness: casual with a trendy twist, bright details, and comfort all the way."
                },
                "Calm": {
                    female: "Your style is harmony and simplicity: natural tones, comfy cuts, and nothing over the top.",
                    male: "Your style is harmony and simplicity: natural tones, comfy cuts, and nothing over the top."
                }
            };

            const personalityDescription = userData.gender === "Man" ? personalityDescriptions[topTrait].male : personalityDescriptions[topTrait].female;
            styleNote = userData.gender === "Man" ? styleDescriptions[topTrait].male : styleDescriptions[topTrait].female;

            document.getElementById("result").innerHTML = `
                <h2>Your Perfect Scent: ${resultPerfume.name}</h2>
                <img src="${resultPerfume.image}" alt="${resultPerfume.name}" onerror="this.src='https://via.placeholder.com/200x300?text=No+Image'">
                <p><strong>Scent Description:</strong> ${resultPerfume.description} This fragrance is your trusty sidekick, bringing out what makes you, you.</p>
                <p><strong>Key Notes:</strong> ${resultPerfume.notes} — these notes feel like they were made just for you!</p>
                <p><strong>Your Personality:</strong> ${personalityDescription}</p>
                <p><strong>Your Style:</strong> ${styleNote}</p>
                <p><strong>A Little Self-Discovery:</strong> ${selfDiscoveryNote}</p>
                <a href="${resultPerfume.url}" class="buy-btn">Shop ${resultPerfume.name} on Etsy</a>
                <button onclick="restartQuiz()">Try Again</button>
            `;
            document.getElementById("result").classList.add("active");
        }

        function restartQuiz() {
            currentQuestion = 0;
            userData.gender = "";
            userData.age = "";
            userData.scores = {"Romantic": 0, "Energetic": 0, "Sophisticated": 0, "Mysterious": 0, "Social": 0, "Calm": 0};
            userData.psychopathyIndicator = "";
            document.getElementById("result").classList.remove("active");
            document.getElementById("quiz-content").style.display = "block";
            showQuestion(0);
            updateProgress();
        }
    </script>
</body>
</html>
