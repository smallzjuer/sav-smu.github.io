---
title: Smart Concolic Testing

people:
  - prof-sunjun
  - alum-jingyi

active: false

layout: project
last-updated: 2021-06-19
---

<p>Concolic testing integrates concrete execution (e.g., random testing) and symbolic execution for test case generation. It is shown to be more cost-effective than random testing or symbolic execution sometimes. A concolic testing strategy is a function which decides when to apply random testing or symbolic execution, and if it is the latter case, which program path to symbolically execute. Many heuristics-based strategies have been proposed. It is still an open problem what is the optimal concolic testing strategy.</p>
<p>In this work, we make two contributions towards solving this problem. First, we show the optimal strategy can be defined based on the probability of program paths and the cost of constraint solving. The problem of identifying the optimal strategy is then reduced to a model checking problem of Markov Decision Processes with Costs. Secondly, in view of the complexity in identifying the optimal strategy, we design a greedy algorithm for approximating the optimal strategy. We conduct two sets of experiments. One is based on randomly generated models and the other is based on a set of C programs. The results show that existing heuristics have much room to improve and our greedy algorithm often outperforms existing heuristics.</p>
<p>Our prototype implementation and experiment subjects can be found <a href="/supplementary-material/data126.zip">HERE</a>.</p>

## Key Publication

<span class="pubtitle">
				<a href="https://doi.org/10.1145/3180155.3180177">Towards optimal concolic testing</a>.
			</span><br />
			<span class="authors">
				Xinyu Wang, Jun Sun, Zhenbang Chen, Peixin Zhang, Jingyi Wang, and Yun Lin.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Proceedings of the 40th International Conference on Software Engineering, ICSE 2018, Gothenburg, Sweden, May 27 - June 03, 2018</span></span>.
			<br />
			<span class="links">
</span>