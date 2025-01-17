# ViLT

Code for the paper: "ViLT: Vision-and-Language Transformer Without Convolution or Region Supervision"

---
<p align="center">
  <img align="middle" src="./assets/figure.png" alt="The main figure"/>
</p>

## Install
```bash
pip install -r requirements.txt
pip install -e .
```

## Download Pretrained Weights
We provide five pretrained weights
1. ViLT-B/32 Pretrained with MLM+ITM for 200k steps on GCC+SBU+COCO+VG (ViLT-B/32 200k) [link](https://www.dropbox.com/s/5b3slhy5uvdw8k0/vilt_200k_mlm_itm.ckpt?dl=0)
2. ViLT-B/32 200k finetuned on VQAv2 [link](https://www.dropbox.com/s/fy8jkj71bxwqett/vilt_vqa.ckpt?dl=0)
3. ViLT-B/32 200k finetuned on NLVR2 [link](https://www.dropbox.com/s/vzzh4ag1jchk1wv/vilt_nlvr2.ckpt?dl=0)
4. ViLT-B/32 200k finetuned on COCO IR/TR [link](https://www.dropbox.com/s/dx3id644873fcgn/vilt_irtr_coco.ckpt?dl=0)
5. ViLT-B/32 200k finetuned on F30K IR/TR [link](https://www.dropbox.com/s/asidty0d4a1p2f4/vilt_irtr_f30k.ckpt?dl=0)

## Out-of-the-box MLM + Visualization Demo
```bash
pip install gradio==1.6.4
python demo.py with num_gpus=<0 if you have no gpus else 1> load_path="<YOUR_WEIGHT_ROOT>/vilt_200k_mlm_itm.ckpt"

ex)
python demo.py with num_gpus=0 load_path="weights/vilt_200k_mlm_itm.ckpt"
```

## Out-of-the-box VQA Demo
```bash
pip install gradio==1.6.4
python demo_vqa.py with num_gpus=<0 if you have no gpus else 1> load_path="<YOUR_WEIGHT_ROOT>/vilt_vqa.ckpt" test_only=True

ex)
python demo_vqa.py with num_gpus=0 load_path="weights/vilt_vqa.ckpt" test_only=True
```

## Dataset Preparation
See [`DATA.md`](DATA.md)

## Train New Models
See [`TRAIN.md`](TRAIN.md)

## Evaluation
See [`EVAL.md`](EVAL.md)

## Citation
If you use any part of this code and pretrained weights for your own purpose, please cite our [paper](https://arxiv.org/abs/2102.03334).
```
@article{kim2021vilt,
  title={ViLT: Vision-and-Language Transformer Without Convolution or Region Supervision},
  author={Kim, Wonjae and Son, Bokyung and Kim, Ildoo},
  journal={arXiv preprint arXiv:2102.03334},
  year={2021}
}
```

## Contact for Issues
- [Wonjae Kim](https://wonjae.kim/)
- [Bokyung Son](https://bo-son.github.io/)
- [Ildoo Kim](https://www.linkedin.com/in/ildoo-kim-56962034/)