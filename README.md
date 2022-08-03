# Temp-Converter
Create a Celsius to  Fahrenheit converter using HTML, CSS and JS

Just made a Celcius to Fahrenheit and Fahrenheit to Celsius converter, as a beginning project fo web-fundamentals.

<!DOCTYPE html>
<html>
    <style>
        body {
            background-color: maroon;
        }
        h1 {
            text-align: center;
            text-decoration: wavy;
            color: goldenrod;
            margin-bottom: 40px;
            
        }
        form {
            width: 400px;
            height: 300px;
            padding: 40px 0 0px 60px;
            margin: auto;
            background-color: whitesmoke;
            box-sizing: border-box;
            box-shadow: 0px 0px 2px 9px whitesmoke;
            margin-top: 20px;
            border-radius: 20px;
        }
        input {
            border-radius: 15px;
            border: 2px solid #3c4043;
            font-size: 18px;
            line-height: 1.5;
            outline: none;
            font-weight: bold;
            /* color: #FFFFFF; */
            padding: 5px 10px;
            background-color: #303134;
            color: goldenrod;
        }
        label {
            font-family: Georgia, 'Times New Roman', Times, serif;
            font-size: 24px;
            font-weight: 900;
            color: maroon;
        }
        footer {
            position: fixed;
            bottom: 0;
            left: 0;
            background-color: aliceblue;
            color: black;
            font-weight: 600;
            width: 100%;
            height: 40px;
            font-size: 24px;
            text-align: center;
        }
        em {
            text-decoration: underline;
        }

        #reset {
            display: block;
        }
    </style>
<body>
    <h1>Temperature Converter</h1>
    <form>
        <label for="celcius">Celcius:</label><br />
        <input type="number" id="celcius" value="0"><br />
        <br />
        <label for="fahr">Fahrenheit:</label><br />
        <input type="number" id="fahr" value="32"><br />
        <br />
        <input type="reset" id="reset">
    </form>
    <footer>by <em><b>Sai Vignesh</b></em></footer>
</body>
<script>
    window.onload = function() {
        let c = document.getElementById("celcius");
        let f = document.getElementById("fahr");

        c.oninput = function() {
            f.value = (c.value*9/5) + 32;
        };

        f.oninput = function() {
            c.value = (f.value - 32) * (5/9);
        };
    };
</script>
</html>
