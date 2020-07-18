# locana

**locana (लोचन)** - Sanskrit for ***"sight"***

This project aims at building a system to recognize hand gestures in images and eventually a live camera feed. No pretrained models are being used. The current approach leverages convolutional neural networks implemented using Tensorflow. At the moment only using one data source is being used for training and testing, but I am planning to integrate several others in the near future to improve the real world performance of the model (more about the data below).

This is a work on progress and the final goal is fully bundled python package that can be used in other projects to make gesture recognition more accessible.

![undraw_chat_bot_kli5](https://user-images.githubusercontent.com/25454503/87858885-67c89300-c931-11ea-8f39-9bab5b983a89.png)

### Installation & Usage

The current code only has a few things you need before you can get up and running. Depending on your environment you might want to use **pip** or **conda** to install all the necessary dependencies.

```python
# Install dependencies with pip
pip install tensorflow scikit-learn pandas numpy tqdm pillow

# Install dependencies with conda
conda install -c conda-forge tensorflow scikit-learn pandas numpy tqdm pillow
```

You also need Jupyter to be able to open the notebook. Again depending on your environment, pick the proper command to install.

```python
pip install juypter
# or
conda install jupyter
```

Now simply navigate to the root directory of the repo and run ```jupyter notebook``` in the command line (don't forget to activate your environment first if you are using conda).

### Data Sources

As stated earlier, the project is currently based on only one dataset, the [Hand Gesture Recognition Database](https://www.kaggle.com/gti-upm/leapgestrecog). It contains images of 10 different gestures with 2000 images per gesture. The images are given in gray scale and all have the same resolution, making for an easy starting point to train a model, but also invites overfitting. A few example images are given below.

![dataset-cover](https://user-images.githubusercontent.com/25454503/87858687-018f4080-c930-11ea-82f2-0b68cd659bad.png)

### Planned Progress

Given the very homogenous data and the overfitting that comes with it, I am planning on introducing several more data sources to diversify the images in quality, size, angle etc. That should help creating a model with a more robust performance in real world scenarios. Additionally the CNN structure sure could need some more research and tweaking and the whole thing should be able to recognize gestures in real time. This is very much a work in progress.

#### Upcoming ToDos:

- Find & integrate new data sources
- Improve data augmentation setup
- Change/tweak CNN structure
- Capture live webcam feed & run it through processing pipeline and model

&nbsp;

![Daniel Putzer, 2020](https://i.ibb.co/LSxTsY3/dan.png "Daniel Putzer, 2020")  
<https://danielputzer.com>
