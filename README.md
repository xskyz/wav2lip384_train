
# 我来实际训一个版本.

0.py    输入数据在data_train里面. 一堆.mp4

1.py    syncnet

2.py    训练wav2lip网络

跑通代码.png  是我跑通的图.跑的wav2lip, 1.py也跑通了.

训完还是inference.py代码 使用方法跟wav2lip一样. 

目前计算资源有限还没训好. 有训完的可以issue一下交流.












## **Wav2Lip** - a modified wav2lip 384 version


Lip-syncing videos using the pre-trained models (Inference)
-------
You can lip-sync any video to any audio:
```bash
python inference.py --checkpoint_path <ckpt> --face <video.mp4> --audio <an-audio-source> 
```
The result is saved (by default) in `results/result_voice.mp4`. You can specify it as an argument,  similar to several other available options. The audio source can be any file supported by `FFMPEG` containing audio data: `*.wav`, `*.mp3` or even a video file, from which the code will automatically extract the audio.

Train!
----------
There are two major steps: (i) Train the expert lip-sync discriminator, (ii) Train the Wav2Lip model(s).

##### Training the expert discriminator
You can use your own data (with resolution 384x384)

```bash
python parallel_syncnet_tanh.py
```
##### Training the Wav2Lip models
You can either train the model without the additional visual quality disriminator (< 1 day of training) or use the discriminator (~2 days). For the former, run: 
```bash
python parallel_wav2lip_margin.py
```

# wav2lip384_my
# wav2lip384_my
#   w a v 2 l i p 3 8 4 _ m y 2 
 
 "# wav2lip384_my2" 
"# wav2lip384_my2" 


Lip-syncing videos using the pre-trained models (Inference)
You can lip-sync any video to any audio:

python inference.py --checkpoint_path <ckpt> --face <video.mp4> --audio <an-audio-source> 
The result is saved (by default) in results/result_voice.mp4. You can specify it as an argument, similar to several other available options. The audio source can be any file supported by FFMPEG containing audio data: *.wav, *.mp3 or even a video file, from which the code will automatically extract the audio.

Train!
There are two major steps: (i) Train the expert lip-sync discriminator, (ii) Train the Wav2Lip model(s).

Training the expert discriminator
You can use your own data (with resolution 384x384)

python parallel_syncnet_tanh.py
Training the Wav2Lip models
You can either train the model without the additional visual quality disriminator (< 1 day of training) or use the discriminator (~2 days). For the former, run:

python parallel_wav2lip_margin.py


