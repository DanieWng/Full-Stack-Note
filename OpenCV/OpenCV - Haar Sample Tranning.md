#OpenCV - Haar Sample Tranning

* 적절한 이미지의 배경색은 동일하면 좋음
* gray 권장
* 각도에 따라 다양하게
* 图片归一化或者特征归一化
* 부절한 샘플중에 가능하면 적저한 샘플의 배경 있으면 좋음
* 샘플 비율 1:2? 1:3?
* opencv_traincascade & vec 사이즈 같은


###적절한 샘플 준비
* 자동 합성 경우:
	
	* `opencv_createsamples -img 적절한 이미지 파일 경로 -bg neg.txt -info pos/pos.txt -num 2000 -w 100 -h 100`
	* **w**는 합성된 **적절한 샘플 영역**의 가로 길이
	* **h**는 합성된 **적절한 샘플 영역**의 세로 길이
	* 불적절한 샘플 크기는 150x150, 여기에서 최대 길이(100x100)였음.