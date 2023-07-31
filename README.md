# Hand_Detection
Hand_Tracking

# 1. MediaPipe Models: 
As discussed previously MediaPipe pipeline is based on a graph that uses different subgraphs like hand landmark tracking subgraph from landmark module and renders using hand renderer subgraph and from palm detection module a palm detection subgraph.

# 2. Hand Detection using MediaPipe:
MediaPipe is open-source library released by Google. Which is 3-D based state of art dataset for object detection. All previous frameworks were based on 2-D object detection. With this library we can predict, capture object, angle, and position in 3 dimensions. It is a framework for creating pipelines to have implication over arbitrary data. With MediaPipe a perception pipeline is built as graph and Sensory data enter the graph, which comes out as localized data (Hand or Face landmarks), after passing through media processing algorithms.

# 3. Hand Gesture Recognition:
Using MediaPipe to predict hand landmarks in real time environment is pretty much straight forward. Where hand detection method is precisely explained as above. In this section we will describe in detail how we can use hand detection model, plot 21 landmarks on hand and use them to differentiate different hand gestures.
In this section we will go side by side with python code to explain detection and plotting algorithm of landmarks on hand. Figure shows sample picture of hand landmarks which are being plotted using MediaPipe library.

<img src="https://imgur.com/a/POGf6vH">

# 4. Gesture Recognition Algorithm:
With reference to figure , where MediaPipe library is used to find landmarks on hand in real time. This algorithm is very simple itself but let’s have a look in more details.
Detection is initialized by calling MediaPipe library in the beginning and then drawing and plotting variables are defined. Using this library and model we can detect 2 hands at the same time and then classify them as left and right hand. As depicted above if we run this algorithm, we will get landmarks plotted on our hand.
We are using MediaPipe library not only for detection but also for tracking purpose. To track our object, we need its coordinates in real time. Also, the same is mentioned above in detection method that these landmarks are plotted in 3D so there are going to be x, y and z coordinates. x and y are normalized respectively to [0.0, 1.0] by image width and height. z represents depth of landmark, and such depth is calculated from wrist as origin. The magnitude of these values depends upon distance from camera. Closer the hand the values will be smaller.
