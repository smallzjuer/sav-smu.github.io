---
title: Tzuyu

people:
  - prof-sunjun
  - alum-swl

active: false

layout: project
last-updated: 2021-06-19
---

Behavioral models are useful for various software engineering tasks. They are, however, often missing in practice. Thus, specification mining was proposed to tackle this problem. Existing work either focuses on learning simple behavioral models such as finite-state automata, or relies on techniques (e.g., symbolic execution) to infer finite-state machines equipped with data states, referred to as stateful typestates. The former is often inadequate as finite-state automata lack expressiveness in capturing behaviors of data-rich programs, whereas the latter is often not scalable. In this work, we propose a fully automated approach to learn stateful typestates by extending the classic active learning process to generate transition guards (i.e., propositions on data states). The proposed approach has been implemented in a tool called TzuYu and evaluated against a number of Java classes. The evaluation results show that TzuYu is capable of learning correct stateful typestates efficiently.

Details of this work can be found in the following publication.

## Key Publication

<span class="pubtitle">
				<a href="https://doi.org/10.1109/ASE.2013.6693101">TzuYu: Learning stateful typestates</a>.
			</span><br />
			<span class="authors">
				Hao Xiao, Jun Sun, Yang Liu, Shang-Wei Lin, and Chengnian Sun.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">2013 28th IEEE/ACM International Conference on Automated Software Engineering, ASE 2013, Silicon Valley, CA, USA, November 11-15, 2013</span></span>.
			<br />
			<span class="links">
</span>