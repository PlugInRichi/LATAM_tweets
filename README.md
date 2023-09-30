# Data Engineer Challenge

## Instalación 🚀
```bash
# From LATAM_tweets/build/
docker build -t latam_tweets .
```

## Ejecución
```bash
#From LATAM_tweets
docker run -d -p 8888:8888 latam_tweets -v .:/opt/project \ 
    jupyter notebook --ip 0.0.0.0  --no-browser --allow-root --NotebookApp.token='' --NotebookApp.password='' 
```

http://127.0.0.1:8888/tree