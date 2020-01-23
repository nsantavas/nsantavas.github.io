---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---


<center><img src="files/hand.png" class="centerImage" height="300" width="300"  />
</center>
<br />

# Abstract
---


<div style="text-align: justify">
 Vision based human pose estimation is an non-invasive technology for human-computer interaction (HCI). Direct use of the hand as an input device provides an attractive interaction method, with minimum need for specialized equipment, such as exoskeletons, gloves etc, but a camera and a processing platform. Various applications exploit algorithms which have the capability of estimating a hand's pose. Such applications include control of robotics systems, video games, computer-generated imagery (CGI) etc. In this letter, we present a novel Convolutional Neural Network architecture, reinforced with a Self-Attention module that it could be deployed on an embedded system, due to its lightweight nature, with just <B><i>1,9 Million</i></B> parameters.
 </div>

<br />
<center>
<a href="https://arxiv.org/abs/2001.08047" ><font size="6">Paper </font></a>
</center>
<br />
<br />

# Method Overview
---

<div style="text-align: justify">
The presented architecture is based on the very successful
idea of DenseNets. In a DenseNet, each layer obtains
additional inputs from all preceding ones and propagates its
own feature-maps to all subsequent layers, by a channel-wise
concatenation.
 </div>

<br />
 <center><img src="files/densenet.png" class="centerImage" height="140" width="600"  />
 <figcaption>Dense Block with growth rate <i>k</i></figcaption>
</center>
<br />

<div style="text-align: justify">
We implement the <i>inverted bottleneck block</i>,
enhanced by an <i>Attention Augmented Convolutional layer</i>,
which output is added to the product of the Depthwise Separable Convolutional layer, as shown to the following figure.
</div>

<br />
 <center><img src="files/aaib.png" class="centerImage" height="220" width="280"  />
 <figcaption>Attention Augmented Inverted Bottleneck Layer</figcaption>
</center>
<br />

# Results
---

<center>
<div class="masonry">
  <img src="files/pck.png" width="32%"  alt>
  <img src="files/pck_h.png" width="32%" alt>
  <img src="files/pck_all.png" width="32%"  alt>
</div>
</center>


<br />
<br />
<br />
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:5px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:5px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg .tg-9wq8{border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-wh93{font-weight:bold;border-color:#cccccc;text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-7btt{font-weight:bold;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-o57c{border-color:#cccccc;text-align:center;vertical-align:top}
</style>
<table class="tg" align='center'>
  <tr>
    <th class="tg-c3ow" rowspan="2"></th>
    <th class="tg-9wq8" rowspan="2">AUC</th>
    <th class="tg-c3ow" colspan="2">EPE (px)</th>
  </tr>
  <tr>
    <td class="tg-c3ow">Mean</td>
    <td class="tg-c3ow">Median</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">MPII+NZSL Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Zimm. et al. (ICCV 2017)</td>
    <td class="tg-c3ow">0.17</td>
    <td class="tg-c3ow">59.4</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Bouk. et al. (CVPR 2019)<br></td>
    <td class="tg-c3ow">0.50</td>
    <td class="tg-c3ow">18.95</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Ours<br></td>
    <td class="tg-7btt">0.55</td>
    <td class="tg-7btt">16.1</td>
    <td class="tg-7btt">11</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">LSMV Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Gomez-Donoso et al.</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">10</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Li et al.</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">8</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-wh93">Ours</td>
    <td class="tg-o57c">0.89</td>
    <td class="tg-wh93">3.3</td>
    <td class="tg-o57c">2.5</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">Stereo Hand Pose Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Zimm et al. (ICCV 2017)</td>
    <td class="tg-c3ow">0.81</td>
    <td class="tg-c3ow">5</td>
    <td class="tg-c3ow">5.5</td>
  </tr>
  <tr>
    <td class="tg-7btt">Ours</td>
    <td class="tg-7btt">0.92</td>
    <td class="tg-7btt">2.2</td>
    <td class="tg-7btt">1.8</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">FreiHand Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Ours</td>
    <td class="tg-c3ow">0.87</td>
    <td class="tg-c3ow">4</td>
    <td class="tg-c3ow">3.1</td>
  </tr>
</table>



# Examples
---

<center>
<div class="masonry">
  <img src="files/images/hand1.png" width="32%"  alt>
  <img src="files/images/hand2.png" width="32%"  alt>
  <img src="files/images/hand3.png" width="32%"  alt>

  <img src="files/images/hand14.png" width="32%"  alt>
  <img src="files/images/hand11.png" width="32%"  alt>
  <img src="files/images/hand12.png" width="32%"  alt>

  <img src="files/images/hand18.png" width="32%"  alt>
  <img src="files/images/hand19.png" width="32%"  alt>
  <img src="files/images/hand20.png" width="32%"  alt>

  <img src="files/images/hand29.png" width="32%"  alt>
  <img src="files/images/hand26.png" width="32%"  alt>
  <img src="files/images/hand27.png" width="32%"  alt>

  <img src="files/images/hand35.png" width="32%"  alt>
  <img src="files/images/hand37.png" width="32%"  alt>
  <img src="files/images/hand41.png" width="32%"  alt>
</div>
</center>

### Citation
---
If you find this paper useful in your research, please consider citing:

	@article{huang2019convolutional,
	 title={Convolutional Networks with Dense Connectivity},
	 author={Huang, Gao and Liu, Zhuang and Pleiss, Geoff and Van Der Maaten, Laurens and Weinberger, Kilian},
	 journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
	 year={2019}
	 }
