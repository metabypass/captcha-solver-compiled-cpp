# MetaBypass ( AI Captcha Solver )
## C++ wrapper to work with [MetaBypass](https://metabypass.tech) services
### This is C++ compiled version. to use C++ pure version check [this repo](https://github.com/metabypass/captcha-solver-cpp) 

Free demo (no credit card required) -> https://app.metabypass.tech/application

<br/>

### Features

Solve image captcha , reCaptcha v2 & v3 , invisible reCaptcha <br/>
Auto handler for reCaptcha v2 <br/>
Use easily with the shell everywhere

<br/>
<br/>

## Notice
to request we used the curl library in codes. so make sure that the curl library has been installed on your machine. <br/>


<br/>
<br/>


## Usage

<br/>

first , you need to credentials<br>
1. Go to [Application Section](https://app.metabypass.tech/application)
2. You can see credentials like below image


![Screenshot 2023-05-21 120957](https://github.com/metabypass/metabypass-python/assets/128980891/4420f7ed-1588-412a-b0e8-2876d4ae1854)

and click on "Copy Json" button to copy your credentials easily. then store your credentials in json file. your json file should be like this:

```json
{
  "grant_type": "password",
  "client_id": "YOUR_CLIENT_ID",
  "client_secret": "YOUR_CLIENT_SECRET",
  "client_name": "not important.can be empty",
  "username": "YOUR_EMAIL",
  "password": "YOUR_PASSWORD"
}

```
now you can use compiled files. see exampls: <br><br><br>

## Examples

<br>

**imageCaptcha** <br/>
--img-path : image captcha file path <br>
--credentials-path: your credentails.json file path <br>

```shell

./image_captcha --img-path "samples/icaptcha1.jpg" --credentials-path "credentials.json"

```
<br>
<br>

**reCAPTCHA v2** <br/>
--credentials-path: your credentails.json file path


```shell

./recaptcha_v2 --site-url "SITE_URL" --site-key "SITE_KEY" --credentials-path "credentials.json"

```

<br>
<br>

**reCAPTCHA v3** <br/>
--credentials-path: your credentails.json file path


```shell

./recaptcha_v3 --site-url "SITE_URL" --site-key "SITE_KEY" --credentials-path "credentials.json"

```

<br>
<br>

**reCAPTCHA invisible** <br/>
--credentials-path: your credentails.json file path


```shell

./recaptcha_invisible --site-url "SITE_URL" --site-key "SITE_KEY" --credentials-path "credentials.json"

```