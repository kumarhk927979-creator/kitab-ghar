========================================
KITAB GHAR — AAPKI BOOKS KI WEBSITE
Kaise use karein (bilkul aasan, koi coding nahi)
========================================

Is folder mein 2 cheezein hain:
  1. index.html   <- yeh aapki poori website hai
  2. README.txt   <- yeh file (padhne ke liye)

PRICING KA TARIKA (naya):
  Aap har book ka ONLINE PRICE (Flipkart/Amazon ka aaj ka daam) daalte hain.
  Website usse khud 20% kam kar ke aapka price dikhati hai.
  Delivery charge alag se dikhta hai ("Delivery charges extra").
  Aap chahein to 20% ki jagah koi bhi number rakh sakte hain (STEP 1 dekhein).


----------------------------------------
STEP 0 — SABSE PEHLE: WEBSITE DEKHEIN
----------------------------------------
index.html par double-click karein. Website browser (Chrome) mein
khul jayegi. Yehi aapki website hai.


----------------------------------------
STEP 1 — APNI DETAILS BADLEIN
----------------------------------------
index.html ko Notepad (ya kisi bhi text editor) mein kholein.
Sabse upar "STEP 1" likha milega. Uske neeche:

    const SHOP = {
      name: "Kitab Ghar",
      tagline: "Used books · NCERT & JEE",
      whatsapp: "919942849146",
      discountPercent: 20,
      deliveryNote: "Delivery charges extra",
      heroLead: "..."
    };

- name            : apni shop ka naam
- tagline         : chhoti line jo header mein dikhti hai
- whatsapp        : APNA WhatsApp number, country code ke saath, bina + aur space.
                    Jaise 98765 43210 ke liye likhein: 919876543210  (91 = India)
- discountPercent : online price se kitne percent kam. Abhi 20. Badalna ho to
                    number badal dein (jaise 25).
- deliveryNote    : card par dikhne wali delivery line.
                    Aap chunte hain — jaise "Delivery ₹50 extra" ya
                    "Delivery extra (₹40–₹80 by city)".

Sirf " " ke andar wala text badlein. Quotes (" ") hatayein nahi.


----------------------------------------
STEP 2 — APNI BOOKS ADD KAREIN
----------------------------------------
Usi file mein "STEP 2" ke neeche "const BOOKS = [ ... ]" hai.
Yahan har book ek block hai, aise:

    {
      title: "NCERT Physics — Class 12 (Part 1)",
      author: "NCERT",
      category: "NCERT",
      condition: "Very good",
      onlinePrice: 300,
      ourPrice: null,
      image: "",
      note: "No writing inside. Cover slightly worn."
    },

- title       : book ka naam
- author      : lekhak / publisher (NCERT, H. C. Verma, etc.)
- category    : "NCERT" ya "JEE"  (naya category bhi likh sakte hain)
- condition   : "Like new" / "Very good" / "Good" / "Fair"
- onlinePrice : aaj Flipkart/Amazon par jo daam hai (sirf number, jaise 450)
- ourPrice    : KHAALI chhodein (null) to 20% discount khud lag jayega.
                Ya khud apna price likh dein, jaise 340.
- image       : apni photo ka naam (STEP 3 dekhein)
- note        : chhoti detail (optional). Khaali ho to "" likhein

Nayi book add karne ke liye block copy karke comma ke saath paste karein.
Book hatani ho to uska pura { ... } block delete kar dein.


----------------------------------------
STEP 3 — APNI PHOTOS ADD KAREIN
----------------------------------------
SABSE AASAN TARIKA (recommended):
  Photo mujhe bhej dein (WhatsApp/chat par). Main usse website ke
  andar hi daal deta hoon. Isse website ek hi file mein poori rah jaati
  hai aur photo HAR JAGAH dikhti hai — preview mein bhi, hosting par bhi.
  Aapko kuch nahi karna padta.

  Kyun: agar photo alag "images" folder mein rakhein, to kuch jagah
  (jaise link preview) photo load nahi hoti. Isliye main photo ko
  file ke andar embed karta hoon — 100% bharosemand.

KHUD KARNA HO (advanced, Netlify hosting ke saath):
  1. is folder ke andar ek folder banayein:  images
  2. Photos us folder mein daalein, naam aasan rakhein (ncert-phy-12.jpg)
  3. index.html mein us book ke "image" mein likhein:
         image: "images/ncert-phy-12.jpg"
  Photo khaali chhodi (image: "") to "Photo coming soon" box dikhega.

Tip: Phone se acchi roshni mein, book seedhi rakh kar photo khinchein.
Photo ki zaroorat nahi to mujhe bhej dein — main sahi size mein
compress karke laga dunga (bhaari photo site ko slow karti hai).


----------------------------------------
STEP 4 — WEBSITE KO INTERNET PAR LIVE KAREIN (FREE)
----------------------------------------
Ab website sirf aapke computer par hai. Duniya ko dikhane ke liye
free host karein. Sabse aasan — Netlify Drop:

  1. Computer par ek folder banayein:  my-books-website
  2. Usme daalein:  index.html  aur  images folder
  3. Browser mein kholein:  https://app.netlify.com/drop
  4. Poora folder us page par DRAG karke chhod dein.
  5. Kuch second mein website live ho jayegi aur ek link milega,
     jaise:  https://random-name-123.netlify.app
  6. Woh link WhatsApp status, Instagram bio, ya juniors ko bhej dein.

Free plan ka link hamesha chalta rahega. Naam badalna ho to Netlify ke
"Site settings" mein ja kar badal sakte hain (jaise aman-ki-books.netlify.app).


----------------------------------------
KAISE UPDATE KAREIN
----------------------------------------
1. index.html mein STEP 2 mein book add karein ya price badlein.
2. File save karein (Ctrl + S).
3. Netlify par: "Deploys" -> "Drag and drop" -> folder dobara drag karein.
   Nayi version turant live. (Bina hosting ke, browser refresh F5 se bhi dikhega.)


----------------------------------------
CHHOTI CHHOTI ZAROORI BAATEIN
----------------------------------------
- Book bik gayi? Uska block hata dein, ya "sold: true" likh dein
  (yeh feature abhi nahi hai — bikne par block hata dena best hai).
- Website mobile par bhi acchi dikhti hai — buyers phone se dekhenge.
- Buyer ka message seedha aapke WhatsApp par aayega. Aap reply karein.
- Paisa: cash ya UPI, book handover ke waqt. Website par payment nahi hota.
- Delivery charge aap WhatsApp par location dekh kar confirm karein.
- Koi problem ho to bata dein, main theek kar dunga.


----------------------------------------
AGAR AAP CHAHEIN (aage ke options)
----------------------------------------
- SOLD badge aur "1 left" jaise tags
- Search box (book ke naam se dhoondhna)
- Photo gallery (ek book ki 2-3 photos)
- Delivery charge ka alag section (city-wise rates)
- UPI QR code
- Instagram / YouTube link
Jo chahiye bas bol dein.
