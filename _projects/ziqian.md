---
title: ZiQian

people:
  - prof-sunjun
  - alum-jingyi

active: false

layout: project
last-updated: 2021-06-19
---

<p><strong>Introduction:</strong></p>
<p>Model checking, unlike other model-based analysis and development methods, is perhaps not as popular as it ought to be due to the fact that a good model is required beforehand. In the setting of PMC, users are further required to provide a probabilistic model with accurate distributions, which is often challenging. In practice, system modeling is often done manually, which is both time-consuming and error-prone. Worse, it could be infeasible if the system is a black box or it is simply too complicated so that no accurate model exists.</p>
<p>One way to avoid manual modeling is statistical model checking (SMC), which samples the system executions and apply hypothesis testing for verification purpose. Another approach <strong>we are more interested in is to automatically learn probabilistic models from system executions.</strong></p>
<p>We investigate two categaries of learning algorithms: learn from multiple executions and learn from a single, long execution. The resulting models are both discrete-time Markov Chains (DTMCs). We propose a new learning framework based on evolution algorithms to provide better generalization from system executions compared to existing state-of-art algorithms, which orgnizes data as a tree and generalize a model based on it. We then conduct an empirical study on multiple case studies (see <a href="http://www.prismmodelchecker.org/benchmarks/models.php#dtmcs">here</a>) to compare the state-of-art learning algorithms, evolution-based algorithms and SMC in terms of effectiveness and efficiency. We also apply them on real-world complicated system (see <a href="http://itrust.sutd.edu.sg/research/">water treatment system</a>) where manual modeling is impossible.</p>
<p><strong>Implementation:</strong></p>
<p>The source code of the project is hosted in BitBucket. (Click <a href="https://github.com/wang-jingyi/Ziqian">here</a>)</p>
<p>You can follow the project guideline to try out the case studies or format your own system executions to Ziqian input to run the learning algorithms.</p>
<p>Do try it out!</p>

## Key Publications

<span class="pubtitle">
				<a href="https://doi.org/10.1109/TSE.2018.2886898">Automatically 'Verifying' Discrete-Time Complex Systems through Learning, Abstraction and Refinement</a>.
			</span><br />
			<span class="authors">
				Jingyi Wang, Jun Sun, Shengchao Qin, and Cyrille Jégourel.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">IEEE Trans. Software Eng. 47(1)</span></span>.
			<br />
			<span class="links">
</span>

<span class="pubtitle">
				<a href="https://doi.org/10.1007/s10009-018-0492-7">Learning probabilistic models for model checking: an evolutionary approach and an empirical study</a>.
			</span><br />
			<span class="authors">
				Jingyi Wang, Jun Sun, Qixia Yuan, and Jun Pang.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Int. J. Softw. Tools Technol. Transf. 20(6)</span></span>.
			<br />
			<span class="links">
</span>
