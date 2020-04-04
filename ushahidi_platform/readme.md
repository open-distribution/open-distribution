# The Ushahidi platform

[Ushahidi](https://www.ushahidi.com/) is an opensource humanitarian platform which is centred round a map. 
The main components of the platform are:
- The ability to collate/aggregatee and map data sources
- A built in task manager which supports different types of user permissions to manage the content on the platform 
- Integration with the United Nations Humanitarian Data platform [HDX](https://data.humdata.org/)

The code can be forked from their [repo](https://github.com/ushahidi) or you can use their hosted deployment with customisation. Other covid response projects are already running on the platform.

From the offical intro:

> Ushahidi, which translates to “testimony” in Swahili, was developed to map reports of violence in Kenya after the post-election violence in 2008. Since then, thousands have used our crowdsourcing tools to raise their voice. We’re a technology leader in Africa, headquartered in Nairobi, with a global team. We are a social enterprise that provides software and services to numerous sectors and civil society to help improve the bottom up flow of information.

# Open distribution on Ushahidi platform 

Deployment notes

A version of Ushahidi specific to UK Covid response has been deployed using the hosted option on free tier. This is running as https://frontlinehelp.ushahidi.io/.

## Configuration of the plaftform todate (please update this if changes are made)

You'll need to be logged in to adjust the config. 

Data soruces:
The platform can ingest data from web forms, SMS, Twitter, Email or webhooks to other applications. Current config:
- Email is linked to a holding gmail account but not displaying (TO FIX), we aren't currently using email, follow [link](https://frontlinehelp.ushahidi.io/settings/datasources) for config page
- Twitter Is scraping from a specific hastag , follow [link](https://frontlinehelp.ushahidi.io/settings/datasources) for config page 
- Webforms- There are currently webforms for PPE Request, PPE Supplier. Follow [link](https://frontlinehelp.ushahidi.io/settings/surveys)

Webform workflows
Before a incoming datasource is displayed onto the map there is a task system that requires it to be assigned to a volunteer name. Without assignment the datasource will not be displayed. This is to enable verfication of the data as the suggested workflow below. Additional tasks can be added to incoming data sources by editting the [survey](https://frontlinehelp.ushahidi.io/settings/surveys)

# Suggested volunteer workflow 
This is a first draft of managing the data coming in from any source, needs testing.

1. Create volunteer role (done)
2. Creat login for each volunteer for the platform through this [link](https://frontlinehelp.ushahidi.io/settings/users) using the big yellow plus button. Needs doing. 
3. Assign them as volunteer
4. Volunteers can now triage incoming data, the feed for this is [here](https://frontlinehelp.ushahidi.io/views/data) 
5. Volunteer sees data post, clicks the three dot (top right) button. This allows them to: 
   - Edit if satisifed it's a genuine and valid request - Ie. Use this to add location from postcode in tweet and copy image from tweet to the web form. If not then next option is:
   - Put under review - Discuss with volunteer coordinator
   - Publish button: This puts the post on the map
   - Archive: Once a request is met then use this to remove from the map
   - Delete: Only use this for datasources which aren't genuine or actionable

# Open data
The data coming into the platform can be manually pushed to HDX. We've had a conversation with thei data manager to understand the steps required to set this up.

# Integration with Frontline.it home page 
The front end picks up one of the API end points and uses the data in json to plot pins onto the map. Documentation for API is found [here](http://preview.ushahidi.com/platform/develop/api/index.html#posts)
