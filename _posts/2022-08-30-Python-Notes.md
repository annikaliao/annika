---
keywords: fastai
description: What I have learned
title: Lists, Dictionaries, Iteration Notes
toc: true
categories: [jupyter, week2]
tags: [python]
nb_path: _notebooks/2022-08-30-Python-Notes.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-08-30-Python-Notes.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Lists-and-Dictionaries">Lists and Dictionaries<a class="anchor-link" href="#Lists-and-Dictionaries"> </a></h3><ul>
<li>Variables all have a type: String, Integer, Float, List and Dictionary are some key types</li>
<li>In Python, variables are given a type at assignment<ul>
<li>Types are important to understand and will impact operations, as we saw when we were required to user str() function in concatenation</li>
</ul>
</li>
<li>Developers often think of variables as primitives or collections</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># variable of type string</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">name</span> <span class="o">=</span> <span class="s2">&quot;John Doe&quot;</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;name&quot;</span><span class="p">,</span> <span class="n">name</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">name</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>


<span class="c1"># variable of type integer</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">age</span> <span class="o">=</span> <span class="mi">18</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;age&quot;</span><span class="p">,</span> <span class="n">age</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">age</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type float</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">score</span> <span class="o">=</span> <span class="mf">90.0</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;score&quot;</span><span class="p">,</span> <span class="n">score</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">score</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type list (many values in one variable)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection?&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is different about the list output?&quot;</span><span class="p">)</span>
<span class="n">langs</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;Python&quot;</span><span class="p">,</span> <span class="s2">&quot;JavaScript&quot;</span><span class="p">,</span> <span class="s2">&quot;Java&quot;</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;langs&quot;</span><span class="p">,</span> <span class="n">langs</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">langs</span><span class="p">),</span> <span class="s2">&quot;length&quot;</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">langs</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;- langs[0]&quot;</span><span class="p">,</span> <span class="n">langs</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="nb">type</span><span class="p">(</span><span class="n">langs</span><span class="p">[</span><span class="mi">0</span><span class="p">]))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type dictionary (a group of keys and values)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is different about the dictionary output?&quot;</span><span class="p">)</span>
<span class="n">person</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="n">name</span><span class="p">,</span>
    <span class="s2">&quot;age&quot;</span><span class="p">:</span> <span class="n">age</span><span class="p">,</span>
    <span class="s2">&quot;score&quot;</span><span class="p">:</span> <span class="n">score</span><span class="p">,</span>
    <span class="s2">&quot;langs&quot;</span><span class="p">:</span> <span class="n">langs</span>
<span class="p">}</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;person&quot;</span><span class="p">,</span> <span class="n">person</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">person</span><span class="p">),</span> <span class="s2">&quot;length&quot;</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">person</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;- person[&quot;name&quot;]&#39;</span><span class="p">,</span> <span class="n">person</span><span class="p">[</span><span class="s2">&quot;name&quot;</span><span class="p">],</span> <span class="nb">type</span><span class="p">(</span><span class="n">person</span><span class="p">[</span><span class="s2">&quot;name&quot;</span><span class="p">]))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>What is the variable name/key? value? type? primitive or collection, why?
name John Doe &lt;class &#39;str&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
age 18 &lt;class &#39;int&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
score 90.0 &lt;class &#39;float&#39;&gt;

What is variable name/key? value? type? primitive or collection?
What is different about the list output?
langs [&#39;Python&#39;, &#39;JavaScript&#39;, &#39;Java&#39;] &lt;class &#39;list&#39;&gt; length 3
- langs[0] Python &lt;class &#39;str&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
What is different about the dictionary output?
person {&#39;name&#39;: &#39;John Doe&#39;, &#39;age&#39;: 18, &#39;score&#39;: 90.0, &#39;langs&#39;: [&#39;Python&#39;, &#39;JavaScript&#39;, &#39;Java&#39;]} &lt;class &#39;dict&#39;&gt; length 4
- person[&#34;name&#34;] John Doe &lt;class &#39;str&#39;&gt;
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="List-and-Dictionary-purpose">List and Dictionary purpose<a class="anchor-link" href="#List-and-Dictionary-purpose"> </a></h3><ul>
<li>List and Dictionaries are used to collect information</li>
<li>When information is collected it is formed into patterns<ul>
<li>Pattern is established you will be able collect many instances of that pattern.</li>
</ul>
</li>
<li>List is used to collect many instances of a pattern</li>
<li>Dictionary is used to define data patterns</li>
<li>Iteration is often used to process through lists</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">InfoDb</span> <span class="o">=</span> <span class="p">[]</span>

<span class="c1"># InfoDB is a data structure with expected Keys and Values</span>

<span class="c1"># Append to List a Dictionary of key/values related to a person and cars</span>
<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;FirstName&quot;</span><span class="p">:</span> <span class="s2">&quot;Annika&quot;</span><span class="p">,</span>
    <span class="s2">&quot;LastName&quot;</span><span class="p">:</span> <span class="s2">&quot;Liao&quot;</span><span class="p">,</span>
    <span class="s2">&quot;DOB&quot;</span><span class="p">:</span> <span class="s2">&quot;April 26&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Residence&quot;</span><span class="p">:</span> <span class="s2">&quot;San Diego&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Email&quot;</span><span class="p">:</span> <span class="s2">&quot;liao.92127@gmail.com&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Owns_Cars&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;N/A&quot;</span><span class="p">]</span>
<span class="p">})</span>

<span class="c1"># Append to List a 2nd Dictionary of key/values</span>
<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;FirstName&quot;</span><span class="p">:</span> <span class="s2">&quot;Lyndsey&quot;</span><span class="p">,</span>
    <span class="s2">&quot;LastName&quot;</span><span class="p">:</span> <span class="s2">&quot;Couch&quot;</span><span class="p">,</span>
    <span class="s2">&quot;DOB&quot;</span><span class="p">:</span> <span class="s2">&quot;March 29&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Residence&quot;</span><span class="p">:</span> <span class="s2">&quot;Hyden&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Email&quot;</span><span class="p">:</span> <span class="s2">&quot;lyndsey@gmail.com&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Owns_Cars&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;Tractor&quot;</span><span class="p">]</span>
<span class="p">})</span>

<span class="c1"># Print the data structure</span>
<span class="nb">print</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[{&#39;FirstName&#39;: &#39;Annika&#39;, &#39;LastName&#39;: &#39;Liao&#39;, &#39;DOB&#39;: &#39;April 26&#39;, &#39;Residence&#39;: &#39;San Diego&#39;, &#39;Email&#39;: &#39;liao.92127@gmail.com&#39;, &#39;Owns_Cars&#39;: [&#39;N/A&#39;]}, {&#39;FirstName&#39;: &#39;Lyndsey&#39;, &#39;LastName&#39;: &#39;Couch&#39;, &#39;DOB&#39;: &#39;March 29&#39;, &#39;Residence&#39;: &#39;Hyden&#39;, &#39;Email&#39;: &#39;lyndsey@gmail.com&#39;, &#39;Owns_Cars&#39;: [&#39;Tractor&#39;]}]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Formatted-output-of-List/Dictionary---for-loop">Formatted output of List/Dictionary - for loop<a class="anchor-link" href="#Formatted-output-of-List/Dictionary---for-loop"> </a></h3><ul>
<li>Managing data in Lists and Dictionaries is for the convenience of passing the data across the internet, to applications, or preparing it to be stored into a database
  -Exchange of data between programs includes the data type the method/function and the format of the data type</li>
<li>Application Programming Interface (API): write functions, receive, and return data.  </li>
</ul>
<p>Next, we will take the stored data and output it within our notebook.  There are multiple steps to this process...</p>
<ul>
<li>Preparing a function to format the data, the print_data() function receives a parameter called "d_rec" short for dictionary record.  It then references different keys within [] square brackets.   </li>
<li>Preparing a function to iterate through the list, the for_loop() function uses an enhanced for loop that pull record by record out of InfoDb until the list is empty.  Each time through the loop it call print_data(record), which passes the dictionary record to that function.</li>
<li>Finally, you need to activate your function with the call to the defined function for_loop().  Functions are defined, not activated until they are called.  By placing for_loop() at the left margin the function is activated.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># print function: given a dictionary of InfoDb content</span>
<span class="k">def</span> <span class="nf">print_data</span><span class="p">(</span><span class="n">d_rec</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;FirstName&quot;</span><span class="p">],</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;LastName&quot;</span><span class="p">])</span>  <span class="c1"># using comma puts space between values</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Residence:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Residence&quot;</span><span class="p">])</span> <span class="c1"># \t is a tab indent</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Birth Day:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;DOB&quot;</span><span class="p">])</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Cars: &quot;</span><span class="p">,</span> <span class="n">end</span><span class="o">=</span><span class="s2">&quot;&quot;</span><span class="p">)</span>  <span class="c1"># end=&quot;&quot; make sure no return occurs</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Owns_Cars&quot;</span><span class="p">]))</span>  <span class="c1"># join allows printing a string list with separator</span>
    <span class="nb">print</span><span class="p">()</span>


<span class="c1"># for loop algorithm iterates on length of InfoDb</span>
<span class="k">def</span> <span class="nf">for_loop</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;For loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
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
<pre>For loop output

Annika Liao
	 Residence: San Diego
	 Birth Day: April 26
	 Cars: N/A

Lyndsey Couch
	 Residence: Hyden
	 Birth Day: March 29
	 Cars: Tractor

</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Alternate-methods-for-iteration---while-loop">Alternate methods for iteration - while loop<a class="anchor-link" href="#Alternate-methods-for-iteration---while-loop"> </a></h3><p>In coding, there are usually many ways to achieve the same result.  Defined are functions illustrating using index to reference records in a list, these methods are called a "while" loop and "recursion".</p>
<ul>
<li>The while_loop() function contains a while loop, "while i &lt; len(InfoDb):".  This counts through the elements in the list start at zero, and passes the record to print_data()</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># while loop algorithm contains an initial n and an index incrementing statement (n += 1)</span>
<span class="k">def</span> <span class="nf">while_loop</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;While loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="nb">len</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">):</span>
        <span class="n">record</span> <span class="o">=</span> <span class="n">InfoDb</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>
        <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>
    <span class="k">return</span>

<span class="n">while_loop</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>While loop output

Annika Liao
	 Residence: San Diego
	 Birth Day: April 26
	 Cars: N/A

Lyndsey Couch
	 Residence: Hyden
	 Birth Day: March 29
	 Cars: Tractor

</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Calling-a-function-repeatedly---recursion">Calling a function repeatedly - recursion<a class="anchor-link" href="#Calling-a-function-repeatedly---recursion"> </a></h3><p>This final technique achieves looping by calling itself repeatedly.</p>
<ul>
<li>recursive_loop(i) function is primed with the value 0 on its activation with "recursive_loop(0)"</li>
<li>the last statement indented inside the if statement "recursive_loop(i + 1)" activates another call to the recursive_loop(i) function, each time i is increasing</li>
<li>ultimately the "if i &lt; len(InfoDb):" will evaluate to false and the program ends</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># recursion algorithm loops incrementing on each call (n + 1) until exit condition is met</span>
<span class="k">def</span> <span class="nf">recursive_loop</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="nb">len</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">):</span>
        <span class="n">record</span> <span class="o">=</span> <span class="n">InfoDb</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>
        <span class="n">recursive_loop</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>
    <span class="k">return</span>
    
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Recursive loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
<span class="n">recursive_loop</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Recursive loop output

Annika Liao
	 Residence: San Diego
	 Birth Day: April 26
	 Cars: N/A

Lyndsey Couch
	 Residence: Hyden
	 Birth Day: March 29
	 Cars: Tractor

</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

