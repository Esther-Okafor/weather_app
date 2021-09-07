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

#css
html {
    font-family: 'Roboto', sans-serif;
    color: white;
    font-size: 20px;
    width: 100%;
    height: 100%;
}

.Search {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 12px auto;
}

button {
    margin: 0.3rem;
    width: 1.7rem;
    height: 1.7rem;
    border-radius: 50%;
    background: #3b3d54;
    color: white;
    border: none;
    outline: none;
    transition: background 0.1s ease-in-out;
}

.Searchbar:hover {
    box-shadow: 2px 2px 5px rgba(0,0,0,0.7);
}

button:hover {
    background: #4c4f69;
    cursor: pointer;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.7);
}

input {
    border: none;
    outline: none;
    padding: 0.2rem 1rem;
    border-radius: 15px;
    background: #3b3d54;
    color: white;
    font-family: inherit;
    font-size: 105%;
}


.Card {
    display: flex;
    margin: 12px 20rem;
    width: auto;
    height: auto;
}

.Card-1 {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    border-radius: 25px;
    width: 24rem;
    height: 26rem;
    flex-grow: 1;
    padding: 0.5rem;
    position: relative;
    box-shadow: 3px 3px 20px rgba(0,0,0,0.7);
    text-shadow: #000 1px 0 25px;
    transition: transform 500ms ease;
}
.Card-1::after {
    content: "";
    border-radius: 25px;
    background: var(--background);
    background-position: center;
    background-repeat: no-repeat;
    filter: brightness(90%);
    opacity: 0.92;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    position: absolute;
    z-index: -1;   
}

.Card-2 {
    border-radius: 25px;
    width: 24rem;
    height: 26rem;
    flex-grow: 1;
    padding: 0.5rem;
    transition: width 0.2s, height 0.2s;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    position: relative;
    box-shadow: 3px 3px 20px rgba(0,0,0,0.7);
    transition: transform 500ms ease;
}

.Card-2::after {
    content:"";
    border-radius: 25px;
    background-color: #252836;
    opacity: 0.92;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    position: absolute;
    z-index: -1;
}

.Card-1:hover, .Card-2:hover {
    transform: scale(1.05);
}  

.Day {
    margin-bottom: 0px;
    padding-bottom: 0px;
    font-size: 2rem;
    margin-left: 15px;
}

.Date {
    margin-top: none;
    padding-top: none;  
    margin-left: 15px;
}  
.Location {
    margin-top: 15px;
    margin-left: 5px;
    font-size: 22px;
}

.Card-1 i, .icon {
    margin-left: 15px;
    margin-bottom: 0px;
}

.Temp {
    margin-left: 15px;
    margin-top: 0px;
    padding-top: 0px;
    margin-bottom: 0px;
    font-size: 4rem;
}

.Description {
    font-size: 1.4rem;
    font-weight: bold;
    margin-left: 20px;
    margin-bottom: 10px;
}

table {
    margin: 1.2rem;
    margin-top: 2rem;
    margin-bottom: 2rem;
}

tr td:nth-child(1) {
    font-weight: bold;
    text-align: left;
}

tr td:nth-child(2) {
    text-align: right;
    width: 90%;
}

.Weekdays {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    border-radius: 1rem;
    background-color: #303445;
    width: auto;
    height: auto;
    margin: auto;
}

.Days {
    padding: 0.2rem;
    border-radius: 1rem;
    padding-top: 1rem;
    flex-direction: column;
    text-align: center;
    background-color: #303445;
    transition: background-color 300ms ease;
}

.Days:hover {
    background-color: whitesmoke;
    color: #303445;
    border-radius: 1rem;
    cursor: pointer;
}

.Days:hover img {
    filter: invert(1);
}

.Card.Loading {
    visibility: hidden;
    max-height: 20px;
    position: relative;
}

.Card.Loading::after {
    visibility: visible;
    content: "Loading...";
    color: white;
    position: absolute;
    top: 0;
}

#javascript
let D = null;

let weather = {
    "apiKey": "dea886ab571fa9ba5defd3fe2cb73358",
    fetchWeather: function(city) {
        fetch("https://api.openweathermap.org/data/2.5/forecast?q=" 
        + city 
        + "&units=metric&appid=" 
        + this.apiKey
        )
            .then((response) => response.json())
            .then((data) => {D = data; this.displayWeather(data, 1);});
    },
    displayWeather: function(data, DayNumber) {
        const cityname = data.city.name;
        const country = data.city.country;
        // DAY 1
        let date1 = data.list[0].dt_txt;
        const icon1 = data.list[0].weather[0].icon;
        const description1 = data.list[0].weather[0].description;
        const temp1 = data.list[0].main.temp;
        const humidity1 = data.list[0].main.humidity;
        const speed1 = Math.round((Number(data.list[0].wind.speed) * 3.6) * 100) / 100;
        const pop1 = data.list[0].pop;
        const main1 = data.list[0].weather[0].main;
        // DAY 2
        let date2 = data.list[7].dt_txt;
        const icon2 = data.list[7].weather[0].icon;
        const description2 = data.list[7].weather[0].description;
        const temp2 = data.list[7].main.temp;
        const humidity2 = data.list[7].main.humidity;
        const speed2 = Math.round((Number(data.list[7].wind.speed) * 3.6) * 100) / 100;
        const pop2 = data.list[7].pop;
        const main2 = data.list[7].weather[0].main;
        // DAY 3
        let date3 = data.list[15].dt_txt;
        const icon3 = data.list[15].weather[0].icon;
        const description3 = data.list[15].weather[0].description;
        const temp3 = data.list[15].main.temp;
        const humidity3 = data.list[15].main.humidity;
        const speed3 = Math.round((Number(data.list[15].wind.speed) * 3.6) * 100) / 100;
        const pop3 = data.list[15].pop;
        const main3 = data.list[15].weather[0].main;
        // DAY 4
        let date4 = data.list[23].dt_txt;
        const icon4 = data.list[23].weather[0].icon;
        const description4 = data.list[23].weather[0].description;
        const temp4 = data.list[23].main.temp;
        const humidity4 = data.list[23].main.humidity;
        const speed4 = Math.round((Number(data.list[23].wind.speed) * 3.6) * 100) / 100;
        const pop4 = data.list[23].pop;
        const main4 = data.list[23].weather[0].main;

        let months   = ['', 'January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];

        function dateList(date) {
            let myarr1 = date.split(" ");
            date = myarr1[0];
            let myArr2 = date.split("-");
            let year = myArr2[0]
            let month = months[Number(myArr2[1])];
            let d = myArr2[2];
            return [d, month, year];
        }

        let arr1 = dateList(date1);
        let d = new Date(`${arr1[0]} ${arr1[1]}, ${arr1[2]}`);

        let arr2 = dateList(date2);
        let dx = new Date(`${arr2[0]} ${arr2[1]}, ${arr2[2]}`);

        let arr3 = dateList(date3);
        let dy = new Date(`${arr3[0]} ${arr3[1]}, ${arr3[2]}`);

        let arr4 = dateList(date4);
        let dz = new Date(`${arr4[0]} ${arr4[1]}, ${arr4[2]}`);

        let weekday = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
        let day1 = weekday[d.getDay()];
        let day2 = weekday[dx.getDay()];
        let day3 = weekday[dy.getDay()];
        let day4 = weekday[dz.getDay()];

        function modify(day, arr, icon, temp, desc, pop, humidity, speed) {
            document.querySelector(".Day").innerText = day;
            document.querySelector(".Date").innerText = `${arr[0]} ${arr[1]} ${arr[2]}`;    
            document.querySelector(".Card-1 .part2 img").src = "https://openweathermap.org/img/wn/" + icon + ".png";
            document.querySelector(".Temp").innerText = Math.round(Number(temp)) + "°C";
            document.querySelector(".Description").innerText = desc;    
            document.querySelector("table tr:nth-child(1) td:nth-child(2)").innerText = pop + " %";
            document.querySelector("table tr:nth-child(2) td:nth-child(2)").innerText = humidity + " %";
            document.querySelector("table tr:nth-child(3) td:nth-child(2)").innerText = speed + " km/h";
        }

        function CardBackground(main) {

            let style = document.querySelector('.Card-1').style;
            if (main == 'Rain') {
                style.setProperty('--background', "url('https://source.unsplash.com/1600x900/?Rain')");
              } else if (main == 'Clouds') {
                style.setProperty('--background', "url('https://source.unsplash.com/1600x900/?Clouds')");
              } else if (main == 'Clear') {
                style.setProperty('--background', "url('https://source.unsplash.com/1600x900/?Sun')");
              } else {
                style.setProperty('--background', "url('https://source.unsplash.com/1600x900/?" + main +"')");
            }            
        }

        switch(DayNumber) {
            case 1:
                modify(day1, arr1, icon1, temp1, description1, pop1, humidity1, speed1);
                CardBackground(main1);
                break;
            case 2:
                modify(day2, arr2, icon2, temp2, description2, pop2, humidity2, speed2);
                CardBackground(main2);
                break;
            case 3:
                modify(day3, arr3, icon3, temp3, description3, pop3, humidity3, speed3);
                CardBackground(main3);
                break;
            case 4:
                modify(day4, arr4, icon4, temp4, description4, pop4, humidity4, speed4);
                CardBackground(main4);
                break;

        }

        // modifications common to all 4 days
        document.querySelector(".City").innerText = cityname + ", " + country;
        document.querySelector(".One img").src = "https://openweathermap.org/img/wn/" + icon1 + ".png";
        document.querySelector("#d1").innerText = day1.substr(0, 3);
        document.querySelector("#t1").innerText = Math.round(Number(temp1)) + "°C";

        document.querySelector(".Two img").src = "https://openweathermap.org/img/wn/" + icon2 + ".png";
        document.querySelector("#d2").innerText = day2.substr(0, 3);
        document.querySelector("#t2").innerText = Math.round(Number(temp2)) + "°C";

        document.querySelector(".Three img").src = "https://openweathermap.org/img/wn/" + icon3 + ".png";
        document.querySelector("#d3").innerText = day3.substr(0, 3);
        document.querySelector("#t3").innerText = Math.round(Number(temp3)) + "°C";

        document.querySelector(".Four img").src = "https://openweathermap.org/img/wn/" + icon4 + ".png";
        document.querySelector("#d4").innerText = day4.substr(0, 3);
        document.querySelector("#t4").innerText = Math.round(Number(temp4)) + "°C";

        document.querySelector(".Card").classList.remove("Loading");
        document.body.style.backgroundImage = "url('https://source.unsplash.com/1600x900/?" + cityname +"')"
    },

    search: function() {
        this.fetchWeather(document.querySelector(".Searchbar").value);
    },

};

document.querySelector(".Search button").addEventListener("click", function() { weather.search(); });
document.querySelector(".Searchbar").addEventListener("keyup", function(event) {
    if (event.key == "Enter") {
        weather.search();
    }
});

document.querySelector(".One").addEventListener("click", function() { weather.displayWeather(D , 1) });
document.querySelector(".Two").addEventListener("click", function() { weather.displayWeather(D , 2) });
document.querySelector(".Three").addEventListener("click", function() { weather.displayWeather(D , 3) });
document.querySelector(".Four").addEventListener("click", function() { weather.displayWeather(D , 4) });

weather.fetchWeather("Lagos");
