JImageLoader
=======
A asynchronous web image loader with CircleProgressView written in Swift

<img src="https://raw.githubusercontent.com/joehour/JImageLoader/master/Example/pic.gif"  />

Features
----------

- [x] Simple methods with UIImageView Category.
- [x] Support CircleProgressView.
- [x] Support complete and progress handler.
- [x] Using NSURLSession module to download image.

Requirements
----------

- iOS 7.0+
- Xcode 7.3+ Swift 2.2

Installation
----------

#### CocoaPods

Check out [Get Started](https://guides.cocoapods.org/using/getting-started.html) tab on [cocoapods.org](http://cocoapods.org/).

To use ScratchCard in your project add the following 'Podfile' to your project

       source 'https://github.com/joehour/JImageLoader.git'
       platform :ios, '7.0'
       use_frameworks!

       pod 'JImageLoader', '~> 1.0.0'

Then run:

    pod install

Example
----------

####Please check out the Example project included.

#####Basic setting:

       UIImageView.LoadImageFromUrl("https://raw.githubusercontent.com/joehour/JImageLoader/master/Example/test.jpg")

#####Advanced setting: (web image contentMode, circleProgress size, complete and progress hanlder)

       UIImageView.LoadImageFromUrl("https://raw.githubusercontent.com/joehour/JImageLoader/master/Example/test.jpg", contentMode: .ScaleAspectFit,CircleProgressViewParameters: CircleProgressParameters(width: 50, height: 50, linewidth: 3, alpha: 0.7, fillColor: UIColor.clearColor(), strokeColor: UIColor.greenColor(), backgroundColor: UIColor.blackColor() ), progress: {(Prograss: Float) in

           print(Prograss)

           } ,completion: { ( Sucess: Bool) in
           if(Sucess){
              dispatch_async(dispatch_get_main_queue(),{

              })           
             }
            }
           )



License
----------

JImageLoader is available under the MIT License.

Copyright © 2016 Joe.

