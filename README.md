Download Link: https://assignmentchef.com/product/solved-web_technology-lab-exercise-week-11
<br>
<strong>Initial Setup: </strong>Create​ a directory to store the code of this lab exercise. Follow the instructions below to start a web server at the newly created directory.

Running web server on <strong>Mac</strong>​ using command:​

python3 -m http.server [port-number] -d [web-directory]

For example, to run on port 50000 and directory /Users/jsmith/Desktop/myweb

python3 -m http.server 50000 -d “/Users/jsmith/Desktop/myweb”

The website will be at the address: http://localhost:50000/​

Running web server on <strong>Windows</strong>​ using command:​

python -m http.server [port-number] -d [web-directory]

For example, to run on port 8000 and directory “C:UsersjsmithDesktopmy web”




python -m http.server 8000 -d “C:UsersjsmithDesktopmy web”




<h1>The website will be at the address: http://localhost:8000/​</h1>

This is a sample code for making AJAX call to get JSON:




<table width="624">

 <tbody>

  <tr>

   <td width="624">// make ajax query function makeAjaxQuery(){// create an XMLHttpRequest   var xhttp = new XMLHttpRequest(); // create a handler for the readyState change   xhttp.onreadystatechange = function() {     readyStateChangeHandler(xhttp);}; // making query by async callvar queryUrl = “url-to-query-the-server”;   xhttp.open(“GET”, queryUrl, true);   xhttp.send();} // handler for the readyState change function readyStateChangeHandler(xhttp){if (xhttp.readyState == XMLHttpRequest.DONE){if(xhttp.status == 200){// status = 200 means OK       handleStatusSuccess(xhttp);}     else{// status is NOT OKhandleStatusFailure(xhttp);}}}        </td>

  </tr>

  <tr>

   <td width="624">// XMLHttpRequest failedfunction handleStatusFailure(xhttp){alert(“AJAX request fail”);   alert(“readyState = ” + xhttp.readyState);   alert(“status = ” + xhttp.status);}  // XMLHttpRequest successfunction handleStatusSuccess(xhttp){alert(“AJAX request success”); // get the response json   var jsonText = xhttp.responseText;   alert(jsonText); // parse the json into an object   var obj = JSON.parse(jsonText); // display the object on the page   display(obj);} // display the javascript object info on the webpage function display(obj){// TODO} </td>

  </tr>

 </tbody>

</table>







<strong>Question 1.</strong> Create a JSON document ​ faculty.json​ with the following content:​




{

“name”: “Faculty of Engineering and Information Sciences”,

“abbreviation”: “EIS”,

“email”: “<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="87e2eef4c7f2e8f0a9e2e3f2a9e6f2">[email protected]</a>”,

“web”: “www.uow.edu.au/engineering-information-sciences”

}




Create a web page Question1.html​ .​

On the web page, display a button “Get Faculty Details”.

When the user clicks this button, write an AJAX call to get the above JSON file, parse the JSON into a Javascript object, and then display the Javascript object on the webpage as follows:










<strong>             </strong>

<strong>Question 2.</strong> Create a JSON document ​ airport.json​ with the following content:​

{

“searchQuery”: “Australia”,

“searchResult”: [

{

“airportName”: “Sydney Airport”,

“ICAO”: “YSSY”,

“IATA”: “SYD”,

“city”: “Sydney”,

“country”: “Australia”

},

{

“airportName”: “Canberra Airport”,

“ICAO”: “YSCB”,

“IATA”: “CBR”,

“city”: “Canberra”,

“country”: “Australia”

},

{

“airportName”: “Brisbane Airport”,

“ICAO”: “YBBN”,

“IATA”: “BNE”,

“city”: “Brisbane”,

“country”: “Australia”

},

{

“airportName”: “Adelaide Airport”,

“ICAO”: “YPAD”,

“IATA”: “ADL”,

“city”: “Adelaide”,

“country”: “Australia”

},

{

“airportName”: “Hobart International Airport”,

“ICAO”: “YMHB”,

“IATA”: “HBA”,

“city”: “Hobart”,

“country”: “Australia”

},

{

“airportName”: “Melbourne Airport”,

“ICAO”: “YMML”,

“IATA”: “MEL”,

“city”: “Melbourne”,

“country”: “Australia”

},

{

“airportName”: “Perth Airport”,

“ICAO”: “YPPH”,

“IATA”: “PER”,

“city”: “Perth”,

“country”: “Australia”

},

{

“airportName”: “Darwin International Airport”,

“ICAO”: “YPDN”,

“IATA”: “DRW”,

“city”: “Darwin”,

“country”: “Australia”

}

]

}




Create a web page Question2.html​ .​

On the web page, display a button “Search Airport”.

When the user clicks this button, write an AJAX call to get the above JSON file, parse the JSON into a Javascript object, and then display the Javascript object on the webpage as follows:


