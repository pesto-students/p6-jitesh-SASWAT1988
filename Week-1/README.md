WEEK1-HTML:Assignment<br/>
**Exercise 1.1**<br/>
Question.When a user enters an URL in the browser, how does the browser fetch the desiredresult ?<br/>
Answer: 
    The browser is a software used to access the infomation like Picture, Audio, Video & Files available on the World Wide Web/ any WebServer.
It also could be defined as a client program used to request the webserver information demanded by the user. Most common webbrowsers are Microsoft EDGE,Chrome,Safari.

**High Level Components of a browser**
  Brower has the mainly the following 7 components
   1.**User Interface**
          The user interface is the first page that you see when you open the web browser. 
      This page has the address bar, forward/ backward button, menu, bookmarking option, and a few more options.
   2.**Browser Engine**
          The browser engine acts as an interface between the rendering engine and the UI of the browser. 
      Based on the input, it manipulates the rendering engine to provide output.
   3.**Rendering engine**
          The rendering engine is responsible for producing requested content to the browser and displaying it on the screen. 
      It parses the HTML documents and then converts them to readable form. All the browsers we know have their own rendering engines.
   4.**Networking**
        The network layer is responsible for security and communication on the internet. 
      It is also used for HTTP requests and to cache the documents retrieved in order to reduce network traffic.
   5.**UI Backend**
        It is for drawing basic boxes and windows/ widgets. 
      This is for a generic interface and independent of any specific platform. Behind all this, it uses an Operating system for UI methods.
   6.**JavaScript Interpreter**
        As we all know the JavaScript is responsible for all the websites/ webpages. 
      All these pages are written in JavaScript language. 
      Therefore this interpreter translates these pages and these are sent to the rendering engine to display the final results.
   7.**Data persistence**
        Data persistence or storage is for saving the data locally, like cookies. 
      The browsers support storage mechanisms like IndexedDB, WebSQL, File System, etc. to store databases locally on your computer. 
      This way user data is handled like cache, bookmarks, cookies, etc.
      
  ![image](https://user-images.githubusercontent.com/36676059/193511903-99488dcf-c1f5-4f63-8f12-aa46adf4ede3.png)

   When the user directly clicks on a link, writes a web address in the browser's address bar or submits a form the content is fetched and displyed on the browser.
   This oversimplified process is broadly classified into 4 Major Steps.
   
   **Navigation**
     - Navigation is the first step in loading a web page. It refers to the process that happens when the user is requesting a web page by directly clicking a link,
     writing a web address in brower's address bar or submits a form.
     - DNS Lookup is step of finding where the assets for that page are located (HTML, CSS, Javascript and other kind of files). 
     If we navigate to https://example.com, the HTML page is located on the server with IP address of 93.184.216.34 (for users, websites are domain names but for computers they are IP adresses). 
     If we've never visited this site before, a Domain Name System (DNS) lookup must happen.
     DNS servers are computer servers that contain a database of public IP addresses and their associated hostnames.
     So when we request a DNS lookup, what we actually do is interogate one of these servers and ask to find out which IP address coresponds to the https://example.com name. 
     If a corresponding IP is found, it is returned. If something happens and the lookup is not successful, we'll see some kind of error message in the browser.
     - TCP Handshake is process of estblishing a two way connection with the webserver using the IP Address received from the DNS Server.
     This is done through 3-way Handshake process SYNC, SYNC-ACK & ACK.
     - TLS Negotiation is s step of exstablishing a secure connection between browser and webserver by determining the Ciphers to be used to encrypt the communication. 
     
  **Data Fetching**
      - After establishing a secure connection with server, browser shall send an initial HTTP GET Request using HTTP Protocol.
      - Once the server receives the request, it will process it and reply with an HTTP response. 
      Attached to the body of the response we can find all relevant headers and the contents of the HTML document we requested.
      
  **Parsing**
      - Once the browser receives a response containing HTML Files, the browser's Browser Engine starts Parsing of the data whcih means analyzing and converting the program into an internal 
      format that a runtime environment can run. 
      - HTML Parsing involves two steps 
                 a. Tokenization - Its a process of lexical analysis and conversion of input into tokens(basic components of source code)  
                 b. DOM Tree Construction - Its a process of creating DOM (Tree Like Structure) based on the previoulsy created parsed tokens
     
     - CSS Parsing is a process of parse the CSS file and Build CSS Object Model(CSSOM) and involves two steps
                 a. Tokenization - The CSS Parser takes the bytes and conevts to characters following by tokens & nodes
                 b. CSS Tree Construction - The Nodes are added to the CSS Object Model using a selector matching.
       Pre-loader is parser that scans the HTML File while the main parser is processing the HTML & CSS. It looks for the resources like stylesheets,images,scripts 
       and downloads them.
       - JAVASCRIPT Execution So, after we get the Javascript file from the server, the code is interpreted, compiled, parsed and executed. 
       The computer can't understand Javascript code, only the browser can. 
       A javascript engine (ECMAScript engine) is a piece of software that executes (runs) Javascript code in the browser.
       The JS code needs to be translated into something the computer can work with and this is the job of the Javascript browser engine.
       When the JS Code is read,its converted to a data structure called Abstract Syntax Tree(AST)
   
   **Rendering**
      - The trees built in the parsing phase (DOM, CSSOM) are combined into something called the render tree. 
      This is used to compute the layout of all visible elements that will be painted to the screen in the end.This step is known as Rendering.
      
      - For each visible node that's found in the DOM, the coresponding rules will be found in the CSSOM and they will be applied.
      To do this, every visible node in the DOM is traversed excluding non-visible nodes and nodes made hidden in CSS.The render tree is the outcome of the same 
      process with all visible nodes along with content & styles.
      - Layout/Reflow Stage is a stage where the calculation of the position of the nodes in the viewport of the device is done.Root of the render tree is traversed node by node.
      
      - Painting(Rasterization) Stage is a stage where the browser converts each calculated box from Layout phase to actual pixels on the screen.
      - Layering and Composition is a technique to separate parts of a page into layers, painting them separately and composite as a page in a separate thread called the compositor thread. 
      When sections of the document are drawn in different layers, overlapping each other, compositing is necessary to ensure they are drawn to the screen in the right order and the content is rendered correctly.
      
      
      
       
    


     
    
    
