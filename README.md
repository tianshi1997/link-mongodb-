# Link-MongoDB-Amazon-AWS
Instructions to link MongoDB to colud9 on Amazon AWS

I suffered a lot from this yesterday, now I will give the instrcutions. Hope you will find it helpful!

# I suppose that you already got an available account on Amazon AWS.

1.You must decide whether your AWS platfrom is Amazon Linux or not. If not, you could find the solution to link MongoDB via
https://www.youtube.com/watch?v=rtZZvti8beU&list=RDCMUCqo2YWBtmFSWhuUk4WEyfGg&index=24

2.If your AWS platform is Amazon Linux. Create a repo on your environemnt
code: //
[mongodb-org-4.2]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/amazon/2/mongodb-org/4.2/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc
//

3.Install the MongoDB packages
code: //sudo yum install -y mongodb-org//

4.Start MongoDB
code: //sudo service mongod start//

You could use MongoDB on Amazon AWS now!
For more details, you could visit https://docs.mongodb.com/manual/tutorial/install-mongodb-on-amazon/

P.S. To install Mongoose package you should add codes as follows:
code: //
var mongoose=require('mongoose');
mongoose.set('useNewUrlParser', true);
mongoose.set('useFindAndModify', false);
mongoose.set('useCreateIndex', true);
mongoose.set('useUnifiedTopology', true);
//

Hope you could find it helpful!
