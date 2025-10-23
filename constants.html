<!DOCTYPE html>
<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Control de Constants Vitals (Actualitzat)</title>
    <style>
        /* Estil general de la pàgina */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #f4f7f6;
            color: #333;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        /* Contenidor principal */
        .container {
            width: 100%;
            max-width: 500px;
            background-color: #ffffff;
            padding: 25px 30px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }

        h1 {
            text-align: center;
            color: #005a9c;
            margin-top: 0;
            margin-bottom: 25px;
        }

        /* Estil per a cada grup d'entrada (mètrica) */
        .metric {
            margin-bottom: 20px;
        }

        .metric label {
            display: block;
            font-weight: 600;
            margin-bottom: 5px; 
        }
        
        .range-info {
            font-size: 0.85rem;
            color: #555;
            margin-top: 0;
            margin-bottom: 10px;
        }

        .metric input[type="number"] {
            width: 100px;
            padding: 8px 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
            box-sizing: border-box; 
        }
        
        /* Grup especial per la Tensió Arterial */
        .ta-group {
            display: flex;
            gap: 15px;
            align-items: center;
        }
        
        .ta-group div {
            flex-grow: 1;
        }
        
        .ta-group input {
            width: 100% !important; 
        }

        /* Estil per als resultats de text */
        .result {
            margin-left: 15px;
            font-size: 1.1rem;
            font-weight: bold;
            padding: 5px 8px;
            border-radius: 4px;
        }

        /* Classes de color per als resultats */
        .normal {
            color: #1e6600;
            background-color: #e8f5e9; /* Verd clar */
        }

        .anormal {
            color: #b71c1c;
            background-color: #ffebee; /* Vermell clar */
        }

        /* Estil del botó */
        button {
            display: block;
            width: 100%;
            padding: 12px;
            font-size: 1.1rem;
            font-weight: bold;
            color: #fff;
            background-color: #007bff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 25px;
            transition: background-color 0.2s;
        }

        button:hover {
            background-color: #0056b3;
        }
        
        /* Avís legal */
        .disclaimer {
            font-size: 0.8rem;
            color: #777;
            text-align: center;
            margin-top: 25px;
            border-top: 1px solid #eee;
            padding-top: 15px;
        }

    </style>
</head>
<body>

    <div class="container">
        <h1>Control de Constants Vitals</h1>

        <div class="metric">
            <label for="fc">Freqüència Cardíaca (batecs per minut):</label>
            <p class="range-info">Rang normal (adult en repòs): 60 - 100 bpm</p>
            <input type="number" id="fc" placeholder="Ex: 70">
            <span id="result-fc" class="result"></span>
        </div>

        <div class="metric">
            <label for="spo2">Saturació d'Oxigen (SpO₂ %):</label>
            <p class="range-info">Rang normal: 95% - 100%</p>
            <input type="number" id="spo2" placeholder="Ex: 98">
            <span id="result-spo2" class="result"></span>
        </div>

        <div class="metric">
            <label for="fr">Freqüència Respiratòria (respiracions per minut):</label>
            <p class="range-info">Rang normal (adult en repòs): 12 - 20 rpm</p>
            <input type="number" id="fr" placeholder="Ex: 16">
            <span id="result-fr" class="result"></span>
        </div>
        
        <div class="metric">
            <label for="glicemia">Glicèmia Capil·lar (mg/dL) (en dejú):</label>
            <p class="range-info">Rang normal (en dejú): 70 - 130 mg/dL</p>
            <input type="number" id="glicemia" placeholder="Ex: 90">
            <span id="result-glicemia" class="result"></span>
        </div>

        <div class="metric">
            <label>Tensió Arterial (Sistòlica / Diastòlica):</label>
            <p class="range-info">Rang normal: 90-145 / 60-85 mmHg</p>
            <div class="ta-group">
                <div>
                    <input type="number" id="ta-sistolica" placeholder="Sistòlica (Ex: 110)">
                </div>
                <span>/</span>
                <div>
                    <input type="number" id="ta-diastolica" placeholder="Diastòlica (Ex: 70)">
                </div>
            </div>
            <span id="result-ta" class="result" style="margin-left: 0; margin-top: 10px; display: inline-block;"></span>
        </div>

        <button id="checkButton">Comprovar Valors</button>
        
        <p class="disclaimer">
            <strong>Avís:</strong> Aquests valors són orientatius per a adults en repòs i no substitueixen una avaluació mèdica. Consulta sempre un professional sanitari.
        </p>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const checkButton = document.getElementById('checkButton');
            checkButton.addEventListener('click', function() {
                comprovarConstants();
            });
        });

        // Funció principal que s'executa en fer clic
        function comprovarConstants() {
            
            // 1. FREQÜÈNCIA CARDÍACA (FC)
            // Valors normals: 60 - 100 bpm (en repòs)
            const fc = parseFloat(document.getElementById('fc').value);
            const resultFC = document.getElementById('result-fc');
            if (fc >= 60 && fc <= 100) {
                setResult(resultFC, 'Normal', 'normal');
            } else if (fc) { 
                setResult(resultFC, 'Anormal', 'anormal');
            } else {
                clearResult(resultFC); 
            }

            // 2. SATURACIÓ D'OXIGEN (SpO₂)
            // Valors normals: 95% - 100%
            const spo2 = parseFloat(document.getElementById('spo2').value);
            const resultSpo2 = document.getElementById('result-spo2');
            if (spo2 >= 95 && spo2 <= 100) {
                setResult(resultSpo2, 'Normal', 'normal');
            } else if (spo2) {
                setResult(resultSpo2, 'Anormal', 'anormal');
            } else {
                clearResult(resultSpo2);
            }

            // 3. FREQÜÈNCIA RESPIRATÒRIA (FR)
            // Valors normals: 12 - 20 rpm
            const fr = parseFloat(document.getElementById('fr').value);
            const resultFR = document.getElementById('result-fr');
            if (fr >= 12 && fr <= 20) {
                setResult(resultFR, 'Normal', 'normal');
            } else if (fr) {
                setResult(resultFR, 'Anormal', 'anormal');
            } else {
                clearResult(resultFR);
            }
            
            // 4. GLICÈMIA CAPIL·LAR (en dejú)
            // Valors normals: 70 - 130 mg/dL (Segons sol·licitud)
            const glicemia = parseFloat(document.getElementById('glicemia').value);
            const resultGlicemia = document.getElementById('result-glicemia');
            if (glicemia >= 70 && glicemia <= 130) { 
                setResult(resultGlicemia, 'Normal', 'normal');
            } else if (glicemia) {
                setResult(resultGlicemia, 'Anormal', 'anormal');
            } else {
                clearResult(resultGlicemia);
            }

            // 5. TENSIÓ ARTERIAL (TA)
            // === VALORS ACTUALITZATS SEGONS SOL·LICITUD ===
            // Rang normal: Sistòlica 90-145 I Diastòlica 60-85
            const sis = parseFloat(document.getElementById('ta-sistolica').value);
            const dia = parseFloat(document.getElementById('ta-diastolica').value);
            const resultTA = document.getElementById('result-ta');
            
            if (sis && dia) {
                // === LÍNIES ACTUALITZADES ===
                if ((sis >= 90 && sis <= 145) && (dia >= 60 && dia <= 85)) {
                    setResult(resultTA, 'Normal', 'normal');
                } else {
                    setResult(resultTA, 'Anormal', 'anormal');
                }
            } else {
                 clearResult(resultTA);
            }
        }
        
        // Funció auxiliar per posar el resultat i el color
        function setResult(element, text, className) {
            element.textContent = text;
            element.className = 'result ' + className;
        }
        
        // Funció auxiliar per esborrar el resultat
        function clearResult(element) {
            element.textContent = '';
            element.className = 'result';
        }

    </script>

</body>
</html>
