    yum install wget unzip -y

    wget https://github.com/letran3691/ELK_Active/releases/download/8.16.0/active-elasticsearch-by-docker-8.16.0.zip
    unzip active-elasticsearch-by-docker-8.16.0.zip
    cd active-elasticsearch-by-docker-8.16.0

    version=8.16.0
    bash crack.sh $version
    cp output/x-pack-core-$version.crack.jar x-pack-core-$version.jar
    cp -f x-pack-core-$version.jar  /usr/share/elasticsearch/modules/x-pack-core/

    systemctl restart elasticsearch.service

- các bước còn lại làm tương tự trong file README.md