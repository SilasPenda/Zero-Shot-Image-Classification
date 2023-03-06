# Zero-Shot-Image-Classification

Clone this repo

cd into cloned repo

Create a Virtual environment.

```
pip install virtualenv
python -m venv zero-shot
```

Activate Virtual environment

```
 zero-shot/source/activate
```

Install requirements

```
pip install -r openvino_requirements.txt
```

Inference using Native Pytorch (GPU)

```
python3 detect.py --weights best.pt --conf 0.25 --source clip39.m4v
```

Inference using Native Pytorch (CPU)

```
python3 detect_without_jit.py --weights best.pt --conf 0.25 --source clip39.m4v
```

Inference using Torch-ort-infer (CPU) \
NB: Linux machine only (Can use Colab) \

Access ORTModule

```
python3 -m onnxruntime.training.ortmodule.torch_cpp_extensions.install
```
Run Inference
```
python3 detect_ort.py --weights best.pt --conf 0.25 --source clip39.m4v
```
