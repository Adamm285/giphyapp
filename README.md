# Giphy App

![Project Image](https://image-cdn.hypb.st/https%3A%2F%2Fhypebeast.com%2Fimage%2F2018%2F08%2Fgiphy-film-festival-announcement-00.jpg?q=90&w=1400&cbr=1&fit=max)

> Search for fun memes! Searching for a term makes a button once clicked memes appear. a few buttons are included for fun!.

---

### Table of Contents

- [Description](#description)
- [How To Use](#how-to-use)
- [References](#references)
- [License](#license)
- [Author Info](#author-info)

---

## Description

Built to make API calls to Giphy and return Gifs of your choosing!

#### Technologies

- APIS
- HTML
- BootStrap
- JavaScript

[Back To The Top](#read-me-template)

---

## How To Use

#### Installation

No need to install anything just click this link [here](https://adamm285.github.io/giphyapp/)

#### API Reference

```
    function topicInfo() {
    event.preventDefault();
    var q = $(this).attr("data-topic");
    var queryURL = "https://api.giphy.com/v1/gifs/search?&q=" +
        q + "&api_key=roxSMmfrpjx5oCeWIrawLb3xWGXfKDnN";
    $.ajax({
        url: queryURL,
        method: "GET"
    }).then(function (res) {
        console.log("---------------\nURL: " + queryURL 
        + "\n---------------");
        console.log(q);
        console.log(res.data);
        var results = res.data;
          for (var i = 0; i < 10; i++) {
            var animalDiv = $("<div>");
            var p = $("<p>").text("Rating: " 
            + results[i].rating);
            var animalImage = $("<img>");
            animalImage.attr("src", 
            results[i].images.fixed_height.url);
            animalDiv.append(p);
            animalDiv.append(animalImage);
            $("#giphy-section").prepend(animalDiv);
          }
    });
};
```

[Back To The Top](#read-me-template)

---

## References

Giphy API [here](https://developers.giphy.com/)


[Back To The Top](#read-me-template)

---

## License

MIT License

Copyright (c) [2020][Adam M Murphy]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[Back To The Top](#read-me-template)

---

## Author Info

- LinkedIn - [@AdamMurphy](https://Linkedin.com/in/Adam-Murphy-73690bbb/)
- Website - [Adam M Murphy](https://adamm285.github.io/AdamMurphy'sPortfolio/)
- Resume - [Adam Murphy Software Developer](https://docs.google.com/document/d/1GLxDLwlrQkmdugH2Xl9MsOv5Rz6rmzqqSrbzfTZ-R3E/edit?usp=sharing)

[Back To The Top](#read-me-template)
