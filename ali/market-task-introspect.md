# The introspection regarding the task 运营市场一期



## check list creating a new module in a project

*  shared
   - create packages: *model* *service*
   - create models and service interface

*  center
   - implement service defined in shared
   - new packages dataobject daointerface ibatis
   - **create several ibatis config and spring bean definitions resources for unit testing**
   - **create sql xml in the sqlmap fold under resources**
   - **add dao implementations to biz-dao.xml under industrycenter.config module**
   - **append the new sql files in dal to sqmMap.xml under config module**
   - **create and add beans to service config file(eg. market-service.xml) under auto-config of config module**
   - **append the new service config file to auto-config.xml under autoconf and import to applicationContext.xml under ic.deploy**
   - **add dubbo provider config file and append to biz-dubbo-provider-read(or write).xml**
   - **put the new dubbo provider config file to auto-config.xml under industrycenter.deploy**


*  web
   - **create bean definition xml like biz-market.xml under common module**
   - create new modules for biz and web like industryweb.biz.market and industryweb.web.market
   - put the new modules to project pom.xml
   - create templates under deploy module
   - **add dubbo references in the dubbo-service.xml under common module**
   - **add webx compoment config file like webx-market.xml and form.xml**
   - **add the new module to the pom file for bundle module**
   - add biz service implementation to biz-market.xml under common module
   - add the new module to pom.xml for common module

