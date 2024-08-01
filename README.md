
# Reflexion Pipeline

This project implements a Reflexion Pipeline, which allows for iterative task refinement and evaluation.
this file can be used as a module in your own computer
just clone the repo and use the file path as a module(better keep this file in your directory where you are trying to import it)
still a work in progress a lot of optimizations and work is in progress

## Usage

Here's a basic example of how to use the Reflexion Pipeline:

<pre><div class="relative flex flex-col rounded-lg"><div class="text-text-300 absolute pl-3 pt-2.5 text-xs">python</div><div class="pointer-events-none sticky my-0.5 ml-0.5 flex items-center justify-end px-1.5 py-1 mix-blend-luminosity top-0"><div class="from-bg-300/90 to-bg-300/70 pointer-events-auto rounded-md bg-gradient-to-b p-0.5 backdrop-blur-md"><button class="flex flex-row items-center gap-1 rounded-md p-1 py-0.5 text-xs transition-opacity delay-100 hover:bg-bg-200"><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" viewBox="0 0 256 256" class="text-text-500 mr-px -translate-y-[0.5px]"><path d="M200,32H163.74a47.92,47.92,0,0,0-71.48,0H56A16,16,0,0,0,40,48V216a16,16,0,0,0,16,16H200a16,16,0,0,0,16-16V48A16,16,0,0,0,200,32Zm-72,0a32,32,0,0,1,32,32H96A32,32,0,0,1,128,32Zm72,184H56V48H82.75A47.93,47.93,0,0,0,80,64v8a8,8,0,0,0,8,8h80a8,8,0,0,0,8-8V64a47.93,47.93,0,0,0-2.75-16H200Z"></path></svg><span class="text-text-200 pr-0.5">Copy</span></button></div></div><div><div class="code-block__code !my-0 !rounded-lg !text-sm !leading-relaxed"><code class="language-python"><span><span class="token">from</span><span> reflexion </span><span class="token">import</span><span> ReflexionPipeline
</span></span><span>
</span><span><span></span><span class="token"># Initialize the pipeline with a model name</span><span>
</span></span><span><span>reflexion </span><span class="token">=</span><span> ReflexionPipeline</span><span class="token">(</span><span>model_name</span><span class="token">)</span><span>
</span></span><span>
</span><span><span></span><span class="token"># Define your task</span><span>
</span></span><span><span>task </span><span class="token">=</span><span></span><span class="token">""</span><span>
</span></span><span>
</span><span><span></span><span class="token"># Run the reflexion loop</span><span>
</span></span><span><span>final_task</span><span class="token">,</span><span> final_output</span><span class="token">,</span><span> final_evaluation </span><span class="token">=</span><span> reflexion</span><span class="token">.</span><span>reflexion_loop</span><span class="token">(</span><span>task</span><span class="token">,</span><span> max_iterations</span><span class="token">=</span><span class="token">5</span><span class="token">,</span><span> criteria</span><span class="token">=</span><span class="token">0.9</span><span class="token">)</span></span></code></div></div></div></pre>

## Parameters

* `model_name`: The name of the model to use for the Reflexion Pipeline.`<br>`
* `task`: The initial task or prompt to refine and evaluate.`<br>`
* `max_iterations`: The maximum number of iterations for the reflexion loop (default is 5).`<br>`
* `criteria`: The exit criteria score (between 0 and 1) at which the loop will stop if reached before max_iterations (default is 0.9).

## Customization

You can customize the Reflexion Pipeline by adjusting the following parameters:

* `max_iterations`: Set this to the number of reflexion iterations you want to perform.`<br>`
* `criteria`: Adjust this value to change the satisfactory score at which the loop will exit early.

## Output

The `reflexion_loop` method returns three values:

1. `final_task`: The refined task after iterations.`<br>`
2. `final_output`: The final output generated for the task.`<br>`
3. `final_evaluation`: The evaluation score for the final output.

## Note

Make sure to define your `task` variable with an appropriate prompt or task description before running the reflexion loop.
