# Google Drive Direct Link Generator
Unlike Other Google Drive Direct Link Generators Where Limit Is 100 MB. This Generator Can Create Direct Link For Files Of Any Size 

This Program Is Coded In HTML & Javascript Only 

So If You Want You Can Open This Wile Without Hosting It On Any Server. That Means Completly Offline.

## Introduction

Hi my name is PixelPlayz

This is my first open source project as a developer.

## Change Logs
### v0.2.0

• Added Support For Files UP to 5 TB (Which As Of Now Is The Maximum Size For A Single File In Google Drive)

### v0.1.0

• Released

• Create Direct Link For Files UP to 100 MB (Files Above That Limit Will Not Be Scanned For Antivirus By Google.)



## Installation

Copy The Html/JavaScript Code From The [index.html](https://github.com/PixelPlayz1887/Google-Drive-Direct-Link-Generator/blob/main/index.html) or from below and paste inside your website folder as AnyName.html

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
          body{
              background-color: black;
              font-family: sans-serif;
          }
          input[type=text], select {
              width: 50%;
              padding: 12px 20px;
              margin: 8px 0;
              display: inline-block;
              border: 1px solid #A1A1A1;
              border-radius: 4px;
              box-sizing: border-box;
          }
          h1{
              color: white;
              font-family: sans-serif;
              font-size: 350%;
          }
          h3{
              color: white;
              font-family: sans-serif;
          }
          .button {
            background-color: #00CDFF;
            border: none;
            color: white;
            font-family: sans-serif;
            padding: 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            border-radius: 200px;
            cursor: pointer;
          }
          div.a{
              text-align: center;
            font-family: sans-serif;
              
          }
        </style>
    </head>
    <body>
        <div class="a">
             <h1>Google Drive Direct Link Generator</h1>
             <input type="text" id="glink" placeholder="https://drive.google.com/file/d/1BMNWqro86SogIOFaasA8Zk0J7c5u2jQJ/view?usp=sharing">
                 <br>
                 <br>
             <a onclick="myFunction()" class="button">Generate Direct Link</a>
             <h3 id="link"></h3>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <br>
             <h3>* This Is My First Project So Expect Some Bugs</h3>
             <h3>If You Want Source Code Of This Project It Will Be Available On My <a href="https://github.com/PixelPlayz1887/Google-Drive-Direct-Link-Generator">GitHub</a>.</h3>
        </div>
        <script>
            function myFunction(){
                var glink = document.getElementById("glink").value;
                var id = "https://drive.google.com/uc?id=";
                var id2 = "&confirm=t";
                var replaced = glink.replace("https://drive.google.com/file/d/", "");
                var replaced = replaced.replace("/view?usp=sharing", "");
                var link = id.concat(replaced);
                var link = link.concat(id2);
                var flag = "https://drive.google.com/uc?export=download&id=";
                var msg = "Please enter a valid Google Drive link!!!";
                if (link != flag){
                    document.getElementById("link").innerHTML = link;
                } else {
                    document.getElementById("link").innerHTML = msg;
                }
            }
        </script>
    </body>
</html>
```
    
## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.



## License

[MIT](https://choosealicense.com/licenses/mit/)
