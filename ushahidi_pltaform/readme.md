# The Ushahidi platform

[Ushahidi](https://www.ushahidi.com/) is an opensource humanitarian platform which is centred round a map. 
The main components of the platform are:
- The ability to collat/aggregatee and map data sources
- A built in task manager which supports different types of user permissions to manage the content on the platform 
- Integration with the United Nations Humanitarian Data platform [HDX](https://data.humdata.org/)

The code can be forked from their repo or you can use their hosted deployment with customisation. Other covid response projects are already running on the platform.

From the offical intro:

> Ushahidi, which translates to “testimony” in Swahili, was developed to map reports of violence in Kenya after the post-election violence in 2008. Since then, thousands have used our crowdsourcing tools to raise their voice. We’re a technology leader in Africa, headquartered in Nairobi, with a global team. We are a social enterprise that provides software and services to numerous sectors and civil society to help improve the bottom up flow of information.

# Open distribution ushahidi platform deployment 
A version of Ushahidi specific to UK Covid response has been deployed using the hosted option on free tier. This is running as https://frontlinehelp.ushahidi.io/.

## Configuration of the plaftform todate (please update this if changes are made)

You'll need to be logged in to adjust the config. 

Data soruces:
The platform can ingest data from web forms, SMS, Twitter, Email or webhooks to other applications. Current config:
- Email is linked to a holding gmail account but not displaying (TO FIX), we aren't currently using email, follow [link](https://frontlinehelp.ushahidi.io/settings/datasources) for config page
- Twitter Is scraping from a specific hastag , follow [link](https://frontlinehelp.ushahidi.io/settings/datasources) for config page 
- Webforms- There are currently webforms for PPE Request, PPE Supplier. Follow [link](https://frontlinehelp.ushahidi.io/settings/surveys)


# Suggested volunteer workflow 

# Integration with Frontline.it home page 
