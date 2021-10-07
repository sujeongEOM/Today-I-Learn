# :sparkles:png/jpg/jpeg

- pillow  
```python
from PIL import Image  

#image 파일 읽기
img = Image.open()

#resize
img = img.resize((w, h))

#into array
img_arr = np.asarray(img)

#color image일 때 RGB 평균값으로 grayscale로 변경
img_arr = np.mean(img_arr, axis=2)

#color inversion (흑백 반전)
img_arr = np.abs(255-image)

# pixel 0-1 rescale
img_arr = img_arr.astype(np.float32)/255.

#reshape 
img_arr = np.reshape(img_arr, (batch, w, h)) #reshape 하고 싶은 shape 설정
```
