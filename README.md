### TODO:
- Read and understand nginx config
- Read and understand travis config
- Read and understand docker-compose file


#### AWS Elastic Beanstalk Multiplecontainer Docker
 - To deploy multiple container running on one EC2 instance using Elastic Beanstalk, we need a `Dockerrun.aws.json` configuration file, which is specific to Elastic Beanstalk.
 - When writting the configuration file, note that we have to specify `AWSEBDockerrunVersion=2`, because version 2 is to handle multiple container. The format differs significantly from the previous version 1.
 - Further reading: https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_docker_ecs.html

### Architecture:
<img src="misc/Architecture.jpg" width="700">