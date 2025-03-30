# Technologii-internetowych
Technologii internetowych - repozytorium na potrzeby zaliczenia przedmiotu


## Przygotowanie środowiska do Large langurage models

### IDE
Jupyter Notebooks 
- Google Collab

Colab, lub inaczej „Colaboratory”, pozwala pisać i wykonywać kod w języku Python bezpośrednio w przeglądarce dzięki

brakowi konieczności konfigurowania,
Bezpłatny dostęp do GPU
łatwemu udostępnianiu.
Colab może Ci ułatwić pracę niezależnie od tego, czy jesteś studentem, badaczem danych czy badaczem sztucznej inteligencji. Obejrzyj Wprowadzenie do Colab, by dowiedzieć się więcej, lub po prostu zjedź niżej i zacznij korzystać z tej usługi.
https://colab.research.google.com/

- Local installation of Jupyter Lab/Notebooks

Jupyter Notebook to interaktywne środowisko pracy, działające w przeglądarce internetowej, które umożliwia przeprowadzanie obliczeń naukowych. Jest to sztandarowy produkt o otwartym kodzie źródłowym Projektu Jupyter, powszechnie wykorzystywany w dziedzinie nauki o danych.


Wymagane : 
- python 3.12
https://www.python.org/downloads/
- scikit-learn
https://scikit-learn.org/stable/index.html
- nltk
https://www.nltk.org/index.html

```
# instalacja jupyter lab 
pip install jupyterlab

#instalacja git extension
pip install jupyterlab-git

#Natural Language Toolkit dla python
pip install nltk

#Simple and efficient tools for predictive data analysis
pip install scikit-learn
```

### Azure ML
Azure Machine Learning to usługa w chmurze służąca do przyspieszania cyklu życia projektu uczenia maszynowego(ML) i zarządzania nim. 
Specjaliści ds. uczenia maszynowego, analitycy danych i inżynierowie mogą używać ich w codziennych przepływach pracy do trenowania i wdrażania modeli oraz zarządzania operacjami uczenia maszynowego (MLOps).
Model można utworzyć w usłudze Machine Learning lub użyć modelu utworzonego na podstawie platformy typu open source, takiej jak PyTorch, TensorFlow lub scikit-learn.
Narzędzia MLOps ułatwiają monitorowanie, ponowne trenowanie i ponowne wdrażanie modeli.

Stworzenie maszyny dla JupyterLab

<img src=https://github.com/Behton/Technologii-internetowych/blob/main/img/img.png>

Integracja git z maszyna compute vm w Azure.
```
git clone git@github.com:Behton/Technologii-internetowych.git
git config --global --add safe.directory /mnt/batch/tasks/shared/LS_root/mounts/clusters/light-vm/code/Users/Technologii-internetowych
git config --global user.email ""  
git config --global user.name ""
```

Tworzenie autentykacji poprzez klucz ssh na vm w Azure
```
(azureml_py38) azureuser@light-vm:/mnt/batch/tasks/shared/LS_root/mounts/clusters/light-vm/code$ cd ~
(azureml_py38) azureuser@light-vm:~$ cd .ssh/
(azureml_py38) azureuser@light-vm:~/.ssh$ ls
authorized_keys  config  github  github.pub  known_hosts
(azureml_py38) azureuser@light-vm:~/.ssh$ cat config 
HostName github.com 
        IdentityFile ~/.ssh/github
(azureml_py38) azureuser@light-vm:~/.ssh$ 
```




