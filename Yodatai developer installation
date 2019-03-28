1. Install Bot Framework and Bot Framework Emulator
2. Install Redis for Windows, setup it to run as service on the default port
3. Install AWS Dynamo DB
4. Run local Dynamo database, an example of run.cmd:
    @echo off
    start java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
5. Build solution
6. Add separate domain in IIS, bind it to URL bot.org. Add it to hosts.
7. Setup Bot Framework Emulator
   a. Add endpoint http://bot.org/api/bot
   b. Use appId, appPassword from setting microsoftApp in web.config.
8. For portal bots:
   a. Add URL in IIS and hosts: kapsarc.bot.org
   b. In emulator add endpoint http://bot.org/api/bot/kapsarc, use respective appId, appPassword.
9. To enable Twitter checker command you need to enable auto-loading of application
   a. Open C:\WINDOWS\system32\inetsrv\config\applicationHost.config
   b. Change site config:
<application path="/" applicationPool="Bot.org" serviceAutoStartEnabled="true" serviceAutoStartProvider="PrewarmMyCache">
   c. In option <system.applicationHost> add
<serviceAutoStartProviders>
	<add name="PrewarmMyCache" type="Bot.Web.ApplicationPreload, Bot.Web" />
</serviceAutoStartProviders>

Useful endpoints:
http://bot.org/hangfire - Hangfire dashboard
http://bot.org/admin - Admin panel, works after you log-in on the home page.
