c言語のコンパイラを作ってみる


参考資料は以下のリンク

https://www.sigbus.info/compilerbook


## 動かし方

前提としてdockerが入っていること。
linux環境ならdockerなしでも動くかも

cd c_lang_make
docker build -t my-cc ./

docker run -dit --rm --name my-cc-run -v $(pwd)/src:/home/src my-cc
docker exec -it my-cc-run bash

-- 以後docker内での作業 --

cd /home/src/cc
make test 
