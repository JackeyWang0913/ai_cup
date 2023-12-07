# 文本识别模型训练项目

## 项目介绍
这个项目是关于使用机器学习模型进行文本识别，专注于医疗文件文本的分类和整理。它使用了 EleutherAI 的 Pythia 模型（可选用 70m-deduped 或 160m-deduped 版本）进行训练，以实现高效的文本处理。

## 数据集
项目使用了两个数据集：
1. 训练集：`opendid_set1.tsv`
2. 验证集：`opendid_valid.tsv`

这些数据集包含了用于训练和验证模型的医疗文本数据。

## 安装指南
首先克隆仓库到本地环境：
```bash
git clone https://github.com/yourusername/yourprojectname.git
cd yourprojectname
```
然后安装所需的依赖：
```bash
pip install -r requirements.txt
```

## 使用说明
要训练模型，请运行：
```bash
python train_model.py --model EleutherAI/pythia-70m-deduped --batch_size <your_batch_size>
```
您可以选择不同的模型和批量大小。

如果您已经有了训练好的模型，可以使用 `loading model.ipynb` 来加载和应用模型。

## 输出
模型训练完成后，会生成一个 `answer.txt` 文件，包含模型对验证集的预测结果。


