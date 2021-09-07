# weather_app
#html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="Author" content="Dassah">
    <meta name="Description" content="Group II Weather App">
    <title>Weather-App</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://kit.fontawesome.com/6392c1211e.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700;900&display=swap" rel="stylesheet">
    <script src="script.js" defer></script>

</head>
<body>
    <div class="Search">
        <input type="text" class="Searchbar" placeholder="Search">
        <button><i class="fas fa-search-location"></i></button>
    </div>
    <div class="Card Loading">
        <div class="Card-1">
            <div class="part1">
                <h2 class="Day">Monday</h2>
                <div class="Date">07 September 2021</div>
                <div class="Location">
                    <i class="fas fa-map-marker-alt"></i>
                    <span class="City">Lagos, NG</span>
                </div>
            </div>
            <div class="part2">
                <img src="https://openweathermap.org/img/wn/04n.png" alt="" class="icon" height="90px" width="90px" />
                <h1 class="Temp">30°C</h1>
                <div class="Description">Sunny</div>
            </div>
        </div>

        <div class="Card-2">
            <table cellpadding="4">
                <tr>
                    <td>FEELS LIKE</td>
                    <td>35°C</td>
                </tr>
                <tr>
                    <td>PRECIPITATION</td>
                    <td>65 %</td>
                </tr>
                <tr>
                    <td>HUMIDITY</td>
                    <td>77%</td>
                </tr>
                <tr>
                    <td>WIND</td>
                    <td>11 km/h</td>
                </tr>
            </table>

            <div class="Weekdays">
                <div class="Days One">
                    <img src="https://openweathermap.org/img/wn/04n.png" alt="" class="icon" />
                    <p id="d1">Tue</p>
                    <p id="t1">32°C</p>
                </div>
                <div class="Days Two">
                    <img src="https://openweathermap.org/img/wn/04n.png" alt="" class="icon" />
                    <p id="d2">Wed</p>
                    <p id="t2">27°C</p>
                </div>
                <div class="Days Three">
                    <img src="https://openweathermap.org/img/wn/04n.png" alt="" class="icon" />
                    <p id="d3">Thur</p>
                    <p id="t3">10°C</p>
                </div>
                <div class="Days Four">
                    <img src="https://openweathermap.org/img/wn/04n.png" alt="" class="icon" />
                    <p id="d4">Fri</p>
                    <p id="t4">21°C</p>
                </div>
            </div>
        </div>
    </div>

</body>
</html>
