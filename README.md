# wcxncj4zp6-sys.github.io
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentinstag Frage</title>
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
        text-align: center;
        background: #ffe6e8;
        color: #333;
    }
    .container {
        margin-top: 80px;
    }
    img {
        width: 180px;
        height: auto;
    }
    h1 {
        font-size: 28px;
        margin-top: 20px;
    }
    button {
        margin: 15px;
        padding: 14px 30px;
        font-size: 20px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        transition: transform 0.2s ease;
    }
    #btnYes {
        background: #ff5c8d;
        color: white;
    }
    #btnNo {
        background: #b0b0b0;
        color: white;
    }
    .hidden {
        display: none;
    }
    #celebrateImg {
        width: 280px;
        margin-top: 30px;
    }
    #juhuText {
        font-size: 32px;
        margin-top: 18px;
        color: #e6004c;
    }
</style>
</head>
<body>
    <div class="container">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Red_Heart.svg" alt="Herz">
        <h1>Willst du mein Valentinstagsdate sein?</h1>

        <button id="btnYes">Ja</button>
        <button id="btnNo">Nein</button>

        <div id="result" class="hidden">
            <img id="celebrateImg" src="https://media.giphy.com/media/3oEjI6SIIHBdRxXI40/giphy.gif" alt="Feuerwerk">
            <div id="juhuText">Juhuuu! ❤️</div>
        </div>
    </div>

<script>
    const btnYes = document.getElementById("btnYes");
    const btnNo = document.getElementById("btnNo");
    const resultDiv = document.getElementById("result");

    // Größe des Ja-Buttons
    let scale = 1;

    btnNo.addEventListener("click", () => {
        scale += 0.3;
        btnYes.style.transform = "scale(" + scale + ")";
        
        // wenn Ja groß genug ist → Nein ausblenden
        if (scale > 2.5) {
            btnNo.style.display = "none";
        }
    });

    btnYes.addEventListener("click", () => {
        btnYes.style.display = "none";
        btnNo.style.display = "none";
        resultDiv.classList.remove("hidden");
    });
</script>

</body>
</html>
