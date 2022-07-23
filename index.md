<link rel="stylesheet" href="/dist/custom_captcha.min.css" />
<script src="/dist/custom_captcha.min.js"></script>

# Custom Captcha

Extending Google reCaptcha v3 with a custom checkbox.

This script creates a custom "skin" for the Google reCaptcha, using the v3 invisible captcha.

You can make your own branded reCaptcha to make a unique experience.

## **⚠️ Warning**

### This captcha is using reCaptcha v3 which is based on scoring instead of a real challenge.

## Usage:

### Add this to the \<head>:

```html
<link rel="stylesheet" href="https://custom-captcha.js.org/dist/custom_captcha.min.css"></link>
<script src="https://custom-captcha.js.org/dist/custom_captcha.min.js"></script>
```

### Add this to your form(s):

```html
<captcha required></captcha>
```

### And finally initialize the widget:

```js
CustomCaptcha.init("<your reCaptcha v3 siteKey>");
```

### Configuration:

| parameter    |              description                 |   values                   |       default        
|--------------|------------------------------------------|----------------------------|----------------------
| name         | the name used in the form                | \<string>                  | g-recaptcha-response 
| text         | the text displayed in the bottom right   | \<string>                  | reCAPTCHA            
| lang         | language of the "I'm not a robot"        | en, hu, de, sk, ro, hr, fr | browser default      
| label        | Custom text instead of "I'm not a robot" | \<string>                  | "I'm not a robot"    
| theme        | the color scheme of the widget           | light, dark | light        |                      
| required     | makes the field required (recommended)   |                            |                      
| logo-rounded | makes the logo rounded                   |                            |                      

### Default configuration on initialization:

```html
<captcha required></captcha>
<captcha theme="light" required></captcha>
```

```js
CustomCaptcha.init({
    siteKey: "<your reCaptcha v3 siteKey>",
    text: "Example",
    logo: "https://twemoji.maxcdn.com/v/13.1.0/svg/1f916.svg",
    theme: "dark"
});
```

<captcha text="Example" logo="https://twemoji.maxcdn.com/v/13.1.0/svg/1f916.svg" theme="dark" required></captcha>
<captcha text="Example" logo="https://twemoji.maxcdn.com/v/13.1.0/svg/1f916.svg" theme="light" required></captcha>

### Configuration on the element:

```html
<captcha required></captcha>
<captcha theme="dark" required></captcha>
<captcha text="Example" required></captcha>
<captcha text="Example" theme="dark" required></captcha>
<captcha label="Click here for a delicious 🍔" logo="https://twemoji.maxcdn.com/v/14.0.2/72x72/303d.png" text="I'm eatin' it" required></captcha>
```

<captcha required></captcha>
<captcha theme="dark" required></captcha>
<captcha text="Example" required></captcha>
<captcha text="Example" theme="dark" required></captcha>
<captcha label="Click here for a delicious 🍔" logo="https://twemoji.maxcdn.com/v/14.0.2/72x72/303d.png" text="I'm eatin' it" required></captcha>
## Placeholder:

### Until you initialize the widget you can show a placeholder text

```html
<captcha required>Please wait while the Captcha is loading...</captcha>
```

## How to get siteKey?

- Go to the [Google reCaptcha admin](https://www.google.com/recaptcha/admin/create) page
- Choose **reCaptcha v3**
- Add your domain(s) under **Domains**
- Click on **Submit**
- Copy the **site key** and use it in **init**

## **⚠️ Please note**

### You need to process captcha score in your backend

<script>
    CustomCaptcha.init("6LdYwRUhAAAAAOPnPnui3qMlO3EGcBLsGduU6W55");
</script>
