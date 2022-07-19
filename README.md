# B38tamil-d3
JSON

For the given JSON itterate overall for loops(for,for in)
`````````````````````````````````````````````````````````

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();

request.onload=function(){
    
    var result=JSON.parse(request.response);
    
   for(var i=0;i<result.length;i++)
   {
    console.log(result[i].name)
   }

   for(var key in result)
   {
    
    console.log(key,result[key].name);
   }


}

my own resume in json formet
````````````````````````````
const sowres={
    name:"sowmiya",
    CAREEROBJECTIVE:"Seeking a challenging and responsible position at entry level to enhance my skills and knowledge",
    QUALIFICATION:"  M.Sc/ Information Technology",
    WebDevelopment:"  HTML and CSS",
    OperatingSystem: " indows 98/ XP/ 7Linux",
    Technology:"  OOPS concepts and Software Engineering",
    TECHNICALACHIEVEMENTS:" Completed project in java entitled “RISK FACTOR OF CANCER DIABETICS AND HEART DISEASE ON NAIVE BAYES ALGORITHM ON WEB BASED APPLICATION” using NAIVE BAYES ALGORITHM",
    TECHNICALACHIEVEMENTS1:"Published a research paper entitled RISK FACTOR OF CANCER DIABETICS AND HEART DISEASE ON NAIVE BAYES ALGORITHM ON WEB BASED APPLICATION in IJRP, Volume  4, Issue  1,  May  2018",
    CompletedInternship :"  JAVA at Dr.Agarwal’s Center For Translational Research.",
    Fathername:	"Shanmugavel",
    Dateofbirth:	"09.08.1995",
    Gender :	" Female",
    Age:23,
    Nationality:"Indian",
    Languagesknown:"tamil english",
    DECLARATION:"I hereby declare that the information furnished above is true to the best of my knowledge"
};
 
for(var key1 in sowres)
{
 
 console.log(key1,sowres[key1]);
}

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
Difference between WINDOW,DOCUMENT AND SCREEN
`````````````````````````````````````````

window is the execution context and global object for that context's JavaScript
document contains the DOM, initialized by parsing HTML
screen describes the physical display's full screen
The most basic relationship among the three is that each browser tab has its own window, and a window has window.document and window.screen properties. The browser tab's window is the global context, so document and screen refer to window.document and window.screen. More details about the three objects are below,

window
Each browser tab has its own top-level window object. Each <iframe> (and deprecated <frame>) element has its own window object too, nested within a parent window. Each of these windows gets its own separate global object. window.window always refers to window, but window.parent and window.top might refer to enclosing windows, giving access to other execution contexts. In addition to document and screen described below, window properties include

setTimeout() and setInterval() binding event handlers to a timer
location giving the current URL
history with methods back() and forward() giving the tab's mutable history
navigator describing the browser software
document
Each window object has a document object to be rendered. These objects get confused in part because HTML elements are added to the global object when assigned a unique id. E.g., in the HTML snippet

<body>
  <p id="holyCow"> This is the first paragraph.</p>
</body>
the paragraph element can be referenced by any of the following:

window.holyCow or window["holyCow"]
document.getElementById("holyCow")
document.querySelector("#holyCow")
document.body.firstChild
document.body.children[0]
screen
The window object also has a screen object with properties describing the physical display:

screen properties width and height are the full screen

screen properties availWidth and availHeight omit the toolbar

The portion of a screen displaying the rendered document is the viewport in JavaScript, which is potentially confusing because we call an application's portion of the screen a window when talking about interactions with the operating system. The getBoundingClientRect() method of any document element will return an object with top, left, bottom, and right properties describing the location of the element in the viewport
