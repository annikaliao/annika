---
keywords: fastai
description: Notes, coding, examples
title: Algorithm Teaching Prep
toc: true 
badges: true
comments: false
categories: [jupyter]
nb_path: _notebooks/2022-11-16-algorithms.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-11-16-algorithms.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Developing-Algorithms">Developing Algorithms<a class="anchor-link" href="#Developing-Algorithms"> </a></h2><ul>
<li>When creating an algorithm, its good to outline its process before coding<ul>
<li>This ensures that it is <strong>sequenced</strong> correctly </li>
</ul>
</li>
<li>You should represent the algorithm using a flowchart or natural language <ul>
<li>Visualization can help you better see the flow of the whole algorithm</li>
<li>This may allow for the coding process to be more efficient and effective</li>
</ul>
</li>
</ul>
<h2 id="Review-of-Selection-and-Iteration">Review of Selection and Iteration<a class="anchor-link" href="#Review-of-Selection-and-Iteration"> </a></h2><ul>
<li>Algorithms with iteration repeat a function until a goal is reached<ul>
<li>To more easily represent an algorithm without showing all the repeated steps, we can use iteration</li>
</ul>
</li>
<li>Algorithms with selection only go through certain functions if certain things are true or false</li>
</ul>
<h2 id="Example-1">Example 1<a class="anchor-link" href="#Example-1"> </a></h2><p><img src="https://mail.google.com/mail/u/0?ui=2&amp;ik=307c2bfad8&amp;attid=0.1&amp;permmsgid=msg-a:r-3887059261601548865&amp;th=184e4f4ea4a304ff&amp;view=att&amp;disp=safe&amp;realattid=f_lbbiony40" alt=""></p>
<ol>
<li>Start</li>
<li>The number of pretzels in the pack is 6</li>
<li>Eat one fruit snack, number of pretzels in pack goes down by 1</li>
<li>How many pretzels are left?</li>
<li>Repeat step 3 until number of pretzels is 0</li>
<li>Display that pack is empty</li>
<li>Finish</li>
</ol>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pretzel</span> <span class="o">=</span> <span class="mi">6</span>
<span class="k">while</span> <span class="p">(</span><span class="n">pretzel</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">):</span>
    <span class="n">pretzel</span> <span class="o">-=</span> <span class="mi">1</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">pretzel</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">pretzel</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;All done!&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>5
4
3
2
1
0
All done!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Example-2">Example 2<a class="anchor-link" href="#Example-2"> </a></h2><p>The parking rate for a garage is as follows: <br> 
Less than one hour: Free <br>
1-2 hours: $5 &lt;br&gt;
2-3 hours: $8 <br> 
3-4 hours: $10 &lt;br&gt; 
4+ hours: $12</p>
<p><img src="https://mail.google.com/mail/u/0?ui=2&amp;ik=307c2bfad8&amp;attid=0.1&amp;permmsgid=msg-a:r2030496128188097827&amp;th=184e52d1193a9407&amp;view=att&amp;disp=inline&amp;realattid=f_lbbkvkt70" alt=""></p>
<ol>
<li>Start</li>
<li>Input number of hours parked</li>
<li>If hours is less than 1, cost is free</li>
<li>If hours is between 1 and 2, cost is $5</li>
<li>If hours is between 2 and 3, cost is $8</li>
<li>If hours is between 3 and 4, cost is $10</li>
<li>If hours is more than 4, cost is $12</li>
<li>Display cost and goodbye</li>
<li>Finish</li>
</ol>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The parking rate is as follows: </span><span class="se">\n</span><span class="s2"> Less than one hour: Free </span><span class="se">\n</span><span class="s2"> 1-2 hours: $5 </span><span class="se">\n</span><span class="s2"> 2-3 hours: $8 </span><span class="se">\n</span><span class="s2"> 3-4 hours: $10 </span><span class="se">\n</span><span class="s2"> 4+ hours: $12&quot;</span><span class="p">)</span>

<span class="n">time</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s2">&quot;How many hours have you parked at this garage?&quot;</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;How many hours have you parked at this garage?&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">time</span><span class="p">,</span> <span class="s2">&quot;hours costs:&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">time</span> <span class="o">&lt;</span> <span class="mi">1</span> <span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Free&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">time</span> <span class="o">&gt;=</span> <span class="mi">1</span> <span class="ow">and</span> <span class="n">time</span> <span class="o">&lt;</span> <span class="mi">2</span> <span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;$5&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">time</span> <span class="o">&gt;=</span> <span class="mi">2</span> <span class="ow">and</span> <span class="n">time</span> <span class="o">&lt;</span> <span class="mi">3</span> <span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;$8&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">time</span> <span class="o">&gt;=</span> <span class="mi">3</span> <span class="ow">and</span> <span class="n">time</span> <span class="o">&lt;</span> <span class="mi">4</span> <span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;$10&quot;</span><span class="p">)</span>
<span class="k">else</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;$12&quot;</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Have a good day!&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Hacks">Hacks<a class="anchor-link" href="#Hacks"> </a></h2><p>Develop your own complex algorithm using a flowchart and natural language, then code it!</p>
<p>Requirements:</p>
<ul>
<li>Includes both a flowchart AND natural language</li>
<li>Working code of the same algorithm</li>
<li>Incorporates selection AND/OR iteration</li>
<li>Make it creative!</li>
</ul>
<p>Tips:</p>
<ul>
<li><a href="https://online.visual-paradigm.com/app/diagrams/#diagram:proj=0&amp;type=Flowchart&amp;width=11&amp;height=8.5&amp;unit=inch">This site</a> is good for making flowcharts!</li>
<li>Natural language should just be a list</li>
<li>Think about the whole process, not just the end result</li>
</ul>

</div>
</div>
</div>
</div>
 
