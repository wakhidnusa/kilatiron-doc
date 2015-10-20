# ElephantSQL: PostgreSQL as a Service

The most advanced open-source database, hosted in the cloud.

As a full-featured, open-source relational DBMS (RDBMS), PostgreSQL boasts many characteristics designed to support high-transaction, mission-critical applications.

## Adding the ElephantSQL Add-on

To add the ElephantSQL Add-on use the addon.add command.

~~~
$ ironapp APP_NAME/DEP_NAME addon.add elephantsql.OPTION
~~~
Replace `elephantsql.OPTION` with a valid option, e.g. `elephantsql.turtle`.

When added, ElephantSQL automatically creates a new user account with your email adress. You can manage the Add-on within the [web console](https://www.cloudcontrol.com/console) (go to the specific deployment and click the link "elephantsql.OPTION").

## Upgrading the ElephantSQL Add-on

To upgrade from a smaller to a more powerful plan use the addon.upgrade command.

~~~
$ ironapp APP_NAME/DEP_NAME addon.upgrade elephantsql.OPTION_OLD elephantsql.OPTION_NEW
~~~

Please note: Upgrading works only between shared plans or between dedicated
plans. To upgrade from a shared to a dedicated plan, you would need to export
your data from the shared plan first and reimport it to the dedicated plan
later.

## Downgrading the ElephantSQL Add-on

To downgrade to a smaller plan use the addon.downgrade command.

~~~
$ ironapp APP_NAME/DEP_NAME addon.downgrade elephantsql.OPTION_OLD elephantsql.OPTION_NEW
~~~

## Removing the ElephantSQL Add-on

The ElephantSQL Add-on can be removed from the deployment by using the addon.remove command.

~~~
$ ironapp APP_NAME/DEP_NAME addon.remove elephantsql.OPTION
~~~

### Internal Access

It's recommended to the read database credentials from the creds.json file. The location of the file is available in the `CRED_FILE` environment variable. Reading the credentials from the creds.json file ensures your app is always using the correct credentials. For detailed instructions on how to use the creds.json file please refer to the section about [Add-on Credentials](https://www.cloudcontrol.com/dev-center/platform-documentation#add-ons) in the general documentation.

You can also find a ready-to-deploy example application on [Github](https://github.com/ElephantSQL/ruby-postgresql-example.git).