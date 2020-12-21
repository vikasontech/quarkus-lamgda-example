
------------------
aws side
------------------
1. create aws account
2. create a user with the required permissions
3. create a role with the lambda execution permission
4. get use access id and access token and configure it to the aws credentials

------------------
quarkus side
------------------
1. create a lambda project
2. mvn package
3. modify the target/manage.sh
	a. add labmda `LAMBDA_ROLE_ARN="arn:aws:iam::785335436437:role/my-lambda-ex"`
	b. if you have more then one profiles in the aws credential file then specifies the profiles using the command `--profile <name-of-profile>` with the `aws cli` commands.
	c. create function in lambda -
		`sh target/manage.sh create`
	d. invoke function in lambda -
		`sh target/manage.sh invoke`
	e. update function in lambda -
		`sh target/manage.sh update`
	f. delete function in lambda -
		`sh target/manage.sh delete`

