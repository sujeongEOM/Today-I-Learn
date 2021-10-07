# about Medical data   
## :point_right: MRI  
#### Brain MRI: NifTI 파일 형식(.nii.gz) > using **_nibabel_** (python package)  
MRI data는 여러개의 이미지가 axis=2에 쌓여있는 형태   
ex) (220, 220, 180) : pixel 220x220 이미지가 180개 있음 = volume, voxel?
- nibabel 문법  
```python
img = nibabel.load(file)      #NifTI 이미지 반환  
img.dataobj                   #array proxy 반환  
img.dataobj[...]              #array proxy 슬라이싱 가능. numpy array 반환
img.get_fdata()               #numpy array 반환  
```
- 
## DICOM
## EKG


## Reference
[MRI] (https://nipy.org/nibabel/images_and_memory.html)
