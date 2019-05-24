## How to install MAD in a Google Cloud instance

### Google Cloud Platform

After accessing Google Cloud Platform with our Google account, we are going to need a Compute Engine instance and a SQL database. You can pin them to show first when you open the left menu. 

#### Computer Engine instance 

You need to create a new instance. Name it whatever descriptive (e.g.: PoGo instance) and use this data:
* Region: `us-east1` (you will be elegible for free tier if it's in this region)
* Zone: whatever
* Machine: `micro`
* Boot disk: `Ubuntu 18.4 LTS`
Make default for APIs.
* Allow HTTP & HTTPS traffic

Once created you will have a ssh connection and you can work with it. 

Now, access via SSH `Connect -> SSH`. We are going to set up the environment.

These are the steps that you need to reproduce in a fresh install of Ubuntu 18.04 LTS:

1. Update your freshly installed server with `sudo apt-get update` and `sudo apt-get upgrade`
2. Now we install pip, required to our installations with `sudo apt-get install python3-pip`
3. Next is apache server. `sudo apt-get install apache2`

If everything is OK, you should be able to see your server in your external IP after typing `sudo systemctl status apache2`. Beware clicking your external IP in the Google Cloud instance! It adds `https` and by now we only have `http` active, so take this into account to test your page. 

Notes for later: 
* [Geofence](http://geo.jasparke.net/)
* [PokéAlarm Docs](https://buildmedia.readthedocs.org/media/pdf/pa/latest/pa.pdf)
