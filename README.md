# datachecking
Please help us to check whether there exists any "blank" audio segment. If so, delete it.

## 1. 文件描述
### 500 ms
内部包含一些文件夹，比如：caralarmTest, caralarmTrain, cleanTest, cleanTrain ...

每个子文件夹内部包含的是500ms的语音片段。
### 250 ms
内部包含一些文件夹，比如：caralarmTest, caralarmTrain, cleanTest, cleanTrain ...

每个子文件夹内部包含的是250ms的语音片段。

## 2. 需求描述
检查每个子文件夹中每个语音片段是否“合理”

### 2.1 对于 500 ms
#### 2.1.1 cleanTrain/cleanTest
"合理" （保留）：
* 能听到有人声说话, 并且相当清晰<br>
 example: cleanTrain/01bc020n_16.wav
* 能听到有人声， 但很短促<br>
 example: cleanTrain/01dc0203_8.wav
 
"不合理" （剔除）：
* 完全没有人声<br>
 example： cleanTrain/01bc0214_8.wav
#### 2.1.2 其他文件夹
包括：**caralarmTest, caralarmTrain, crowdTest, crowTrain, dogTest, dogTrain...**(噪音文件夹)

"合理" （保留）：
* 能明显听出有此类噪声的语音片段<br>
  example: keyboardTrain/4_0_6_6.wav, planeTrain/1_0_1_0.wav, dogTrain/36_0_4_2.wav
 
 "不合理" （剔除）：
 * 很难听出有此类噪声的语音片段<br>
  example: dogTrain/35_0_4_5.wav, dogTrain/36_0_4_1.wav
 * 完全没有此类噪声的语音片段<br>
  example: keyboardTrain/6_0_7_10.wav
### 2.2 对于 250 ms
