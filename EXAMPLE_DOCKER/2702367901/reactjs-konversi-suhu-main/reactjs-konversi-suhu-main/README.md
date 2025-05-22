# reactjs-konversi-suhu

### catatan:
1. ganti nama file <code>.env.example</code> menjadi <code>.env</code> saja (tanpa .example)
2. link video tutorial docker untuk template project ini: <code>https://youtu.be/C0ZXEvdZGME</code>


### - nizam (2702367901)

tutorial hanya single stage;

untuk 2 stage 

build image "docker build -t konversi-suhu:latest ."
run countainer "docker run -p 8080:80 konversi-suhu:latest"
access "http://localhost:8080"