---
title: Ziyuan

people:
  - prof-sunjun
  - alum-loc
  - postdoc-long
  - alum-lyly
  - alum-jingyi

active: false

layout: project
last-updated: 2021-06-19
---

## Introduction

<p>Debugging is difficult and time consuming, even with the help of automatic bug localization techniques. One of the reasons is that programmers have to understand the bug before fixing it and thus focusing on a few program statements marked buggy would not work. In this work, we investigate the problem of helping programmers to understand a bug (e.g., when the same failure manifests) and propose a method and tool which we call Ziyuan to automatically analyze the bug, based on active learning and test case generation. Given a program with an assertion and at least one test case failing the assertion, Ziyuan first generates random test cases, identifies potential bug locations through bug localization, and then generates test cases based on active learning techniques<br />
to identify a “simple” explanation for the cause of the bug. The explanation is in the form of a predicate which is a classifier for the passed test cases and failed test cases. Ziyuan is fully automatic, e.g., it uses an iterative classification and testing process to ensure that the classifier converges. We apply Ziyuan to real-world programs and conduct a user study to show its effectiveness.</p>
<p><em>As far as we know, there are no existing tools which do what Ziyuan does.</em> For instance, tools based on methods like symbolic execution would not work with the real-world bugs that we have dealt with (due to the limitation in encoding the programs and solving the constraint); tools based ideas like delta debugging etc. do not support generating of assertions; tools based on generating invariant based testing do not support the idea of selective sampling and thus are very constrained by the test cases. If you are aware of any tool that Ziyuan should be compared with, we will be really appreciated.</p>
<p>The source code of the project is <a href="https://github.com/sunjun-group/Ziyuan">HERE</a>.</p>

## Key Publications

<span class="pubtitle">
				<a href="https://doi.org/10.1007/978-3-030-34175-6_21">Compositional Verification of Heap-Manipulating Programs Through Property-Guided Learning</a>.
			</span><br />
			<span class="authors">
				Long H. Pham, Jun Sun, and Quang Loc Le.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Programming Languages and Systems - 17th Asian Symposium, APLAS 2019, Nusa Dua, Bali, Indonesia, December 1-4, 2019, Proceedings</span></span>.
			<br />
			<span class="links">
</span>

<span class="pubtitle">
				<a href="https://doi.org/10.1109/ICECCS.2017.12">Learning Likely Invariants to Explain Why a Program Fails</a>.
			</span><br />
			<span class="authors">
				Long H. Pham, Jun Sun, Lyly Tran Thi, Jingyi Wang, and Xin Peng.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">22nd International Conference on Engineering of Complex Computer Systems, ICECCS 2017, Fukuoka, Japan, November 5-8, 2017</span></span>.
			<br />
			<span class="links">
</span>

## Case Studies

<p>We have applied our implemented to a number of real-world bugs and the results can be found below.</p>
<p><a href="/supplementary-material/ziyuan/JavaParser%201.5-Issue46.html">JavaParser 1.5-Issue46</a><br />
<a href="/supplementary-material/ziyuan/JavaParser%201.5-Issue57.html">JavaParser 1.5-Issue57</a><br />
<a href="/supplementary-material/ziyuan/DiffUtils-issue10.html">DiffUtils-issue10</a><br />
<a href="/supplementary-material/ziyuan/Joda-time-Issue227.html">Joda-time-Issue227</a><br />
<a href="/supplementary-material/ziyuan/Joda-time-Issue21.html">Joda-time-Issue21</a><br />
<a href="/supplementary-material/ziyuan/Joda-time-Issue77.html">Joda-time-Issue77</a><br />
<a href="/supplementary-material/ziyuan/Apache%20Commons%20Math-Issue835.html">Apache Commons Math-Issue835</a><br />
<a href="/supplementary-material/ziyuan/Apache%20Commons%20Math-Issue1196.html">Apache Commons Math-Issue1196</a><br />
<a href="/supplementary-material/ziyuan/Apache%20Commons%20Math-Issue1005.html">Apache Commons Math-Issue1005</a><br />
<a href="/supplementary-material/ziyuan/D4J_Time8.html">Defects4j Time-Issue8</a></p>
<p>We also tried to explain two failed test cases created randomly by <a href="https://code.google.com/p/failuredoc/">FailureDoc</a>, which is a tool designed to explain why a test case fails by mutating the test case and generating an invariant using Daikon. Note that The results are below.</p>
<p><a href="/supplementary-material/ziyuan/FailureDoc-Commons%20Math.html">FailureDoc-Apache Commons Math</a><br />
<a href="/supplementary-material/ziyuan/FailureDoc-Commons%20Primitives.html">FailureDoc-Apache Commons Primitives</a></p>
<p>We remark that Ziyuan cannot be applied to other bugs analyzed by FailureDoc due to implementation issues, e.g., some bugs depend on an older version of Java (since that work was done quite some time ago) which is not supported by Ziyuan; for some bugs, there are no pass test cases; some bugs caused extremely large log files generated by javaslicer, etc.</p>
<p>We also get some more results from project Math in Defects4j (issue 1, 4, 38, 40, 58, 61, 70, 79, 84). However, because we are not programmers of the project, we do not understand it well enough to evaluate the usefulness of the learned predicates. Details can be found <a href="/supplementary-material/ziyuan/Inconclusive.html">here</a>.</p>

## User Study
<p>In addition, we have conducted a user study to investigate how real programmers view the usefulness of findings from Ziyuan. Within the time limit, we managed to gather a total of 14 programmers and randomly divided them into two groups. They were divided into two groups randomly except that they are constrained to have similar average years of programming experience. Programmers in group 1 were instructed to fix issue 46 of JavaParser1.5 with Ziyuan’s help and then to fix the java-diff-utils issue 10 without Ziyuan&#8217;s help. Group 2 did the first issue without Ziyuan’s help and then the second issue with Ziyuan’s help. The details of the two issues can be found above. Thus the scenario is designed to see whether Ziyuan helps if a programmer is asked to fix a bug in a legacy code. These two bugs are chosen as they are representative. They are however by no means easy.</p>
<p>Each programmer was given at most 30 minutes to study the bug so as to explain precisely the reason of the bug, i.e., what is the local specification that is violated which causes the bug, and propose a possible fix. We then evaluate whether their explanation/proposal<br />
is correct. The results are as follows.</p>
<p>Subject 1: 7 years of programming experience, group 1, disqualified as she was interrupted during study.<br />
Subject 2: 8 years of programming experience, group 1, done bug 1 correctly in 10 minutes; no result on bug 2<br />
Subject 3: 2 years of programming experience, group 1, no result on both bugs<br />
Subject 4: 3 years of programming experience, group 1, done bug 1 correctly in 27 minutes; no result on bug 2;<br />
Subject 5: 8 years of programming experience, group 1, no result on both bugs<br />
Subject 6: 6 years of programming experience, group 1, no result on both bugs<br />
Subject 7: 4 years of programming experience, group 1, done bug 1 correctly in 30 minutes; no result on bug 2;<br />
Subject 8: 7 years of programming experience, group 2, no result on bug 1; done bug 2 correctly in 23 minutes;<br />
Subject 9: 8 years of programming experience, group 2, done both bugs correctly in 14 and 24 minutes respectively<br />
Subject 10: 7 years of programming experience, group 2,  done both bugs correctly in 30 minutes each<br />
Subject 11: 3 years of programming experience, group 2, no result on both bugs<br />
Subject 12: 4 years of programming experience, group 2, no result on both bugs<br />
Subject 13: 10 years of programming experience, group 2, disqualified as he didn&#8217;t follow the instruction<br />
Subject 14: 9 years of programming experience, group 2, no result on bug 1; done bug 2 correctly in 15 minutes</p>




			
			