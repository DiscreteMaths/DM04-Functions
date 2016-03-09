Python for Finance
===============================

###What is Python?
Python is an **interpreted**, **object-oriented**, high-level programming language with dynamic semantics. its high-level built in data structures, combined with dynamic typing and dynamic binding, make it very attractive for Rapid Application Development, as well as for use as a scripting or glue language to connect existing components together.
Python's simple, easy to learn syntax emphasizes **readability** and therefore reduces the **cost** of program maintenance.
Python supports modules and packages, which encourages program modularity and code reuse.
The Python interpreter and the extensive standard library are available in source or binary form without charge for all major platforms, and can be freely distributed.
Often, programmers fall in love with Python because of the increased productivity it provides. 
Since there is no compilation step, the edit-test-debug cycle is incredibly fast. Debugging Python programs is easy: a bug or bad input will never cause a segmentation fault. 
Instead, when the interpreter discovers an error, it raises an exception
When the program doesn't catch the exception, the interpreter prints a stack trace.
A source level debugger allows inspection of local and global variables, evaluation of arbitrary expressions, setting breakpoints, stepping through the code a line at a time, and so on.
The debugger is written in Python itself, testifying to Python's introspective power.
On the other hand, often the quickest way to debug a program is to add a few print statements to the source: the fast edit-test-debug cycle makes this simple approach very effective.
This pretty well describes why Python has evolved into one of the major programming languages as of today. 
Nowadays, Python is used by the beginner programmer as well as by the highly skilled expert developer, at schools, in universities, at web companies, in large corporations and financial institutions, as well as in any scientific field.
Among others, Python is characterized by the following features:

1. ___``Open source``___: Python and the majority of supporting libraries and tools available are open source and generally come with quite flexible and open licenses.
2. ___``Interpreted``___: The reference CPython implementation is an interpreter of the language that translates Python code at runtime to executable byte code.
3. ___``Multiparadigm``___: Python supports different programming and implementation paradigms, such as object orientation and imperative, functional, or procedural programming.
4. ___``Multipurpose``___: Python can be used for rapid, interactive code development as well as for building large applications; it can be used for low-level systems operations as well as for high-level analytics tasks.
5. ___``Cross-platform``___: Python is available for the most important operating systems, such as Windows, Linux, and Mac OS; it is used to build desktop as well as web applications; it can be used on the largest clusters and most powerful servers as well as on such small devices as the Raspberry Pi.
6. ___``Dynamically typed``___: Types in Python are in general inferred during runtime and not statically declared as in most compiled languages.
7. ___``Indentation aware``___: In contrast to the majority of other programming languages, Python uses indentation for marking code blocks instead of parentheses, brackets, or semicolons.
8. ___``Garbage collecting``___: Python has automated garbage collection, avoiding the need for the programmer to manage memory.

####Brief History of Python
Although Python might still have the appeal of something new to some people, it has been around for quite a long time.
In fact, development efforts began in the 1980s by Guido van Rossum from the Netherlands.
He is still active in Python development and has been awarded the title of Benevolent Dictator for Life by the Python community
The following can be considered milestones in the development of Python:

1. Python 0.9.0 released in **1991** (first release)

2. Python 1.0 released in **1994**
 
3. Python 2.0 released in **2000**

4. Python 2.6 released in **2008**

5. Python 2.7 released in **2010**

6. Python 3.0 released in **2008**

7. Python 3.3 released in **2010**

8. Python 3.4 released in **2014**

It is remarkable, and sometimes confusing to Python newcomers, that there are two major versions available, still being developed and, more importantly, in parallel use since 2008.
As of this writing, this will keep on for quite a while since neither is there 100% code compatibility between the versions, nor are all popular libraries available for Python 3.x.
The majority of code available and in production is still Python 2.6/2.7, and this book is based on the 2.7.x version, although the majority of code examples should work with versions 3.x as well.

####Technology in Finance
[alt text](http://www.bing.com/images/search?q=Python+for+finance&view=detailv2&&id=78A9736C8F3D1003BA8DF311CCC60D767FC556D6&selectedIndex=21&ccid=95hu%2bbi3&simid=608049292789875178&thid=OIP.Mf7986ef9b8b738a5639ba2c9262492dao0&ajaxhist=0 "Logo Title Text 1")

In a sense, technology per se is nothing special to financial institutions (as compared, for instance, to industrial companies) or to the finance function (as compared to other corporate functions, like logistics).
However, in recent years, spurred by innovation and also regulation, banks and other financial institutions like hedge funds have evolved more and more into technology companies instead of being just financial intermediaries.
Technology has become a major asset for almost any financial institution around the globe, having the potential to lead to competitive advantages as well as disadvantages.
Some background information can shed light on the reasons for this development.

#####Technology Spending
Banks and financial institutions together form the industry that spends the most on technology on an annual basis. 
The following statement therefore shows not only that technology is important for the financial industry, but that the financial industry is also really important to the technology sector:

 *Banks will spend 4.2% more on technology in 2014 than they did in 2013, according to IDC analysts. Overall IT spend in financial services globally will exceed $430 billion in 2014 and surpass $500 billion by 2020*, the analysts say.
 
Large, multinational banks today generally employ thousands of developers that maintain existing systems and build new ones.
Large investment banks with heavy technological requirements show technology budgets often of several billion USD per year.

#####Technology as Enabler
The technological development has also contributed to innovations and efficiency improvements in the financial sector:

  *Technological innovations have contributed significantly to greater efficiency in the derivatives market. Through innovations in trading technology, trades at Eurex are today executed much faster than ten years ago despite the strong increase in trading volume and the number of quotes … These strong improvements have only been possible due to the constant, high IT investments by derivatives exchanges and clearing houses.*
  
As a side effect of the increasing efficiency, competitive advantages must often be looked for in ever more complex products or transactions.
This in turn inherently increases risks and makes risk management as well as oversight and regulation more and more difficult.
The financial crisis of 2007 and 2008 tells the story of potential dangers resulting from such developments.
In a similar vein, “algorithms and computers gone wild” also represent a potential risk to the financial markets; this materialized dramatically in the so-called flash crash of May 2010, where automated selling led to large intraday drops in certain stocks and stock indices.

[I'm an inline-style link](https://www.safaribooksonline.com/library/view/python-for-finance/9781491945360/ch01.html)
# Some Random Code Here
</code></pre>
- item 1 ``(([mean, stdev] = stats(vals)
 % #codegen
 % calculates a statistical mean and a standard
 % deviation for the values in vals.
 len = length (vals); mean = avg(vals, len);
 stdev = sqrt (sum ((vals-avg(vals, len)).^2))/len);
 coder/extrinstic ('plot');
 plot (vals, '-+'))``

- item 2 ``(function area = traparea(a,b,h)
	%  traparea(a,b,h)   Computes the area of a trapezoid given
	%                    the dimensions a, b and h, where a and b
	%                    are the lengths of the parallel sides and
	%                    h is the distance between these sides
	
	%  Compute the area, but suppress printing of the result
	area = 0.5*(a+b)*h;)``
- item 3 - fizzbuzztest. ``({ 	public static void main(String[] args){		
		for(int i = 1; i <= 100; i++){
			String test = "";
			test += (i % 3) == 0 ? "fizz" : "";
			test += (i % 5) == 0 ? "buzz" : "";
			System.out.println(!test.isEmpty() ? test : i);
		}
	}

} )``

1. This is in*italics*
2. This is in **bold**
3. This is in both ***bold and ialics***




