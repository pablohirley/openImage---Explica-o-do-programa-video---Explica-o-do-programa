# Aqui importamos a biblioteca do open cv
import cv2

# Abre a imagem, mas tbm podemos considerar que e carregado na memoria
img = cv2.imread('colorido.png',cv2.IMREAD_GRAYSCALE)

# Imprime a imagem em uma janela
cv2.imshow('image',img)

# espera apertarmos qualquer tecla para fechar a imagem, caso aperte o x da janela o programa ira ficar e assim executando para sempre
cv2.waitKey(0)

# Fecha todas as janelar abertas pelo open cv
cv2.destroyAllWindows()j