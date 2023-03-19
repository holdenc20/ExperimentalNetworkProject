<div id="project1" class="section" style="display: flex; justify-content: center; flex-direction: column; align-items: center; text-align: center;">
      <h4>Experimental Network Project</h4>
      <div class="row">
        <div class="col-md-6" style="text-align: center;">
          <h5>Goal</h5>
          <p>Using a dataset of brain CT images provided by a company called Zeta Surgical, we will develop models to accurately classify and segment brain hemorrhages in these CT images.</p>
          <h5>Zeta Surgical</h5>
          <p>A company focused on democratizing the access to accurate, safe and fast image guidance, to unlock the use of image guidance directly at the point-of-care, and to enable new treatments in cases such as emergenciies and bedside precedure.</p> 
        </div>
        <div class="col-md-6" style="text-align: center;">
          <img src="CTImage1.png" alt="Example CT image with hemorrhage" width="200" height="200" align="center" style="border: 1px solid black;">
        </div>
      </div>
      <br/>
      <h5>The CT Image Data Set</h5>
      <p>512x512 CT image scans labeled with locatiions of the hemorrhage in the brain and pixel coordinates of the outline of the hemorrhage.</p>
      <img src="CTImage3.png" alt="Types of CT hemorrhages" width="100%" height="500" align="center" style="border: 1px solid black;"> 
        <h5>Attempt 1: Standard Neural Network</h5>
        <ul style="text-align: left;">
          <li>Small-scale first attempt</li>
          <li>200 of each type of hemorrhaging</li>
          <li>Using sequential keras model</li>
        </ul>
        <img src="CTNN.png" alt="Standard Neural Network Results" width="60%" height="400" align="center" style="border: 1px solid black;"> 
        <h5>Attempt 2: Visual Transformer</h5>
        <p>This did not work...</p>
        <h5>Attempt 3: Transfer Learning - VGG16</h5>
        <p>VGG16 is a convolutional neural network model proposed by K. Simonyan and A. Zisserman from the University of Oxford in the paper "Very Deep Concolutional Networks for Large-Scale Image Recognition".</p>
        <img src="CTImage4.png" alt="VGG16" width="60%" height="400" align="center" style="border: 1px solid black;">
        <div style="display:inline; justify-content: center; flex-direction:row; align-items: center;">  
          <img src="CTImage5.png" alt="VGG16" width="45%" height="300" align="center" style="border: 1px solid black;">
          <img src="CTImage6.png" alt="VGG16" width="45%" height="300" align="center" style="border: 1px solid black;">
        </div>
        <h5>Attempt 4: Transfer Learning - ResNet</h5>
        <p>A convolutional neural network model with a residual block</p>
        <div style="display:inline; justify-content: center; flex-direction:row; align-items: center;">
           <img src="CTImage7.png" alt="ResNet" width="45%" height="350" align="center" style="border: 1px solid black;">
          <img src="CTImage8.png" alt="ResNet" width="45%" height="350" align="center" style="border: 1px solid black;">
        </div>
        <div style="display:inline; justify-content: center; flex-direction:row; align-items: center;">  
          <img src="CTImage9.png" alt="ResNet" width="45%" height="350" align="center" style="border: 1px solid black;">
          <img src="CTImage10.png" alt="ResNet" width="45%" height="350" align="center" style="border: 1px solid black;">
        </div>
        <h5>Main Takeaways</h5>
        <ul style="text-align: left;">
          <li>Our fourth attempt produced the best results for our data set, with a good accuracy of about 55-60% and no over fitting issues with the ResNet model.</li>
          <li>Despite the improved results seen with ResNet, accuracy was still below 60% which is not ideal for a medical implementation.</li>
          <li>Medical data is very difficult to apply current machine learning methods on, and moore development is required in this area before we can begin to see reliable results.</li>
          <li>We are also restricted by the processing power of our computers as processing even fairly small amounts of this data was slow.</li>
        </ul>
        <h5>Future implementation</h5>
        <ul style="text-align: left;">
          <li>Transfer learning on MedNet: Sihong Chen, Kai Ma, Yefeng Zheng: “Med3D: Transfer Learning for 3D Medical Image Analysis”, 2019; [http://arxiv.org/abs/1904.00625 arXiv:1904.00625].</li>
          <li>Federated Learning with distributed updates: J. Zhao et al., "Federated Learning With Heterogeneity-Aware Probabilistic Synchronous Parallel on Edge," in IEEE Transactions on Services Computing, vol. 15, no. 2, pp. 614-626, 1 March-April 2022, doi: 10.1109/TSC.2021.3109910.</li>          
        </ul>
    </div>
