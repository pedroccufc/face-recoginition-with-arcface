# Face recognition with ArcFace

Código para https://www.learnopencv.com/face-recognition-with-arcface/ postagem do blog que ilustra os conceitos de reconhecimento facial.

## Código fonte original

Algumas partes do código e do modelo de identificação de rosto treinado são do repositório [face.evoLVe] (https://github.com/ZhaoJ9014/face.evoLVe.PyTorch) que é lançado sob a [Licença MIT] (https://github.com/ZhaoJ9014/face.evoLVe.PyTorch/blob/master/LICENÇA). Muito obrigado a eles!

## Código adaptado original

O presente repositório é uma cópia do projeto https://github.com/spmallick/learnopencv/tree/master/Face-Recognition-with-ArcFace. Meu muito obrigado ao criador dessa versão adaptada! O presente tutorial também foi criado pelo mesmo, mas que funciona perfeitamente para este projeto, por isso estou usando.

O objetivo deste repositório é apenas facilitar o uso dessa ferramenta, todos os créditos de criação são destinados a [vikasgupta] (https://github.com/spmallick/learnopencv/commits?author=vikasgupta-github)

## Instalação

Faça o clone do repositório.

```
git clone https://github.com/pedroccufc/face-recoginition-with-arcface.git
```

Entre no diretório.

```
cd face-recognition-with-arcface
```

Use seu ambiente virtual Python, como [virtualenv] (https://virtualenv.pypa.io/en/latest/) para isolar o projeto.

```
virtualenv -p python3.7 face-recognition
source face-recognition/bin/activate
```

Em seguida, instale todas as dependências.

```
pip install -r requirements.txt
```

_Observação: a GPU não é necessária para executar este código, mas a inferência do modelo será mais rápida se você tiver um._

## Modelo
Baixe o ponto de verificação para um modelo de [GoogleDrive] (https://drive.google.com/drive/folders/1omzvXV_djVIW2A7I09DWMe9JR-9o_MYh) / [Baidu] (https://pan.baidu.com/s/1L8yOF1oZf6JHfeY9iN59Mg =% 2Fms1m-ir50) e mova-o para `checkpoint/backbone_ir50_ms1m_epoch120.pth`
## Data

Todos os conjuntos de dados com faces devem suportar o formato [ImageFolder] (https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder). Veja os exemplos preparados no diretório `data`.

Para todos os comandos subsequentes, use o argumento `tags` para selecionar conjuntos de dados específicos no diretório `data`.

## Pré-processamento de dados
Para preparar dados com faces cortadas e alinhadas de suas imagens originais, execute:

```
python face_alignment.py --tags actors actresses musk woman --crop_size 112
```

_Observação: o argumento crop_size deve ser 112 ou 224._

## Visualização de similaridade

Para visualizar a semelhança entre as faces no formato de tabela, execute:

```
python similarity.py --tags actors actresses musk woman
```

O resultado de cada conjunto de dados será salvo no diretório `images`.

## visualização t-SNE

Para usar t-SNE para redução de dimensionalidade e visualização 2D de embeddings de face, execute:

```
python tsne.py --tags actors actresses musk woman
```

Os resultados serão plotados em uma janela separada. Você pode ampliar a imagem para ver os detalhes.


# Cursos de IA por OpenCV

Quer se tornar um especialista em IA? [AI Courses by OpenCV] (https://opencv.org/courses/) é um ótimo lugar para começar.

<a href="https://opencv.org/courses/">
<p align="center">
<img src="https://www.learnopencv.com/wp-content/uploads/2020/04/AI-Courses-By-OpenCV-Github.png">
</p>
</a>
