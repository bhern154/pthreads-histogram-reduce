# Problema do histograma com pthreads

Compilando usando `make`:

```shell
$ CFLAGS=-pthread make split-bins
cc -pthread    split-bins.c   -o split-bins
```

Ao executar o programa, deve-se inserir os valores de:

* Valores reais mínimos e máximos `<a>` e `<b>` do intervalo
* Valor inteiro da quantidade de números `<data_count>`
* Valor inteiro da quantidade de *bins* `<bin_count>`

Por exemplo, rodando o programa `split-bins` gerado:

```shell
$ ./split-bins
Type in the values for: <a> <b> <data_count> <bin_count>: 3 9 500 10
sequence range: [3.00, 9.00]
sequence length: 500
number of bins: 10
interval: 0.60
[3.00, 3.60) |################################### 55
[3.60, 4.20) |################################# 52
[4.20, 4.80) |######################### 40
[4.80, 5.40) |######################################## 62
[5.40, 6.00) |####################### 36
[6.00, 6.60) |################################## 54
[6.60, 7.20) |############################### 49
[7.20, 7.80) |############################# 46
[7.80, 8.40) |################################## 53
[8.40, 9.00) |################################## 53
```

