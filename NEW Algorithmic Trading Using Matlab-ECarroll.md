Algorithmic Trading Using Matlab
=========================================

####Introduction

MATLAB is a high-performance language for technical computing. It integrates computation, visualization, and programming in an easy-to-use environment where problems and solutions are expressed in familiar mathematical notation. Matlab was originally written by Cleve Moler, chairman of the computer science department at the University of New Mexico in 1970’s, to provide easy access to matrix software developed by the LINPACK and EISPACK for his students. Recognizing its commercial potential Jack Little, an engineer from Stamford, joined Moler to develop the language and interface into what it is today.

The programming environment was first adopted by researchers and practitioners in control engineering, Little's specialty, but quickly spread to many other domains such as data analysis, problem solving, and for experimentation and algorithm development. It is now also heavily used in education, in particular the teaching of linear algebra, numerical analysis, and is popular amongst scientists involved in image processing. Its influence in education is confirmed by the fact that more than 1000 textbooks use MATLAB as a teaching vehicle.

Over the years discipline-specific software written in MATLAB which is organized into libraries of functions called **toolboxes**, are widely used as well, a particular advantage for algorithmic trading with MATLAB. These *toolboxes* are simply add-ons to the basic package subscription some example of which are *Statistics*, and *Optimization* and *Financial* toolboxes. The Financial toolbox in particular is of great use for developing algorithms and testing them in MATLAB. The toolbox provides functions such as sde(), ftsbound() and corrcoef() for mathematical modelling and statistical analysis of financial data. The toolbox has the following features:* Portfolio Optimization * Risk and Investment Analysis * Financial Time Series Analysis * Technical Indicators and Charts * Theoretical Simulation for Finance

These features can be used and adapted for developing trading algorithms in MATLAB.


####Algorithmic Trading









Algorithmic trading uses algorithms to drive trading decisions, usually in electronic financial markets. Applied in buy-side and sell-side institutions algorithmic trading forms the basis of high-frequency trading, FOREX trading, and associated risk and execution analytics.

Builders and users of algorithmic trading applications need to develop, backtest, and deploy mathematical models that detect and exploit market movements. An effective workflow involves:



Things to include:

<pre><code>
for i=1:Nrealiz
    x=zeros(N,1);
    t=zeros(N,1);
    x(1)=x0; % initial condition
    t(1)=0;
    r=randn(N,1);
    for n=1:(N-1)
        x(n+1)=x(n)+nudt+sigsdt*r(n);
        t(n+1)=t(n)+dt;
    end
    Sv=exp(x);
    plot(t,Sv,'k-');
end
</code></pre>



functionname(autocorr)

    -Getting data from the web (yahoo, google, CBOE etc)
    -Aligning and filtering datasets
    -Nearest-neighbor classification
    -Designing & backtesting strategies
    -Interfacing with Interactive Brokers
    -Keeping track of strategy performance


-numerated list
-image/logo
-bold

-italics/ both
-streamstats.jl >github
