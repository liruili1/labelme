# labelme
#separte the test and train





import os
import shutil
img_dir = "C:/Users/lirui/desktop/data/train/imgs"
mask_dir = "C:/Users/lirui/desktop/data/train/masks"
test_img_dir =  "C:/Users/lirui/desktop/data/test/imgs"
test_mask_dir = "C:/Users/lirui/desktop/data/test/masks"
img_list = sorted(os.listdir(img_dir))
test_ratio = 4

for idx,img_name in enumerate(img_list):
    if idx % test_ratio == 0:
        shutil.move(os.path.join(img_dir,img_name),os.path.join(test_img_dir,img_name))
        shutil.move(os.path.join(mask_dir,img_name),os.path.join(test_mask_dir,img_name))
