# AI配音多风格分类音频语料

### 风格分类数据集

出门问问旗下有一款业界知名的AI配音神器[魔音工坊](https://www.moyin.com/)，其中有一个[听声识人功能](https://mp.weixin.qq.com/s/6grvwjEiHVyubdagVewXCA)，这是我们对声纹系统应用的一次尝试。由于魔音工坊拥有几百个speaker，每个speaker又拥有多种风格。根据中意的声音去查找speaker和对的应风格，对于一般用户来讲是非常困难的。我们基于这些风格数据和声纹技术做了一些尝试。目前选择部分数据面向公众开放。

## 数据格式简介
  - 一共 50 个 speaker
  - 每个 speaker 包含至少两种风格
  - 总音频时长 60h
  - 数据格式：
    - 音频：mp3
    - 文件名字：speaker_id-style_id-wav_id.mp3
  - 数据以`*.tar.bz2`形式提供，解压后的一级目录结构是
    - style.csv：格式`speaker_id,style_id,audio_path`
    - style_data：音频文件所在目录

| 文件名字组成 | 说明            |
| ------------ | --------------- |
| `speaker_id` | speaker的唯一ID |
| `style_id`   | style的唯一ID，不同speaker会有相同的style   |
| `wav_id`     | 音频的唯一ID    |


## 数据下载

### 下载地址

数据集的下载链接如下：
  - http://share.mobvoi.com:5000/sharing/WcaXmxYDK

  ![下载链接](../images/qr_code_style_data.png)

### 完整性校验

数据集的 `MD5` 摘要信息如下。在下载完成后，可以通过对比该摘要信息来验证下载数据的完整性。
  - `dd949c9a59532ba4f503a10edcb90d4d`

比如在Linux系统上，可使用如下命令来计算下载后数据的 `MD5` 摘要信息：

  ```shell
  md5sum <下载后保存的文件路径>
  ```

### 数据解压

请在下载完成之后进行解压，以得到最终的开源数据。

比如在Linux系统上，可使用如下命令来进行解压：

  ```shell
  tar xvfj <压缩包文件>
  ```
