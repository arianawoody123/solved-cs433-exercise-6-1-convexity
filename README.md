Download Link: https://assignmentchef.com/product/solved-cs433-exercise-6-1-convexity
<br>
Recall that we say that a function <em>f </em>is <em>convex </em>if the domain of <em>f </em>is a convex set and

<em>f</em>(<em>θ</em><em>x </em>+ (1 − <em>θ</em>)<em>y</em>) ≤ <em>θf</em>(<em>x</em>) + (1 − <em>θ</em>)<em>f</em>(<em>y</em>)<em>, </em>for all <em>x</em><em>,y </em>in the domain of <em>f, </em>0 ≤ <em>θ </em>≤ 1<em>.</em>

And <em>strictly convex </em>if

<em>f</em>(<em>θ</em><em>x </em>+ (1 − <em>θ</em>)<em>y</em>) <em>&lt; θf</em>(<em>x</em>) + (1 − <em>θ</em>)<em>f</em>(<em>y</em>)<em>, </em>for all <em>x </em>=6 <em>y </em>in the domain of <em>f, </em>0 <em>&lt; θ &lt; </em>1<em>.</em>

Prove the following assertions.

<ol>

 <li>The affine function <em>f</em>(<em>x</em>) = <em>ax </em>+ <em>b </em>is convex, where <em>a,b </em>and <em>x </em>are scalars.</li>

 <li>If multiple functions <em>f<sub>n</sub></em>(<em>x</em>) are convex over a fixed domain, then their sum <em>g</em>(<em>x</em>) = <sup>P</sup><em><sub>n </sub></em><em>f<sub>n</sub></em>(<em>x</em>) is convex over the same domain.</li>

 <li>Take <em>f,g </em>: R → R to be convex functions and <em>g </em>to be increasing. Then <em>g </em>◦ <em>f </em>is also convex.</li>

</ol>

Note: A function <em>g </em>is increasing if <em>a </em>≥ <em>b </em>⇔ <em>g</em>(<em>a</em>) ≥ <em>g</em>(<em>b</em>). An example of a convex and increasing function is exp(<em>x</em>)<em>,x </em>∈ R.

<ol start="4">

 <li>If <em>f </em>: R → R is convex, then <em>g </em>: R<em><sup>D </sup></em>→ R, where <em>g</em>(<em>x</em>) := <em>f</em>(<em>w</em><sup>&gt;</sup><em>x </em>+ <em>b</em>), is also convex. Here, <em>w </em>is a constant vector in R<em><sup>D</sup></em>, <em>b </em>is a constant in R and <em>x </em>∈ R<em><sup>D</sup></em>.</li>

 <li>Let <em>f </em>: R<em><sup>D </sup></em>→ R be strictly convex. Let <em>x</em><em><sup>? </sup></em>∈ R<em><sup>D </sup></em>be a global minimizer of <em>f</em>. Show that this global minimizer is unique. Hint: Do a proof by contradiction.</li>

</ol>

<h1>1           Extension of Logistic Regression to Multi-Class Classification</h1>

Suppose we have a classification dataset with <em>N </em>data example pairs {<em>x</em><em><sub>n</sub></em><em>,y<sub>n</sub></em>}, <em>n </em>∈ [1<em>,N</em>], and <em>y<sub>n </sub></em>is a categorical variable over <em>K </em>categories, <em>y<sub>n </sub></em>∈ {1<em>,</em>2<em>,…,K</em>}. We wish to fit a linear model in a similar spirit to logistic regression, and we will use the softmax function to link the linear inputs to the categorical output, instead of the logistic function.

We will have <em>K </em>sets of parameters <em>w</em><em><sub>k</sub></em>, and define  and compute the probability distribution of the output as follows,

<em>.</em>

Note that we indeed have a probability distribution, as. To make the model <em>identifiable</em>, we will fix <em>w</em><em><sub>K </sub></em>to <strong>0</strong>, which means we have <em>K</em>−1 sets of parameters to learn. As in logistic regression, we will assume that each <em>y<sub>n </sub></em>is i.i.d., i.e.,

<em>.</em>

<ol>

 <li>Derive the log-likelihood for this model.</li>

 <li>Derive the gradient with respect to each <em>w</em><em><sub>k</sub></em>.</li>

 <li>Show that the negative of the log-likelihood is convex with respect to <em>w</em><em><sub>k</sub></em>.</li>

</ol>

<h1>2           Mixture of Linear Regression</h1>

In Project-I, you worked on a regression dataset with two or more distinct clusters. For such datasets, a mixture of linear regression models is preferred over just one linear regression model.

Consider a regression dataset with <em>N </em>pairs {<em>y<sub>n</sub>,</em><em>x</em><em><sub>n</sub></em>}. Similar to Gaussian mixture model (GMM), let <em>r<sub>n </sub></em>∈ {1<em>,</em>2<em>,…,K</em>} index the mixture component. Distribution of the output <em>y<sub>n </sub></em>under the <em>k</em><sup>th </sup>linear model is defined as follows:

Here, <em>w</em><em><sub>k </sub></em>is the regression parameter vector for the <em>k</em><sup>th </sup>model with <em>w </em>being a vector containing all <em>w</em><em><sub>k</sub></em>. Also, <em>x</em>˜.

<ol>

 <li>Define <em>r</em><em><sub>n </sub></em>to be a binary vector of length <em>K </em>such that all the entries are 0 except a <em>k</em><sup>th </sup>entry, i.e., <em>r<sub>nk </sub></em>= 1, implying that <em>x</em><em><sub>n </sub></em>is assigned to the <em>k</em><sup>th </sup> Rewrite the likelihood <em>p</em>(<em>y<sub>n</sub></em>|<em>x</em><em><sub>n</sub></em><em>,w</em><em>,r</em><em><sub>n</sub></em>) in terms of <em>r<sub>nk</sub></em>.</li>

 <li>Write the expression for the joint distribution <em>p</em>(<em>y</em>|<em>X</em><em>,w</em><em>,r</em>) where <em>r </em>is the set of all <em>r</em><sub>1</sub><em>,r</em><sub>2</sub><em>,…,r</em><em><sub>N</sub></em>.</li>

 <li>Assume that <em>r<sub>n </sub></em>follows a multinomial distribution <em>p</em>(<em>r<sub>n </sub></em>= <em>k</em>|<em>π</em>) = <em>π<sub>k</sub></em>, with <em>π </em>= [<em>π</em><sub>1</sub><em>,π</em><sub>2</sub><em>,…,π<sub>K</sub></em>]. Derive the marginal distribution <em>p</em>(<em>y<sub>n</sub></em>|<em>x</em><em><sub>n</sub></em><em>,w</em><em>,π</em>) obtained after marginalizing <em>r<sub>n </sub></em></li>

 <li>Write the expression for the maximum likelihood estimator L(<em>w</em><em>,π</em>) := −log<em>p</em>(<em>y</em>|<em>X</em><em>,w</em><em>,π</em>) in terms of data <em>y </em>and <em>X</em>, and parameters <em>w </em>and <em>π</em>.</li>

 <li>Is L jointly-convex with respect to <em>w </em>and <em>π</em>? Is the model identifiable? Prove your answers.</li>

</ol>

2