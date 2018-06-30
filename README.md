# ExchangeMoney
Configuring the AWS SDK for .NET with .NET Core

https://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/net-dg-config-netcore.html

https://github.com/aws/aws-sdk-net

 

                AWS S3 Using Pre-Signed URLs

https://docs.aws.amazon.com/AmazonS3/latest/dev/PresignedUrlUploadObject.html

 

                Example .Net Code

https://docs.aws.amazon.com/AmazonS3/latest/dev/ShareObjectPreSignedURLDotNetSDK.html

https://www.example-code.com/dotnet-core/aws_pre_signed_url_v4.asp

 

For S3 Security, I would like to recommend using  Gateway VPC Endpoints, S3 ACL and bucket policies     

                                https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpce-gateway.html

                                https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html

                                https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies-vpc-endpoint.html

 

                Example S3 bucket policy to restricting Access to S3 via  specific VPC Endpoint and Source IP   (For private/confidential data)

{

  "Id": "Policy1526291261064",

  "Version": "2012-10-17",

  "Statement": [

    {

      "Sid": "Stmt1526291248434",

      "Action": "s3:*",

      "Effect": "Deny",

      "Resource": ["arn:aws:s3:::s3-bucket-name",

                   "arn:aws:s3:::s3-bucket-name/*"],

      "Condition": {

        "StringNotEquals": {

          "aws:SourceVpce": "vpce-id"

        },

        "NotIpAddress": {

          "aws:SourceIp": "X.X.X.X/32"

        }

      },

      "Principal": "*"

    }

  ]

}

---------------



USE umayplusmanage_db;

insert into `authen_menu`(`menuID`,`menuDescription`,`departmentID`,`createBy`,`createDateTime`,`updateBy`,`updateDateTime`) values ('100','CS-Report','12,33,34,35','IT','2018-06-28 14:45:04','IT','2018-06-28 14:47:01');
insert into `authen_menu`(`menuID`,`menuDescription`,`departmentID`,`createBy`,`createDateTime`,`updateBy`,`updateDateTime`) values ('200','BP-UploadPromotion','81,33,34,35','IT','2018-06-28 14:48:51','IT','2018-06-28 14:48:55');
insert into `authen_menu`(`menuID`,`menuDescription`,`departmentID`,`createBy`,`createDateTime`,`updateBy`,`updateDateTime`) values ('201','BP-UploadBranch','81,33,34,35','IT','2018-06-28 14:49:17','IT','2018-06-28 14:49:20');
