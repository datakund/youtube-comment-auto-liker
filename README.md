## Youtube-Comment-Auto_Liker
A python library that uses browser automation to login to youtube and like youtube videos automatically
It uses [datakund](https://pypi.org/project/datakund) internally

Complete Documentation available [here](https://youtube-api.datakund.com/en/latest/)


### Support
For any help / feedback you can message us here
* datakund@gmail.com
* https://t.me/datakund

### Installation

```sh
pip install youtube-comment-auto-liker
```

### Import

```javascript
from youtube-comment-auto-liker import *
```

### Login

To like any video comment first we need to login to youtube. There are two ways of login:-
* Credentials
* Cookies

#### Credentials

```javascript
youtube.login(email="",password="")
```

#### Cookies

```javascript
youtube.login_cookie(cookies="list_of_cookies")
```

##### Example Cookies

To login with cookies [Edit this Cookie Extension](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=en) can be added to browser and login to youtube.com , then export cookies and paste in above function of ``login_cookie``. Below is the example of cookies.

```[
{
    "domain": "youtube.com",
    "expirationDate": 1671116358.392265,
    "hostOnly": false,
    "httpOnly": false,
    "name": "__Secure-3PAPISID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "Y1zkx3HJhktM4Y__/A-aOUDHse1TaSaKpQ",
    "id": 1
},
{
    "domain": "youtube.com",
    "expirationDate": 1672322803.302724,
    "hostOnly": false,
    "httpOnly": true,
    "name": "__Secure-3PSID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "5AcqKCt5MuBkjOpLW7PdfNs83knLqt-qVZJzCriY_4_cftxmyExDbYRS65ezLjpKa_Xc7Q.",
    "id": 2
},
...
...

]
```

### Open Video

To open video we use ``open`` function
It requires **url** as input parameter

```javascript
youtube.open("place_video_url_here")
```

### Scroll Down

To bring video comments into view we will scroll the page using ``keypress`` function
It requires **key** as input parameter
We will use **pagedown** key to scroll the page down

```javascript
youtube.keypress("pagedown")
```

### Like a particular comment

To like a particular comment we use ``like_comment`` function
It requires **comment** as input parameter

```javascript
youtube.like_comment(comment="comment_text_here")
```

### DataKund
It uses [datakund](https://pypi.org/project/datakund/) internally to do browser automation
DataKund is an automation library that uses selenium & supports automation of many sites including [Youtube](https://youtube-api.datakund.com/en/latest/), [Amazon](https://amazon-api.datakund.com/en/latest/), [Twitter](https://twitter-api.datakund.com/en/latest/), [LinkedIn](https://linkedin-api.datakund.com/en/latest/) , [Google](https://google-api.datakund.com/en/latest/) etc.
