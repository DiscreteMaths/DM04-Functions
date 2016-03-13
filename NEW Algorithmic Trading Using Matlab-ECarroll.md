Algorithmic Trading Using Matlab
=========================================
MATLAB is a high-performance language for technical computing. It integrates computation, visualization, and programming in an easy-to-use environment where problems and solutions are expressed in familiar mathematical notation. Matlab was originally written by Cleve Moler, chairman of the computer science department at the University of New Mexico in 1970’s, to provide easy access to matrix software developed by the LINPACK and EISPACK for his students. Recognizing its commercial potential Jack Little, an engineer from Stamford, joined Moler to develop the language and interface into what it is today.



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
