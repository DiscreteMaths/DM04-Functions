Research some ideas by reading job advertisements related to Maths, Stats, Data Science or Finance
Why Python for finance? <https://www.safaribooksonline.com/library/view/python-for-finance/9781491945360/ch01.html>
Python for Finance
============================
###What is Python?
- Python is an interpreted, object-oriented, high-level programming language with dynamic semantics. its high-level built in data structures, combined with dynamic typing and dynamic binding, make it very attractive for Rapid Application Development, as well as for use as a scripting or glue language to connect existing components together.
- Python's simple, easy to learn syntax emphasizes readability and therefore reduces the cost of program maintenance.
- Python supports modules and packages, which encourages program modularity and code reuse.
- The Python interpreter and the extensive standard library are available in source or binary form without charge for all major platforms, and can be freely distributed.
- Often, programmers fall in love with Python because of the increased productivity it provides. 
- Since there is no compilation step, the edit-test-debug cycle is incredibly fast. Debugging Python programs is easy: a bug or bad input will never cause a segmentation fault. 
- Instead, when the interpreter discovers an error, it raises an exception
- When the program doesn't catch the exception, the interpreter prints a stack trace.
- A source level debugger allows inspection of local and global variables, evaluation of arbitrary expressions, setting breakpoints, stepping through the code a line at a time, and so on.
- The debugger is written in Python itself, testifying to Python's introspective power.
- On the other hand, often the quickest way to debug a program is to add a few print statements to the source: the fast edit-test-debug cycle makes this simple approach very effective.
- This pretty well describes why Python has evolved into one of the major programming languages as of today. 
- Nowadays, Python is used by the beginner programmer as well as by the highly skilled expert developer, at schools, in universities, at web companies, in large corporations and financial institutions, as well as in any scientific field.
- Among others, Python is characterized by the following features:
1) Open source: Python and the majority of supporting libraries and tools available are open source and generally come with quite flexible and open licenses.
2) Interpreted: The reference CPython implementation is an interpreter of the language that translates Python code at runtime to executable byte code.
3) Multiparadigm: Python supports different programming and implementation paradigms, such as object orientation and imperative, functional, or procedural programming.
4) Multipurpose: Python can be used for rapid, interactive code development as well as for building large applications; it can be used for low-level systems operations as well as for high-level analytics tasks.
5) Cross-platform: Python is available for the most important operating systems, such as Windows, Linux, and Mac OS; it is used to build desktop as well as web applications; it can be used on the largest clusters and most powerful servers as well as on such small devices as the Raspberry Pi.
6) Dynamically typed: Types in Python are in general inferred during runtime and not statically declared as in most compiled languages.
7) Indentation aware: In contrast to the majority of other programming languages, Python uses indentation for marking code blocks instead of parentheses, brackets, or semicolons.
8) Garbage collecting: Python has automated garbage collection, avoiding the need for the programmer to manage memory.
###Brief History of Python
- Although Python might still have the appeal of something new to some people, it has been around for quite a long time.
- In fact, development efforts began in the 1980s by Guido van Rossum from the Netherlands.
- He is still active in Python development and has been awarded the title of Benevolent Dictator for Life by the Python community
- The following can be considered milestones in the development of Python:
  =>Python 0.9.0 released in 1991 (first release)
  =>Python 1.0 released in 1994
  =>Python 2.0 released in 2000
  =>Python 2.6 released in 2008
  =>Python 2.7 released in 2010
  =>Python 3.0 released in 2008
  =>Python 3.3 released in 2010
  =>Python 3.4 released in 2014
-It is remarkable, and sometimes confusing to Python newcomers, that there are two major versions available, still being developed and, more importantly, in parallel use since 2008.
-As of this writing, this will keep on for quite a while since neither is there 100% code compatibility between the versions, nor are all popular libraries available for Python 3.x.
-The majority of code available and in production is still Python 2.6/2.7, and this book is based on the 2.7.x version, although the majority of code examples should work with versions 3.x as well.
###The Python Ecosystem
- A major feature of Python as an ecosystem, compared to just being a programming language, is the availability of a large number of libraries and tools.
- hese libraries and tools generally have to be imported when needed (e.g., a plotting library) or have to be started as a separate system process (e.g., a Python development environment). 
- Importing means making a library available to the current namespace and the current Python interpreter process.
- Python itself already comes with a large set of libraries that enhance the basic interpreter in different directions.
- IPython is also sometimes called the killer application of the Python ecosystem. 
- It enhances the standard interactive shell in many ways.
- For example, it provides improved command-line history functions and allows for easy object inspection. 
- IPython comes in three different versions: a shell version, one based on a QT graphical user interface (the QT console), and a browser-based version (the Notebook).
###Python User Spectrum
- Python does not only appeal to professional software developers; it is also of use for the casual developer as well as for domain experts and scientific developers.
- Professional software developers find all that they need to efficiently build large applications.
- Almost all programming paradigms are supported; there are powerful development tools available; and any task can, in principle, be addressed with Python. 
- These types of users typically build their own frameworks and classes, also work on the fundamental Python and scientific stack, and strive to make the most of the ecosystem.
- Scientific developers or domain experts are generally heavy users of certain libraries and frameworks, have built their own applications that they enhance and optimize over time, and tailor the ecosystem to their specific needs.
- These groups of users also generally engage in longer interactive sessions, rapidly prototyping new code as well as exploring and visualizing their research and/or domain data sets.
- Casual programmers like to use Python generally for specific problems they know that Python has its strengths in. For example, visiting the gallery page of matplotlib, copying a certain piece of visualization code provided there, and adjusting the code to their specific needs might be a beneficial use case for members of this group.
- There is also another important group of Python users: beginner programmers, i.e., those that are just starting to program. Nowadays, Python has become a very popular language at universities, colleges, and even schools to introduce students to programming
- A major reason for this is that its basic syntax is easy to learn and easy to understand, even for the nondeveloper. In addition, it is helpful that Python supports almost all programming styles.
###Technology in Finance
- In a sense, technology per se is nothing special to financial institutions (as compared, for instance, to industrial companies) or to the finance function (as compared to other corporate functions, like logistics).
- However, in recent years, spurred by innovation and also regulation, banks and other financial institutions like hedge funds have evolved more and more into technology companies instead of being just financial intermediaries.
- Technology has become a major asset for almost any financial institution around the globe, having the potential to lead to competitive advantages as well as disadvantages.
- Some background information can shed light on the reasons for this development.
####Technology Spending
- Banks and financial institutions together form the industry that spends the most on technology on an annual basis. 
- The following statement therefore shows not only that technology is important for the financial industry, but that the financial industry is also really important to the technology sector:
  ==>Banks will spend 4.2% more on technology in 2014 than they did in 2013, according to IDC analysts. Overall IT spend in financial services globally will exceed $430 billion in 2014 and surpass $500 billion by 2020, the analysts say.
- Large, multinational banks today generally employ thousands of developers that maintain existing systems and build new ones.
- Large investment banks with heavy technological requirements show technology budgets often of several billion USD per year.
####Technology as Enabler
- The technological development has also contributed to innovations and efficiency improvements in the financial sector:
  ==>Technological innovations have contributed significantly to greater efficiency in the derivatives market. Through innovations in trading technology, trades at Eurex are today executed much faster than ten years ago despite the strong increase in trading volume and the number of quotes … These strong improvements have only been possible due to the constant, high IT investments by derivatives exchanges and clearing houses.
- As a side effect of the increasing efficiency, competitive advantages must often be looked for in ever more complex products or transactions.
- This in turn inherently increases risks and makes risk management as well as oversight and regulation more and more difficult.
- The financial crisis of 2007 and 2008 tells the story of potential dangers resulting from such developments.
- In a similar vein, “algorithms and computers gone wild” also represent a potential risk to the financial markets; this materialized dramatically in the so-called flash crash of May 2010, where automated selling led to large intraday drops in certain stocks and stock indices.
####Technology and Talent as Barriers to Entry
- On the one hand, technology advances reduce cost over time, ceteris paribus. 
- On the other hand, financial institutions continue to invest heavily in technology to both gain market share and defend their current positions. 
- To be active in certain areas in finance today often brings with it the need for large-scale investments in both technology and skilled staff.
- Not only is it costly and time-consuming to build a full-fledged derivatives analytics library, but you also need to have enough experts to do so. 
- And these experts have to have the right tools and technologies available to accomplish their tasks.
- Another quote about the early days of Long-Term Capital Management (LTCM), formerly one of the most respected quantitative hedge funds—which, however, went bust in the late 1990s—further supports this insight about technology and talent:
  ==> Meriwether spent $20 million on a state-of-the-art computer system and hired a crack team of financial engineers to run the show at LTCM, which set up shop in Greenwich, Connecticut. It was risk management on an industrial level.
- The same computing power that Meriwether had to buy for millions of dollars is today probably available for thousands. 
- On the other hand, trading, pricing, and risk management have become so complex for larger financial institutions that today they need to deploy IT infrastructures with tens of thousands of computing cores.



