# python_file_test.py
import os
img_dir = './고래상어/'
# 너무 작은 이미지는 삭제
for filename in os.listdir(img_dir):
    file_path = os.path.join(img_dir, filename)
    # 파일
    if os.path.isfile(file_path):
        # file size
        file_size = os.path.getsize(file_path)
        print(file_size)
        if file_size < 1000:
            print('delete')
            os.remove(file_path)
