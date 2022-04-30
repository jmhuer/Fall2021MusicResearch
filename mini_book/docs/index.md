---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

## VaryCHarm: A Method to Automatically Vary the Complexity of Harmonies in Music

 <sub> <a href="https://jmhuer.github.io/mini_book/_build/html/docs/portfolio.html" style="color: red; text-decoration: underline;text-decoration-style: dotted;">Github Repository</a> </sub>

<img src="../../../../images/varycharm.png" align="center"/>

<br>

Automatically varying the number of notes in symbolic music has various applica-
tions in assisting music creators to embellish simple tunes or to reduce complex
music to its core idea. In this paper, we formulate the problem of varying music
complexity, and propose a method that can preserve harmonic structure while
varying the number of notes. Our method, VaryCharm, adopts an autoencoder
architecture in combination with a masking mechanism to control the number of
notes of the generated music.


## Sample Usage
``` 
import IPython.display
import libfmp.c1

ratio = 1.5
example = # 
original = example.to(device)
output = varycharm.batch_Harmonytransformation(original, ratio, res=50)

original_roll = original[1][0].detach().cpu()
piano_roll = output[1][0].detach().cpu()

print("original_roll note_count: ", float(_note_count(original_roll)))
print("original_roll pitch_diversity: ", float(pitch_diversity(original_roll)))
pm = play_and_write(original_roll , name="ORIGINAL")
visualize(pm)


print("piano_roll note_count: ", float(_note_count(piano_roll)))
print("piano_roll pitch_diversity: ", float(pitch_diversity(piano_roll)))
pm = play_and_write(piano_roll , name="ratio0p7")
visualize(pm)

``` 
<img src="../../../../images/outcode.png" width="65%"  align="center"/>
<div align="center">
<br>


## Results
---

### Example 1
<img src="../../../../images/example1a-1.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example1a-1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example1a-2.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example1a-2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example1a-3.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example1a-3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

---
### Example 2
<img src="../../../../images/example2a-1.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example2a-1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example2a-2.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example2a-2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example2a-3.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example2a-3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

---
### Example 3 - Added Notes as Strings
<img src="../../../../images/example3a-1.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example3a-1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example3a-2.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example3a-2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>

<img src="../../../../images/example3a-3.png" width="70%"  align="center"/>
<div align="center">
<audio controls>
  <source src="../../../../audio/example3a-3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> </div>
<br>
<br>




<!-- Our results indicate the end-to-end autoencoder-BiLSTM Lifetime method outperforms a simple music theory baseline, and a regular auto encoder according to the metrics discussed. The current method does have a few limi- tations. Namely we are compressing pitch information and most of the added embellishments are added vertically and depend on build on the existing rhythm. However, we believe this method and evaluation scheme provides some ground work for exploring rhythmic components to potentially be extended. -->






