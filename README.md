<!DOCTYPE html>
<html lang="sw">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kampeni ya Pepsi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: auto;
        }
        h1 {
            color: #005CBF;
        }
        input[type="text"], input[type="number"] {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        input[type="submit"] {
            background-color: purple;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: purple;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Kuza Pesa</h1>
        <p>Weka pesa ushinde zawadi kubwa!</p>
        
        <form action="/submit-donation" method="post">
            <label for="name">Jina lako:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            
            <label for="amount">Kiasi cha pesa (Tsh):</label><br>
            <input type="number" id="amount" name="amount" required><br><br>
            
            <input type="submit" value="Changia Sasa">
        </form>
        
        <p>Kwa kila shilingi unayoweka, unapata nafasi ya kushinda pesa zaidi!</p>
        
        <!-- Sehemu ya kuangalia kiasi cha pesa -->
        <h2>Angalia Salio Lako</h2>
        <form action="/check-balance" method="post">
            <label for="check-name">Jina lako:</label><br>
            <input type="text" id="check-name" name="check-name" required><br><br>
            
            <input type="submit" value="Angalia Salio">
        </form>
        
        <!-- Sehemu ya kutoa pesa -->
        <h2>Toa Pesa</h2>
        <form action="/withdraw" method="post">
            <label for="withdraw-name">Jina lako:</label><br>
            <input type="text" id="withdraw-name" name="withdraw-name" required><br><br>
            
            <input type="submit" value="Toa Pesa" disabled>
            <!-- Button ya 'Toa Pesa' itadhibitiwa na server -->
        </form>
        
        <p>Utaweza kutoa pesa pale tu salio lako litakapokuwa limeidhinishwa na server.</p>
    </div>

</body>
</html>
