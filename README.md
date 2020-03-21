<html>
<body>


  <h1 align="center"><span style="font-size: 
      26px;">CMP684 Project</span></h1>
  <h1 align="center"><span style="font-size: 26px;"><strong>V<sub>s30</sub> Prediction from Earthquake Accelerograms</strong></span></h1>

  <p style="text-align: justify;"><span style="font-size: 19px;"><strong><span class="fontstyle0" style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial;">Earthquakes are recorded with seismograph devices all over the world especially at countries with high seismicity (eg. Turkey, Japan). Records of these devices, namely accelerograms (t</span></strong><strong><span style="float: none; color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial; display: inline !important;">he recording of the acceleration of the ground during an earthquake</span></strong><strong><span class="fontstyle0" style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial;">), vaguely reflects some characteristics of seismograph site.</span></strong><strong><span style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial; float: none; display: inline !important;">&nbsp;In this study, a parameter of site, average shear wave velocity of top 30 meters of soil (V<sub>s30</sub>) predicted using accelerograms recorded at the same site with the help of a neural network.</span></strong></span></p>
  <p align="center"><span style="font-size: 19px;"><strong><span style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial; float: none; display: inline !important;">
          <img src="./img/AFAD_istassyonlar.PNG" style="width: 637px;">
        </span></strong></span></p>
  <p align="center"><span style="font-size: 16px;"><strong><span style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial; float: none; display: inline !important;"><em>AFAD strong ground motion seismograph network [1].</em></span></strong></span></p>
  <p style="text-align: justify;"><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">In Turkey there are 679 seismograph devices actively working in AFAD's (Disaster &amp; Emergency Management Authority) strong ground motion seismograph network.</span><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">&nbsp;For 68 of those 679 seismographs the geological borehole log reports are available online [2] and for 258 seismographs the V<sub>s30</sub> value of site is known. V<sub>s30</sub> is accepted as a indicator of the hardness of soil of a site. If site has rock-type properties, V<sub>s30</sub> is high and if site has soil-type properties V<sub>s30</sub> is low. An example soil classification according to V<sub>s30&nbsp;</sub>values is shown below:</span></p>
  <p style="text-align: justify;">
    <br>
  </p>

<p align="center"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">
    <img src="./img/Site-Class-descriptions-and-their-V-S-30-ranges.png" height="220">
  </span></p>
<p align="center"><em>Soil classification table according to V<sub>s30</sub> values [3]</em></p>
<p align="center">
  <br>
</p>
<p align="center">
  <img src="./img/image001-1.gif" style="width: 436px;">
</p>
<p align="center"><em>Shear wave propagation in soil medium [4].</em></p>
<p style="text-align: justify;"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;"><span style="color: rgb(0, 0, 0); font-family: Tahoma, Geneva, sans-serif; font-size: 19px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: justify; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">In this study,</span> earthquakes recorded by seismographs with known V<sub>s30</sub> values are used. By the date 26.11.2019 (cut-off date for data gathering) there were around 20.000 earthquake records (Magnitude ≥ 3) caught by these 258 seismographs. Each of these records have three accelerograms in three perpendicular directions (north-south (<em>ns</em>), east-west (<em>ew</em>), up-down(<em>ud</em>)). A sample record shown below.</span></p>
<p align="center"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">
    <img src="./img/acc_sample.PNG" style="width: 639px;">
  </span></p>
<p align="center"><em>North-South, East-West and Up-Down records of earthquake recorded at station no 1009 at 2008.</em></p>
<p style="text-align: justify;"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">These records are not used directly in the training of neural network model. In order to standardize the input and to reflect the frequency dependent behavior better, accelerogram records converted to spectra using Niggam-Jennings methodology [5]. Spectra calculated for sample accelerograms are given below.</span></p>
<p align="center"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">
    <br>
    <img src="./img/rs_sample.PNG" style="width: 675px;">
  </span></p>

 <p align="center"><em>Spectra calculated for North-South, East-West and Up-Down records of earthquake recorded at station no 1009 at 2008.</em></p>
  <p style="text-align: justify;"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;"><span class="fontstyle0">Using the spectra derived from over 20.000 earthquake records a neural network model formed and trained in a way to <strong><u>extract&nbsp;</u></strong></span><strong><u><span class="fontstyle2">V</span><span class="fontstyle3"><sub>s</sub></span><span class="fontstyle4"><sub>30</sub>&nbsp;</span></u></strong><span class="fontstyle0"><u><strong>value from the relation between horizontal and vertical components of earthquake recordings.</strong></u> Thus North-South_Up-Down (<em>ns-ud</em> ) and East-West_Up-Down (<em>ew-ud</em> ) spectrum couples used as input and&nbsp;</span><span class="fontstyle2">V</span><span class="fontstyle3"><sub>s</sub></span><span class="fontstyle4"><sub>30</sub>&nbsp;</span><span class="fontstyle0">value used as output.</span>&nbsp;</span></p>
  <p style="text-align: justify;"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;"><u><strong>Neural Network Model</strong></u></span></p>
  <p style="text-align: justify;"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">Schematic of neural network model is given below:</span></p>
  <p align="center"><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 19px;">
      <img src="./img/model.PNG">&nbsp; 
    </span><span style="font-family: Tahoma, Geneva, sans-serif; font-size: 16px;"><em>&nbsp;Neural network model used in this study.</em></span></p>
 
  <p style="text-align: justify;">
    <br>
  </p>

<p style="text-align: justify;"><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">This study done by&nbsp;</span><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">Ali AKGÖZ (</span>
  <a href="mailto:aliakgoz@gmail.com"><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">aliakgoz@gmail.com</span></a><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">)</span><span style="font-size: 19px; font-family: Tahoma, Geneva, sans-serif;">&nbsp;as a term project for 
    <a href="https://web.cs.hacettepe.edu.tr/~onderefe/bil684/" rel="noopener noreferrer" target="_blank">CMP684 - Neural Networks Course</a> (Hacettepe University - Computer Engineering) under supervision of the instructor of the course 
    <a href="https://web.cs.hacettepe.edu.tr/~onderefe/" rel="noopener noreferrer" target="_blank">Prof. Dr. M.Önder EFE</a>.&nbsp;
  </span></p>
<p>
  <br>
</p>
<p>
  <br>
</p>
<p style="text-align: justify;"><strong>References:</strong></p>
<p style="text-align: justify;">[1] 
  <a href="https://deprem.afad.gov.tr/istasyonlar">https://deprem.afad.gov.tr/istasyonlar</a> &nbsp;
</p>
<p style="text-align: justify;">[2] 
  <a href="http://kyhdata.deprem.gov.tr/">http://kyhdata.deprem.gov.tr/</a>&nbsp; (currently unavailable due to maintenance. 17.03.2020)&nbsp;
</p>
<p style="text-align: justify;">[3] Building Seismic Safety Council, NEHRP Recommended Provisions for Seismic Regulations for New Buildings and Other Structures (Fema 450)," Part 1, no. Fema 450, p. 338, 2003.</p>
<p style="text-align: justify;">[4] 
  <a href="https://web.ics.purdue.edu/~braile/edumod/waves/Swave.gif">https://web.ics.purdue.edu/~braile/edumod/waves/Swave.gif</a> &nbsp;
</p>
<p style="text-align: justify;">[5] N. Nigam, P. Jennings, and C. I. of Technology Earthquake Engineering Research Laboratory, Digital calculation of response spectra from strong-motion earthquake records. California Institute of Technology, Earthquake Engineering Research Laboratory, 1968</p>




</body>
</html>