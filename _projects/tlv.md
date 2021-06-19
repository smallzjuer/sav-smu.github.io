---
title: TLV

people:
  - prof-sunjun
  - alum-swl

active: false

layout: project
last-updated: 2021-06-19
---

A (Java) class provides a service to its clients (i.e., programs which use the class). The service must satisfy certain specifications. Different specifications might be expected at different levels of abstraction depending on the client’s objective. In order to effectively
contrast the class against its specifications, whether manually or automatically, one essential step is to automatically construct an abstraction of the given class at a proper level of abstraction. The abstraction should be correct (i.e., over-approximating) and accurate (i.e., with few spurious traces).

We present an automatic approach, which combines testing, learning, and validation, to constructing an abstraction. Our approach is designed such that a large part of the abstraction is generated based on testing and learning so as to minimize the use of
heavy-weight techniques like symbolic execution. The abstraction is generated through a process of abstraction/refinement, with no user input, and converges to a specific level of abstraction depending on the usage context. The generated abstraction is guaranteed to be correct and accurate. We have implemented the proposed approach in a toolkit named TLV and evaluated TLV with a number of benchmark programs as well as three real-world ones. The results show that TLV generates abstraction for program analysis and verification more efficiently.

## Key Publication

<span class="pubtitle">
				<a href="https://doi.org/10.1145/2786805.2786817">TLV: abstraction through testing, learning, and validation</a>.
			</span><br />
			<span class="authors">
				Jun Sun, Hao Xiao, Yang Liu, Shang-Wei Lin, and Shengchao Qin.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Proceedings of the 2015 10th Joint Meeting on Foundations of Software Engineering, ESEC/FSE 2015, Bergamo, Italy, August 30 - September 4, 2015</span></span>.
			<br />
			<span class="links">
</span>