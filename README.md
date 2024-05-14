# Flask-Elastic-Beanstalk (Not Working)


Note, the best way to use this repo is to "fork it", delete the .elasticbeanstalk directory and replace it with yours generated by the `eb init`.  Also change the `buildspec.yml` file `eb deploy` to your app name.

![eb-deploy](https://user-images.githubusercontent.com/58792/106804626-a3a81900-6633-11eb-9cf6-54c24af6827f.png)



### Deploy via AWs Cloud9 + AWS Code Build

*You can refer to tutorial [here as well for Flask EB](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-flask.html)*

A.  check out this repo and cd into it

B.  create a python virtualenv and source it and run `make all`

`python3 -m venv ~/.eb`
`source ~/.eb/bin/activate`
`make all`

*Note, that awsebcli is installed via requirements*

C. initialize new eb app

`eb init -p python-3.7 flask-continuous-delivery --region us-east-1`

*Optional `eb init` again to create ssh keys*

D. Create remote eb instance

`eb create flask-continuous-delivery-env`

