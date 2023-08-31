# youtube-api-stat
## Objectives and background
Established in 2005, YouTube has evolved into the world's second-largest search platform, processing over 3 billion searches monthly, second only to Google [[1]](https://www.mushroomnetworks.com/infographics/youtube---the-2nd-largest-search-engine-infographic/). Nevertheless, comprehending the inner workings of the YouTube algorithm and the factors influencing video views and recommendations remains somewhat enigmatic. YouTube boasts one of the most extensive and intricate recommendation systems in the industrial landscape [[2]](https://dl.acm.org/doi/10.1145/2959100.2959190). For novice content creators, grasping why some videos garner views while others languish is a formidable challenge. A multitude of "myths" surrounds the success of YouTube videos [[3]](https://vidiq.com/blog/post/5-youtube-algorithm-myths-youtubers-need-to-know-about/). These myths encompass beliefs such as the significance of likes or comments, as well as the optimal video duration. Additionally, it's worthwhile for creators to experiment and identify "trends" within the niches covered by YouTube channels.  

In this project, the YouTube API key is needed to obtain the data from YouTube. In this demonstration, a Taiwanese YouTube Channel called "攝圖日記" is used to do the data analysis. Other YouTube channels can also be analysed if the channel ID is obtained.  

As the YouTuber may upload a new video to the channel, it may affect the statistics for the worse-performing video results.  
## Which data can be analysed?
Null values in the data frame should be checked before analysing data. After converting count columns to numeric and duration to seconds, tag count can also be added to the data frame. Once the data is pre-processed, library Seaborn can be used to plot the bar chart of the best and worst performing videos. If we want to visualize the video distribution per video, we can also use the violin plot to present the data. The relationship between view count and like as well as comment count can be presented by scatter plot. A histogram is a good way to visualize the distribution of video duration. Please note that originally Seaborn could not support Chinese characters, we need to type the following codes:
```
import matplotlib.pyplot as plt
from matplotlib.font_manager import fontManager

!wget -O TaipeiSansTCBeta-Regular.ttf https://drive.google.com/uc?id=1eGAsTN1HBpJAkeVM57_C7ccp7hbgSz3_&export=download
fontManager.addfont('TaipeiSansTCBeta-Regular.ttf')
mpl.rc('font', family='Taipei Sans TC Beta')
```
to display Chinese characters normally.  

Another interesting analysis is that you can use Natural Language Processing (NLP) to make the word cloud. In this project, words in video titles are selected to make the word cloud. Please check the ipynb file to see the result.  

Some people may be interested in the upload schedule of the YouTube channel. So a bar chart which reflects the upload schedule (from Monday to Sunday) is plotted. 
