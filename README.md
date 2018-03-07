# aws-static-site-s3-route53
Cloudformation to create a static site in s3 with route53



## Create Stack

    aws cloudformation deploy --template-file aws-static-site-s3-route53.yml --stack-name [name-stack] --parameter-overrides R53DomainName=[rc.example.pe] R53HostedZoneId=[Z11RD4WPH24] --capabilities CAPABILITY_IAM --region [ap-northeast-1]
    
## Delete Stack

    aws cloudformation delete-stack --stack-name [name-stack] --region [ap-northeast-1]

## Upload Static Files

    aws s3 cp index.html s3://[rc.example.pe]
