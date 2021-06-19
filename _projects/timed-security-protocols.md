---
title: Verifying Timed Security Protocols

people:
  - prof-sunjun
  - alum-lili

active: false

layout: project
last-updated: 2021-05-24
---

<p>Nowadays, protocols often use time to provide better security. For instance, lifetime of critical credentials and latency of physical networks are often introduced as safety thresholds in system designs. However, using time correctly in protocol design is challenging, due to a lack of time related formal specification and verification techniques. Thus, we propose a comprehensive analysis framework to formally specify as well as automatically verify timed security protocols.</p>
<p>A parameterized method is introduced in our framework to handle flexible timing constants whose values cannot be decided in the protocol design stage. In this work, we first propose timed applied π-calculus as a formal specification language for timed protocols. It can express computation of continuous time as well as application of cryptographic functions. Then, we define its formal semantics based on timed logic rules, which facilitates efficient verification against various authentication and secrecy properties. Given a parameterized security protocol, the verification result either produces secure configuration methods of its parameters, or reports an attack that works for any parameter values.</p>
<p>The correctness of our verification algorithm has been formally proved. We evaluate our framework with multiple timed and untimed security protocols and successfully find a previously unknown timing attack in Kerberos V.</p>

<h3>Papers and Supplementary Material</h3>


<span class="pubtitle">
				<a href="https://doi.org/10.1109/TSE.2017.2712621">A Formal Specification and Verification Framework for Timed Security Protocols</a>.
			</span><br />
			<span class="authors">
				Li Li, Jun Sun, Yang Liu, Meng Sun, and Jin Song Dong.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">IEEE Trans. Software Eng. 44(8)</span>. <br />Tool and Models: <a href="http://lilissun.github.io/r/time_files/Darwin-x86_64-v0.1.5.zip" class="tool">Darwin-x86_64-v0.1.5.zip</a>
			<br />
			<span class="links">
</span>

<span class="pubtitle">
				<a href="https://doi.org/10.1007/978-3-319-48989-6_31">Automated Verification of Timed Security Protocols with Clock Drift</a>.
			</span><br />
			<span class="authors">
				Li Li, Jun Sun, and Jin Song Dong.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">FM 2016: Formal Methods - 21st International Symposium, Limassol, Cyprus, November 9-11, 2016, Proceedings</span>. <br />Tool and Models: <a href="http://lilissun.github.io/r/time_files/Darwin-x86_64-v0.1.4.zip" class="tool">Darwin-x86_64-v0.1.4.zip</a>
			<br />
			<span class="links">
</span>

<span class="pubtitle">
				<a href="https://doi.org/10.1007/978-3-319-19249-9_22">Verifying Parameterized Timed Security Protocols</a>.
			</span><br />
			<span class="authors">
				Li Li, Jun Sun, Yang Liu, and Jin Song Dong.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">FM 2015: Formal Methods - 20th International Symposium, Oslo, Norway, June 24-26, 2015, Proceedings</span>. <br />Tool and Models: <a href="http://lilissun.github.io/r/time_files/Darwin-x86_64-v0.0.9.zip" class="tool">Darwin-x86_64-v0.0.9.zip</a>
			<br />
			<span class="links">
</span>

<span class="pubtitle">
				<a href="https://doi.org/10.1007/978-3-319-11737-9_20">TAuth: Verifying Timed Security Protocols</a>.
			</span><br />
			<span class="authors">
				Li Li, Jun Sun, Yang Liu, and Jin Song Dong.
			</span><br />
			<span style="color:grey;"><span class="venuetype"></span><span class="venue">Formal Methods and Software Engineering - 16th International Conference on Formal Engineering Methods, ICFEM 2014, Luxembourg, Luxembourg, November 3-5, 2014. Proceedings</span>. <br />Tool and Models: <a href="http://lilissun.github.io/r/time_files/model.zip" class="tool">model.zip</a>; <a href="http://lilissun.github.io/r/time_files/Darwin-x86_64-v0.0.7.zip" class="tool">Darwin-x86_64-v0.0.7.zip</a>
			<br />
			<span class="links">
</span>
