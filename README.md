![445f0eb9fc8f3ed1679e](https://user-images.githubusercontent.com/56389219/180685647-ce3c94d0-763c-4a60-b985-04ba0aa89596.jpg)
![ad43159de4ab26f57fba](https://user-images.githubusercontent.com/56389219/180685679-b35b7408-7da6-45fa-a46d-4d90446d0f10.jpg)
![fffea4bd598b9bd5c29a](https://user-images.githubusercontent.com/56389219/180685697-38c11a23-b27c-46ea-a478-26af6f03bb57.jpg)

# XmlToTxt
ImageNet file xml format to [Darknet](https://github.com/pjreddie/darknet) text format.
Works well with directories and subdirectories.

### Installation
```bash
sudo pip install -r requirements.txt
```
### Usage

```bash
python xmltotxt.py -c cls.txt -xml xml -out out
```
#### Mandatory arguments

```bash
-xml 
```
#### Optional arguments

```bash
-c, -out
```

### Example

Input xml file.

```xml
<annotation>
	<filename>image-0000016.jpg</filename>
	<size>
		<width>1920</width>
		<height>1080</height>
	</size>
	<object>
		<name>sedan</name>
		<bndbox>
			<xmin>75</xmin>
			<ymin>190</ymin>
			<xmax>125</xmax>
			<ymax>210</ymax>
		</bndbox>
	</object>
</annotation>
```
Output text file.
```text
5 0.052083 0.185185 0.026042 0.018519
```

### Motivation

I used [Darknet](https://github.com/pjreddie/darknet) for real-time object detection and classification. Sometimes you need to collect your own training dataset for train your model. I collected training dataset images and fine awesome [tool](https://github.com/tzutalin/labelImg) for labeling images. But it generates xml files. So I needed to implement tool which translates from ImageNet xml format to Darknet text format.
Also compatible with latest [YOLOv5](https://github.com/ultralytics/yolov5) by Ultralytics.
