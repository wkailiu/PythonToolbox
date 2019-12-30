### OpenCV背景去除[可以调参数]
* MOG
```python
import cv2
import numpy as np
if __name__ == "__main__":
    cap = cv2.VideoCapture(0)
    cap.set(3,2560) #设置分辨率
    cap.set(4,720)
    fgbg = cv2.bgsegm.createBackgroundSubtractorMOG()
    while(1):
        ret, frame = cap.read()
        fgmask = fgbg.apply(frame)

        cv2.imshow('frame',frame)
        cv2.imshow('fgmask',fgmask)
        k = cv2.waitKey(30) & 0xff
        if k == 27:
            break

    cap.release()
    cv2.destroyAllWindows()
```
* MOG2
```
cv2.createBackgroundSubtractorMOG2()
```
* GMG
```
cv2.bgsegm.createBackgroundSubtractorGMG()
```

### OpenCV畸变矫正
```C++
Mat src = imread( argv[1], 1 );
Mat distortion = src.clone();
Mat camera_matrix = Mat(3, 3, CV_32FC1);
Mat distortion_coefficients;
 
//导入相机内参和畸变系数矩阵
FileStorage file_storage("out_camera_data.xml", FileStorage::READ);
file_storage["Camera_Matrix"] >> camera_matrix;
file_storage["Distortion_Coefficients"] >> distortion_coefficients;
file_storage.release();
 
//矫正
undistort(src, distortion, camera_matrix, distortion_coefficients);
 
imshow("img", src);
imshow("undistort", distortion);
imwrite("undistort.jpg", distortion);

waitKey(0);
return 0;
```
### OpenCV SIFT
```python
import cv2
import numpy as np

if __name__ == "__main__":
    cap = cv2.VideoCapture(0)
    cap.set(3,2560) #设置分辨率
    cap.set(4,720)

    sift = cv2.xfeatures2d_SIFT.create()
    
    while(True):
        ret, frame = cap.read()
        
        kp, des = sift.detectAndCompute(frame, None)
        kp_image = cv2.drawKeypoints(frame, kp, None)
        
        cv2.imshow('kp_image', kp_image)
        if cv2.waitKey(1) & 0xFF == ord('q'):
            break
```
### 仿射变换
```
cv.warpAffine()
```
> * https://blog.csdn.net/keith_bb/article/details/56331356