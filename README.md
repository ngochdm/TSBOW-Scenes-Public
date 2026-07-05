<!-- 
__        _______ _     ____ ___  __  __ _____ 
\ \      / / ____| |   / ___/ _ \|  \/  | ____|
 \ \ /\ / /|  _| | |  | |  | | | | |\/| |  _|  
  \ V  V / | |___| |__| |__| |_| | |  | | |___ 
   \_/\_/  |_____|_____\____\___/|_|  |_|_____|
                                   
 _____ ___  
|_   _/ _ \ 
  | || | | |
  | || |_| |
  |_| \___/ 
            

 _____ ____  ____   _____        __
|_   _/ ___|| __ ) / _ \ \      / /
  | | \___ \|  _ \| | | \ \ /\ / / 
  | |  ___) | |_) | |_| |\ V  V /  
  |_| |____/|____/ \___/  \_/\_/   
                                   
-->

# Filter Scenes in TSBOW

A lightweight web interface for browsing and filtering scene samples from the TSBOW dataset by weather, scenario, road type, and scale.

![Example UI](images/Example_UI.png)



<!-- MARK: Website -->

## 🌐 Website

The online demo is available at:

https://ngochdm.github.io/TSBOW-Scenes-Public/



<!-- MARK: Local run -->

## 🚀 Run Locally

Clone or open this repository, then start a local HTTP server from the project root:

```bash
cd Filter-Scenes-TSBOW/

# Start the local server and open the viewer
./local_open_TSBOW_filter_scenes.sh
```

or

```bash
cd Filter-Scenes-TSBOW/

# Start the local server and open the viewer
./local_run_TSBOW_filter_scenes.sh
```

Then, open your browser and navigate to:
> http://localhost:8000/index.html

By default, the viewer opens in your default browser at:
> http://localhost:8000/index.html

To use another port:
```bash

./local_open_TSBOW_filter_scenes.sh 8080
```

A **local HTTP server is recommended** because the page loads `TSBOW_info.csv` using JavaScript.
Press `Ctrl+C` in the terminal to stop the server.



<!-- MARK: Attribute -->

## 🎬 Scenes Filtering

The interface supports filtering scenes by the following attributes:

1. **Weather**: All, Normal, Haze, Rain, Snow

2. **Scenario**: All, Road, Intersection, Special Cases, Disaster

3. **Road Type**: All, Urban, Standard, Boulevard

4. **Scale**: All, Fine, Medium, Coarse

Select the desired attributes and click the `FILTER` button to display matching scenes.



<!-- MARK: Metadata -->

## 📄 Dataset Metadata

Scene metadata is stored in `TSBOW_info.csv`.

The CSV file uses the following column order: 

```text
VIDEO_ID, SCENARIO, DAYTIME, WEATHER, SCALE, ROADTYPE, DURATION
```

<!-- `videoID`, `scenario`, `daytime`, `weather`, `scale`, `roadtype`, `duration`. -->

The filtering logic in `js/main.js` expects the same order:

```js
const [videoID, scenario, daytime, weather, scale, roadtype, duration] = row;
```

If the CSV structure changes, update the parsing logic in `js/main.js` accordingly.



<!-- MARK: Intro -->

## 🌍 About TSBOW

**Comprehensive, annotated dataset for object detection.**
This dataset consists of over 32 hours of real-world traffic surveillance data across 71 CCTV and an additional color cameras, spanning annual weather conditions ([See Demo Videos](https://skkuautolab.github.io/TSBOW/TSBOW_scenes.html)). 

The TSBOW dataset is publicly available at [TSBOW Github](https://github.com/SKKUAutoLab/TSBOW).

- *<span style="color: #FFCC00; font-weight: bold;">Hardware</span>*: CCTV system + color camera. 
- *<span style="color: #33CCCC; font-weight: bold;">Tasks</span>:* Object Detection.
- *<span style="color: #FF6600; font-weight: bold;">Position</span>:* South Korea. 
- *<span style="color: #6699FF; font-weight: bold;">Weather</span>:* sunny/cloudy, haze, rain, snow. 
- *<span style="color: #FF0066; font-weight: bold;">Daytime</span>:* day.



<!-- MARK: Citation -->

## 🏅 Citation

**If our research is helpful to you, please cite our paper using the following BibTeX format**

```bibtex
@article{Huynh2026TSBOW, 
    title={TSBOW: Traffic Surveillance Benchmark for Occluded Vehicles Under Various Weather Conditions}, 
    author={Huynh, Ngoc Doan-Minh and Tran, Duong Nguyen-Ngoc and Pham, Long Hoang and Tran, Tai Huu-Phuong and Jeon, Hyung-Joon and Nguyen, Huy-Hung and Khac Vu, Duong and Jeon, Hyung-Min and Phan, Son Hong and Pham-Nam Ho, Quoc and Tran, Chi Dai and Khanh, Trinh Le Ba and Jeon, Jae Wook}, 
    journal={Proceedings of the AAAI Conference on Artificial Intelligence}, 
    volume={40}, 
    number={7}, 
    url={https://ojs.aaai.org/index.php/AAAI/article/view/37439}, 
    DOI={10.1609/aaai.v40i7.37439}, 
    year={2026}, 
    month={Mar.}, 
    pages={5239-5247} 
}
```

<!-- ```bibtex
@misc{huynh2026tsbowtrafficsurveillancebenchmark,
      title={TSBOW: Traffic Surveillance Benchmark for Occluded Vehicles Under Various Weather Conditions}, 
      author={Ngoc Doan-Minh Huynh and Duong Nguyen-Ngoc Tran and Long Hoang Pham and Tai Huu-Phuong Tran and Hyung-Joon Jeon and Huy-Hung Nguyen and Duong Khac Vu and Hyung-Min Jeon and Son Hong Phan and Quoc Pham-Nam Ho and Chi Dai Tran and Trinh Le Ba Khanh and Jae Wook Jeon},
      year={2026},
      eprint={2602.05414},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2602.05414}, 
}
``` -->



<!-- MARK: Contact -->

## 📧 Contact

**For any inquiries regarding this work, please contact:**

- Name: `Huynh Doan Minh Ngoc` 

- Email: ngochdm@gmail.com / ngochdm@skku.edu
