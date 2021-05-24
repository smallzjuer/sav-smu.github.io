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

TO APPEAR
