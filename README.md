# DictShaper

**The module for convenient viewing of dictionary 
with the all necessary indents.**
---

This module extends the standard `dict` class, so you can
use all its properties and methods. Over all of this `DictShaper`
adds the new method `shape()`. You can also give a name for your
dictionary by the `name=` param.

`your_dictionary.shape(name='any_name')`

You can also add a path to a file for writing the dictionary there,
using the `write_to=` param. It will be writing in a convenient view,
like in an example below.

`your_dictionary.shape(name='any_name', write_to='any_path')`

If you set as a value `1` or `True` in `write_to=` param then the
dictionary will be writing to the end of a current file.

## EXAMPLES

We will work with the dictionary below called **'some dictionary'**.

`some_dictionary = {'Level-1 el-1': [0, 1, 2, 3, 4], 'Level-1 el-2': {'Level-2 el-1': 1, 'Level-2 el-2': 2}, 'Level-1 el-3': 'Some string', 'Level-1 el-4': ('Tuple', 1, ['a', 'b']), 'Level-1 el-5': {'Level-2 el-3': {'Level-3 el-1': 'https://some-site.com/page1?par=120&another=500', 'Level-3 el-2': (9, 125, 87), 'Level-3 el-3': 'Very very very very very very very very very very very very long string.'}, 'Level-2 el-4': 2}, 'Level-1 el-6': {}, 'Level-1 el-7': 'The end of the dictionary!'}`

## For output the dict to console without a name

### Enter following commands

> 1. `some_dictionary = DictShaper(some_dictionary)`
> 2. 
> 3. `print(some_dictionary.shape())`

### Output

<p><code>{<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-1': [0, 1, 2, 3, 4],<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-2': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-1': 1,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-2': 2,<br>
&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-3': 'Some string',<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-4': ('Tuple', 1, ['a', 'b']),<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-5': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-3': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-1': 'https://some-site.com/page1?par=120&another=500',<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-2': (9, 125, 87),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-3': 'Very very very very very very very very very very very very long string.',<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-4': 2,<br>
&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-6': {},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-7': 'The end of the dictionary!',<br>
}</code></p>

<h2>For output the dict to console with a name</h2>

<h3>Enter following commands</h3>

<code style="background: none; padding: 0;">
<ol style="padding: 5px; border: solid 2px #eee; background: #F0FFF0; color: #000000;">
<li>some_dictionary = DictShaper(some_dictionary)</li>
<li></li>
<li>print(some_dictionary.shape(name='shaped_dict'))</li>
</ol>
</code>

<h3>Output</h3>

<p style="background: #5F9EA0; padding: 5px;">
<code style="background: none; color: #fff; padding:0;">
shaped_dict = {<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-1': [0, 1, 2, 3, 4],<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-2': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-1': 1,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-2': 2,<br>
&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-3': 'Some string',<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-4': ('Tuple', 1, ['a', 'b']),<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-5': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-3': {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-1': 'https://some-site.com/page1?par=120&another=500',<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-2': (9, 125, 87),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-3': 'Very very very very very very very very very very very very very very long string.',<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-4': 2,<br>
&nbsp;&nbsp;&nbsp;&nbsp;},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-6': {},<br>
&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-7': 'The end of the dictionary!',<br>
}<br>
</code></p>

<h2>For write the dict to a file with a name</h2>

<code style="background: none; padding: 0;">
<ol style="padding: 5px; border: solid 2px #eee; background: #F0FFF0; color: #000000;">

<li>some_dictionary = DictShaper(some_dictionary)</li>
<li></li>
<li>some_dictionary.shape(name='shaped_dict', write_to=True)</li>
<li></li>
<li></li>
<li>shaped_dict = {</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-1': [0, 1, 2, 3, 4],</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-2': {</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-1': 1,</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-2': 2,</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;},</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-3': 'Some string',</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-4': ('Tuple', 1, ['a', 'b']),</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-5': {</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-3': {</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-1': 'https://some-site.com/page1?par=120&another=500',</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-2': (9, 125, 87),</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-3 el-3': 'Very very very very very very very very very very very very very very long string.',</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;},</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'Level-2 el-4': 2,</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;},</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-6': {},</li>
<li>&nbsp;&nbsp;&nbsp;&nbsp;'Level-1 el-7': 'The end of the dictionary!',</li>
<li>}</li>
<li></li>
</ol>
</code>