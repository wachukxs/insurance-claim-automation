## What kind of insurance claim is this focused on?
Motor insurance products - _mostly car insurance_.

## How it works
I'm following the steps outlined [here](https://mtek-services.com/knowledge-base/how-to-make-a-motor-vehicle-accident-or-damage-claim/). Since media isn't adequately supported for SMS & USSD, they'll only accept text inputs. For illustrative purposes, I've seeded the database with 5 dummy/test users (Their details are in ).
When you contact our service, you'll need to provide a membership id. Ideally this step isn't necessary cause we'd _maybe_ have the registered phone numbers of our users/customers. Got list of motor insurance products [here](https://www.cholainsurance.com/knowledge-center/car-insurance/the-different-types-of-motor-insurance)

## Our Telegram bot?
Find it here [@claim_motor_insurance_bot](http://t.me/claim_motor_insurance_bot)

## Africa's Talking Simulator (for SMS, and USSD)
To test out: visit [Africa's Talking Simulator](https://simulator.africastalking.com:1517/)  
USSD Dial Code: \*384\*25447#  
SMS: 25446  
> Important Note! It seems Africa's Talking Simulator is down for Kenyan numbers (last time I check with was 30th Jan. 2023 - I emailed them about it and they're on it). Test with a different country number. I can show a demo if you need.

## Our API & Frontend
* API: [incourage-insurer](https://incourage-insurer.herokuapp.com/)  
* Frontend: [see-insurance-claims](https://see-insurance-claims.netlify.app/). It's still in progress :)  
    * GitHub repo for the [frontend app](https://github.com/wachukxs/see-insure-claims)


## Deployment
* I'm using Heroku GitHub integration and CI/CD to auto deploy the main branch for our API
* I'm using Netlify to do the same for our frontend application.

## Resources
* Should I use both Africa'sTalking, and Twillo?
* Using [LocalTunnel](https://localtunnel.github.io/www/), not ngrok :)


## Set heroku configs
```heroku config:set CONFIG_VAR_NAME=var_value -a appName```  
```heroku logs --tail -a appName```  
```heroku logs -n 1500 -a appName```   

## From dev/local env to the world
```lt --port <PORT>```

## Delibrations
* Should we have an interface that'll help insurance agents see the claims that have been made?
    * Yes! Improvements.
* Should we include data validation?
    * Yes!, especially for user inputs!
* Do we need API documentation?
    * Yes, just enough at least.
* Users should be able to track the progress of their raised claims
    * Nice to have if there's time, it wasn't asked.