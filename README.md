I built an agent which uses computer vision to drive a go-kart autonomously in the SuperTuxKart game using only the screen image as input; it has no other knowledge about the game.


![](media/self_driving_kart.gif)  

The model is built in pytorch and is a fully convolutional network using an encoder-decoder structure with batch normalization to process the image and predict an “aim point”, which is an xy-coordinate of where the kart should drive. I coded a controller to handle the steering, acceleration, braking, and drifting of the kart based on this predicted aim point.