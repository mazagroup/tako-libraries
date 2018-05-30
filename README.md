# Tako Libraries

## Dependencies

## Build
### ~/.gradlerc Contents @AWS s3 MazaGroup
export BITBUCKET_TAG=r1
export AWS_ACCESS_KEY_ID=AKIAJNYLBP65XTXMCMEQ
export AWS_SECRET_ACCESS_KEY=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

## source ~/.gradlerc
./gradlew s3ReleaseDeploy

## To build
./gradlew clean release
./gradlew s3ReleaseDeploy

# Conf bucket for public access: add ACL policy
{
   "Version":"2012-10-17",
   "Statement":[{
 	"Sid":"PublicReadForGetBucketObjects",
         "Effect":"Allow",
 	  "Principal": "*",
       "Action":["s3:GetObject"],
       "Resource":["arn:aws:s3:::tako-deps/*"
       ]
     }
   ]
 }

# Accessing Repo Index
http://tako-repo.s3-website-us-east-1.amazonaws.com/tako-deps/r1/repo/index.xml.gz
