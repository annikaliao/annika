---
keywords: fastai
description: Exploring lists
title: Python List
toc: false
categories: [jupyter, week2] 
tags: [python]
nb_path: _notebooks/2022-09-01-python-list.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-01-python-list.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">InfoDb</span> <span class="o">=</span> <span class="p">[]</span>

<span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;Hello, you will be asked a few questions.</span><span class="se">\n</span><span class="s2">Are you ready?&quot;</span><span class="p">)</span>
<span class="n">rsp</span> <span class="o">=</span> <span class="nb">input</span> <span class="p">(</span><span class="s2">&quot;Are you ready?&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;yes&quot;</span><span class="p">:</span>
    <span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;Great!</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;no&quot;</span> <span class="p">:</span>
    <span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;That&#39;s too bad.</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>  

<span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;What is your name?&quot;</span><span class="p">)</span>
<span class="n">name</span> <span class="o">=</span> <span class="nb">input</span> <span class="p">(</span><span class="s1">&#39;What is your name?</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>

<span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;Hello &quot;</span> <span class="o">+</span> <span class="n">name</span> <span class="o">+</span> <span class="s2">&quot;! How old are you?&quot;</span><span class="p">)</span>
<span class="n">age</span> <span class="o">=</span> <span class="nb">input</span> <span class="p">(</span><span class="s1">&#39;How old are you?</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>

<span class="nb">print</span> <span class="p">(</span><span class="n">age</span> <span class="o">+</span> <span class="s2">&quot;! Alright, what&#39;s your favorite color?&quot;</span><span class="p">)</span>
<span class="n">color</span> <span class="o">=</span> <span class="nb">input</span> <span class="p">(</span><span class="s2">&quot;What&#39;s your favorite color?</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>

<span class="nb">print</span> <span class="p">(</span><span class="n">color</span> <span class="o">+</span><span class="s2">&quot;? I love that color too!&quot;</span><span class="p">)</span>

<span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">Thanks for doing my quiz! Here is your info:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>

<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;Name&quot;</span> <span class="p">:</span> <span class="n">name</span><span class="p">,</span>
    <span class="s2">&quot;Age&quot;</span> <span class="p">:</span> <span class="n">age</span><span class="p">,</span>
    <span class="s2">&quot;Favorite color&quot;</span> <span class="p">:</span> <span class="n">color</span>
<span class="p">})</span>

<span class="k">def</span> <span class="nf">print_data</span><span class="p">(</span><span class="n">d_rec</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Name:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Name&quot;</span><span class="p">])</span>  <span class="c1"># using comma puts space between values</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Age:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Age&quot;</span><span class="p">])</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Favorite Color:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Favorite color&quot;</span><span class="p">],</span> <span class="n">end</span><span class="o">=</span><span class="s2">&quot;&quot;</span><span class="p">)</span>  <span class="c1"># end=&quot;&quot; make sure no return occurs</span>
    <span class="nb">print</span><span class="p">()</span>

<span class="k">def</span> <span class="nf">for_loop</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">record</span> <span class="ow">in</span> <span class="n">InfoDb</span><span class="p">:</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>

<span class="n">for_loop</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Hello, you will be asked a few questions.
Are you ready?
What is your name?
Hello Haeryn! How old are you?
15! Alright, what&#39;s your favorite color?
Yellow? I love that color too!

Thanks for doing my quiz! Here is your info:

Name Haeryn
Age: 15
Favorite Color: Yellow
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

