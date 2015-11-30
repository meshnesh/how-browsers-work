the main functionality of a browser is present web resources. The location of the resource is specified by the user using the URI(uniform Resource Identifier)
common user interfaces elements in the browser are: address bar, back and forward buttons, bookmarking options, refresh and stop buttons, home button that takes one to the homepage
browsers main components are:
the user interface: includes the address bar, back/forward button, bookmarking menu
The browser engine: marshals actions between the UI and the rendering engine.
The rendering engine: is responsible for displaying requested content.
Networking: network calls such as HTTP requests
UI back-end: used for drawing basic widgets like combo boxes and windows. This back-end exposes a generic interface that is not platform specific. Underneath it uses OS interface methods.
JavaScript interpreter: used to parse and execute code.
Data storage: this is a persistence layer.

The main flow of the rendering engine
the engine will start getting the contents of the requested document from the networking layer. Its usually done in 8KB chunks.
The engine will start parsing the HTML document and covert elements to DOM(Document Object Model) nodes in a tree called “content tree”. Styling information together with visual instructions in the HTML will be used to create another tree “The render tree”.
The render tree contains rectangles with visual attributes like color and dimensions. The rectangles  are in the right order to be displayed on the screen.Once the tree is constructed, the render tree goes through a layout process, this entails giving each node the exact coordinates where it should appear on the screen.
Next is painting the render tree(the render tree is traversed and the renderer's "paint()method is called to display content on the screen) will be painted using the UI back-end layer.
For user experience, the rendering engine will try to display contents as soon as possible. It wont wait until all HTML is parsed before starting to build and lay out the render tree.

Parser-lexer combination
parsing can be separated into two processes: lexical analysis and syntax analysis
lexical analysis: is the process of breaking the input tokens(language vocabulary), the collection of valid building blocks.
Syntax analysis is the applying of the language syntax rules.
Parsers usually divide the work between two components: the lexer (tokenizer) that is responsible for breaking the input into valid tokens, and the parser that is responsible according to the language syntax rules.
