export GH_USERNAME='kickoffqi'
export GH_TOCKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'
export TAG_NAME='ghcr.io/$GH_USERNAME/$GH_IMAGE_NAME:$GH_VER'


echo $GH_TOCKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest $TAG_NAME

docker push $TAG_NAME

add one more thing!
