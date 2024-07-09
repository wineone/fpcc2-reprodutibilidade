### Reprodutibilidade de artigo - FPCC 2

- Aluno: Matheus Lisboa Oliveira dos Santos
- Matrícula: 0123025804-7M

### Paper

Esse artigo descreve a utilização do modelo de linguagem T5 para a geração de questões. Foi utilizada a base de dados SQuAD para a avaliação. Para a reprodutibilidade utilizaremos os modelo T5 small, por limitações de hardware.

- https://aclanthology.org/D19-5821.pdf


### Código do autor
- https://github.com/patil-suraj/question_generation


### Observações

- Originalmente o autor utiliza o batch size de 32 para o treinamento, porém, por limites de memória de GPU, tivemos que diminuir o batch-size para 28.
- Experimento com a reprodutibilidade está localizado em ```reprodutibilidade.ipynb```
- O PDF com a descrição do trabalho está localizado em ```fpcc2_reprodutibilidade.pdf```


### Métricas reportadas pelo author vs métricas com a reprodutibilidade

Podemos ver que as métricas reportadas pelo autor são muito parecidas. A diferença pode se dar pela alteração no parâmetro de batch_size na etapa de treinamento
  
|         | Autor | Esse Experimento |
|---------|-------|------------------|
| BLEU-4  | 18.5  | 19.0             |
| METEOR  | 24.9  | 25.3             |
| ROUGE-L | 40.1  | 40.8             |

As métricas que obtivemos são superiores as reportadas pelo autor, o que indica que o artigo não sofre com problemas de reprodutibilidade.  