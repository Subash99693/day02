# day02

write a blog on the difference between document and windows object


answer:

Well, the window is the first thing that gets loaded into the browser. This window object has the majority of the properties like length, innerWidth, innerHeight, name, if it has been closed, its parents, and more.

What about the document object then?

The document object is your html, aspx, php, or other document that will be loaded into the browser. The document actually gets loaded inside the window object and has properties available to it like title, URL, cookie, etc. What does this really mean? That means if you want to access a property for the window it is window.property, if it is document it is window.document.property which is also available in short as document.property.

That seems simple enough. But what happens once an IFRAME is introduced? Uh oh… frameage.

An iframe actually is considered as a new window with its own document loaded into it. Here is where it may seem a little odd, but does make sense if you think about it. The original, parent window, is responsible for other windows to be loaded, not the document.

The property to access a frame is window.frames[], which is an array of all the frames. If you only have one iframe you access it by using window.frames[0]. Since the iframe is also a window object, accessing window properties of that frame is done by using window.frames[0].mywindowproperty.
