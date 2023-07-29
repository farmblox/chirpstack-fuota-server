# Farmblox Docker Builds

Since this is a lesser used project, Brocaar hasn't regularly been creating new releases for it, even after pushing new changes.
If we want the latest changes, we have to build new docker images ourselves.

### Instructions

First, pull the latest changes from master. Then, run the following command to build the docker image from source:
- `docker build --platform=linux/amd64 -t farmblox/chirpstack-fuota-server:[NEW_TAG] .`

Replace `NEW_TAG` with a meaningful tag name. Since Brocaar hasn't been tagging commits or creating releases, we should use something else that can be used to identify the commit used for the build, the date the image was built, like `2023.07.29`, for example.

Finally, push the new image to dockerhub:
- `docker push farmblox/chirpstack-fuota-server:[NEW_TAG]`
