---
title: ALearner

people:
  - prof-sunjun
  - postdoc-long
  - alum-lyly

active: false

layout: project
last-updated: 2021-06-19
---

ALearner is a tool that can learn likely assertions based on passed and failed test cases according to a set of initial assertions. ALearner can improve the learned assertions by using selective sampling to generate more test cases automatically based on current learned assertions.

## Key Publication

<span class="pubtitle">
				<a href="https://doi.org/10.1007/978-3-319-68690-5_11">Assertion Generation Through Active Learning</a>.
			</span><br />
			<span class="authors">
				Long H. Pham, Lyly Tran Thi, and Jun Sun.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Formal Methods and Software Engineering - 19th International Conference on Formal Engineering Methods, ICFEM 2017, Xi'an, China, November 13-17, 2017, Proceedings</span></span>.
			<br />
			<span class="links">
</span>

## More Information


<p>The source code of ALearner can be downloaded from <a href="https://github.com/sunjun-group/Ziyuan" target="_blank">Github</a>.</p>
<p><strong>Primitive Templates</strong><br />
The list of primitive templates includes:</p>
<p>&#8211; For boolean variables<br />
+ x = true<br />
+ x = false</p>
<p>&#8211; For int and long variables<br />
+ x + y is not overflow<br />
+ x &#8211; y is not overflow<br />
+ x * y is not overflow<br />
+ gcd(x,y) = z<br />
+ x mod y = z</p>
<p>&#8211; For byte, short, int, long, float, double variables<br />
+ x = a<br />
+ x != MIN<br />
+ x != a<br />
+ x >= 0<br />
+ x > 0<br />
+ x = abs(y)<br />
+ x = y ^ 2<br />
+ x = y ^ 3<br />
+ x = sqrt(y)<br />
+ x >= y<br />
+ x > y<br />
+ x = y<br />
+ ax + by = c<br />
+ x + y = z<br />
+ x &#8211; y = z<br />
+ x * y = z<br />
+ x / y = z<br />
+ x ^ y = z</p>
<p>We also use SVM to learn assertions in the form of ax >= b and ax + by >= c.</p>
<p><strong>Experiments</strong><br />
We experimented ALearner with and without selective sampling. The experimental subjects include projects <a href="https://github.com/pedrovgs/Algorithms">pedrovgs/Algorithms</a>, <a href="https://github.com/JodaOrg/joda-time">JodaOrg/joda-time</a>, and <a href="https://github.com/JodaOrg/joda-money">JodaOrg/joda-money</a> from GitHub, and 10 programs from <a href="https://github.com/sosy-lab/sv-benchmarks">SVComp</a> (each program in SVComp is analyzed 20 times with random test cases).</p>
<p>We categorized each of learned assertions into 4 categories:<br />
&#8211; <em>Necessary</em> if it is necessary condition to avoid failure.<br />
&#8211; <em>Sufficient</em> if it is sufficient condition to avoid failure.<br />
&#8211; <em>Correct</em> if it is both necessary and sufficient.<br />
&#8211; <em>Irrelevant</em> if it is not necessary nor sufficient.</p>
<p>For SVComp programs, we consider if the learned assertions are correct or useful (weaker than user-defined precondition but still strong enough to prove the postcondition).</p>
<p>The summary of results are as follow:<br />
&#8211; Project Algorithms:<br />
+ With selective sampling: 69 corr, 10 necc, 2 suff, 4 irre<br />
+ Without selective sampling: 64 corr, 15 necc, 3 suff, 6 irre</p>
<p>&#8211; Project joda-time:<br />
+ With selective sampling: 83 corr, 43 necc, 0 suff, 7 irre<br />
+ Without selective sampling: 25 corr, 31 necc, 37 suff, 60 irre</p>
<p>&#8211; Project joda-money:<br />
+ With selective sampling: 16 corr, 9 necc, 0 suff, 0 irre<br />
+ Without selective sampling: 16 corr, 9 necc, 0 suff, 5 irre</p>
<p>&#8211; SVComp programs:<br />
+ With selective sampling: 90% useful, 80% correct<br />
+ Without selective sampling: 20% useful, nearly 0% correct</p>
<p>We can see with more data from selective sampling, ALearner can filter out a lot of sufficient and irrelevant assertions. Especially, without selective sampling, we almost never learn any correct assertions for SVComp programs.</p>
<p>We also compare ALearner&#8217;s results with <a href="https://plse.cs.washington.edu/daikon/">Daikon</a>&#8216;s results in the same set of subjects. In general, Daikon infers less necessary and correct assertions, but more sufficient and irrelevant assertions than ALearner.</p>
<p>You can download the details of results and test cases used in experiments from <a href="/supplementary-material/alearner-results.zip">HERE</a>.</p>