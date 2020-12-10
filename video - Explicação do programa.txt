# Aqui importamos a biblioteca do open cv
import cv2

# Abre o video que desejamos, mas tbm podemos considerar que e carregado na memoria
capture = cv2.VideoCapture('video.mp4')

# capture.isOpened() retorna True caso o video abra, e assim por consequencia fazemos um loop ate que o paremos
while(capture.isOpened()):
    # Aqui podemos observar que podemos obter o frame do video e se ele e um frame valido
    ret, frame = capture.read()
    # aqui mudamos a escala de cor do frame
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    print(gray)
    # Aqui imprimimos o frame que alteramos a escala
    cv2.imshow('frame', gray)

    # caso o usuario aperte q, o video ira fechar
    if cv2.waitKey(30) == ord('q'):
        break