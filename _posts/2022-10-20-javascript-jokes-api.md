---
keywords: fastai
description: Breaking down the rapidapi code
title: Javascript Web Page using an API
badges: true
toc: true
categories: [jupyter]
nb_path: _notebooks/2022-10-20-javascript-jokes-api.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-20-javascript-jokes-api.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="o">&lt;</span><span class="err">!</span><span class="o">--</span> <span class="n">HTML</span> <span class="n">table</span> <span class="n">fragment</span> <span class="k">for</span> <span class="n">page</span> <span class="o">--&gt;</span>
<span class="o">&lt;</span><span class="n">table</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">thead</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">tr</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Time</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">All</span><span class="o">-</span><span class="n">time</span> <span class="n">Cases</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Recorded</span> <span class="n">Deaths</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Active</span> <span class="n">Cases</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">tr</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">thead</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">tbody</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">td</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;time&quot;</span><span class="o">&gt;&lt;/</span><span class="n">td</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">td</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;total_cases&quot;</span><span class="o">&gt;&lt;/</span><span class="n">td</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">td</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;total_deaths&quot;</span><span class="o">&gt;&lt;/</span><span class="n">td</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">td</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;active_cases&quot;</span><span class="o">&gt;&lt;/</span><span class="n">td</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">tbody</span><span class="o">&gt;</span>
  <span class="o">&lt;/</span><span class="n">table</span><span class="o">&gt;</span>
  
  <span class="o">&lt;</span><span class="n">table</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">thead</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">tr</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Country</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">All</span><span class="o">-</span><span class="n">time</span> <span class="n">Cases</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Recorded</span> <span class="n">Deaths</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="n">th</span><span class="o">&gt;</span><span class="n">Active</span> <span class="n">Cases</span><span class="o">&lt;/</span><span class="n">th</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">tr</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">thead</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">tbody</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;result&quot;</span><span class="o">&gt;</span>
      <span class="o">&lt;</span><span class="err">!</span><span class="o">--</span> <span class="n">generated</span> <span class="n">rows</span> <span class="o">--&gt;</span>
    <span class="o">&lt;/</span><span class="n">tbody</span><span class="o">&gt;</span>
  <span class="o">&lt;/</span><span class="n">table</span><span class="o">&gt;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Constant variables are declared here with keyword const</p>
<p>Key things to know:</p>
<ul>
<li>The document object "result" represents table body in the HTML above.</li>
<li>If you want to access any element in an HTML page in JavaScript, you always start by accessing the document object.  In this case, we are accessing "result" and defining a "resultContainer"</li>
<li>In the code, in following cells, document elements are created and organized for each Joke, each is added to the "resultContainer" as a row in the table body</li>
<li>Accessing the api is done using the variables url and options, this is setup to fetch the Covid data from the backend</li>
</ul>

</div>
</div>
</div>
</div>
 
