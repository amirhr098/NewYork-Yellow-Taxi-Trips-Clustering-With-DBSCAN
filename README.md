# NewYork-Yellow-Taxi-Trips-Clustering-With-DBSCAN

In this project I try to cluster the NY taxi data sets by SciKit Learn DBSCAN and finding the best value of 'eps' and 'min_samples' by Silhouette Score

Original Data: https://www.kaggle.com/c/nyc-taxi-trip-duration (Only used 'train.csv'.)

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="Best-Parameters"><strong>Best Parameters</strong><a class="anchor-link" href="#Best-Parameters"></a></h1>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dbscan</span> <span class="o">=</span> <span class="n">DBSCAN</span><span class="p">(</span><span class="n">eps</span><span class="o">=</span><span class="mf">1.95</span><span class="p">,</span> <span class="n">min_samples</span><span class="o">=</span><span class="mi">300</span><span class="p">)</span>
<span class="n">dbscan</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
</pre></div>


</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">



<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>DBSCAN(eps=1.95, min_samples=300)</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">calinski_harabasz_score</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">dbscan</span><span class="o">.</span><span class="n">labels_</span><span class="p">)</span>
</pre></div>


</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    





<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>2745.4420020496927</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">dbscan</span><span class="o">.</span><span class="n">labels_</span><span class="p">)</span>
</pre></div>


</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    



<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>array([-1,  0,  1,  2,  3,  4,  5])</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dbscan</span><span class="o">.</span><span class="n">get_params</span><span class="p">()</span>
</pre></div>


</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    





<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>{'algorithm': 'auto',
 'eps': 1.95,
 'leaf_size': 30,
 'metric': 'euclidean',
 'metric_params': None,
 'min_samples': 300,
 'n_jobs': None,
 'p': None}</pre>
</div>

</div>

</div>

</div>

</div>

# Help
  
Feel free to send better clustering value for me:)

E-mail: amirhr098@yahoo.com

SocialMedia: @Amirhr098
