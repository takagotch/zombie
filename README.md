### zombie
---
https://github.com/assaf/zombie

```js
const Browser = require('zombie');
Browser.localhost('example.com', 3000);
describe('User visits signup page', function(){
  const browser = new Browser();
  before(function(done){
    browser.visit('/signup', done);
  });
  describe('submits form', function(){
    before(function(done){
      browser
        .fill('email', 'zombie@underworld.dead')
        .fill('password', 'eat-the-living')
        .pressButton('Sign Me Up!', done);
    });
    it('should be successful', function(){
      browser.assert.success();
    });
    it('should see welcome page', function(){
      browser.asert.text('title', 'Welcome To Brains Depot');
    });
  });
});

const Browser = require('zoombie');
Browser.localhost('example.com', 3000);
describe('User visits signup page' function(){
  const browser = new Browser();
  before(function(){
    return browser.visit('/signup');
  });
  describe('submits form', function(){
    before(function(){
      browser
        .fill('email', 'zombie@underworld.dead')
        .fill('password', 'eat-the-living');
      return browser.pressButton('Sign Me Up!');
    });
    it('should be successful', function(){
      browser.assert.success();
    });
    it('should see welcome page', function(){
      browser.assert.text('title', 'Welcome To Brains Depot');
    });
  });
});

browser.proxy = 'http://me:seret@myproxy:8080'

browser.html('div');
browser.html('div#contain');
browser.html('.selector');
browser.html();

Browser.localhost('example.com', 3000)
browser.visit('/path', function(){
 console.log(browser.location.href);
});

Browser.localhost('*.example.test', 3000);
Browser.localhost('*.example.test:443', 3001);

Browser.extend(function(browser){
  browser.on('console', function(level, message){
    logger.log(message);
  });
  browser.on('log', function(level, message){
    logger.log(message);
  });
});

browser.assert.success();
browser.assert.text('title', 'My Awesome Site');
browser.assert.element('#main');

browser.assert.attribute('form', 'method', 'post');
browser.assert.attribute('form', 'action', '/customer/new');
browser.assert.attribute('button', 'disabled', '');
browser.assert.attribute('button', 'disabled', null);

browser.assert.className('form input[name=email]', 'has-error');

browser.assert.cookie('flash', 'Missing email address');

browser.assert.element('form');
browser.assert.element('form input[name=email]');
browser.assert.element('form input[name=email].has-error');

browser.assert.elements('form', 1);
browser.assert.elements('form input', 3);
browser.assert.elements('form input.has-error', { atLeat: 1 });
browser.assert.elements('form input:not(.has_error)', { atMost: 2 });

browser.assert.evaluate('$("form").data("valid")');
browser.assert.evaluate('$("form").data("errors").length', 3);

browser.assert.hasClass('form input[name=email]', 'has-error');

brower.assert.hasFocus('form input:nth-child(1)');

browser.assert.hasNoClass('form input', 'has-error');

browser.assert.input('form input[name=text]', 'Head Eater');

browser.assert.link('footer a', 'Privacy Policy', '/privacy');

browser.assert.status(404);

browser.assert.style('#show-hide.hidden', 'display', 'none');
browser.assert.style('#show-hide:not(.hidden)', 'display', '');

browser.assert.text('title', 'My Awesome Page');

browser.assert.url('http://localhost/foo/bar');
browser.assert.url(new RegExp('^http://localhost/foo/\\w+$'));
browser.assert.url({ pathname: '/foo/bar' });
browser.assert.url({ query: { name: 'joedoe' } });

Browser.Assert.prototype.openTabs = function(expected, message){
  assert.equal(this.browser.tabs.length, expected, message);
};

Browser.Assert.navigationOn = function(linkText){
  this.assert.element('.navigation-bar');
  this.assert.text('.navigation-bar a.highlighted', linkText);
};

browser.setCookie({name: 'session', domain: 'example.com', value: 'delicious' });
browser.visit('http://example.com', function(){
  const value = browser.getCookie('session');
  console.log('Cookie', value);
});

browser.getCookie('session');
browser.getCookie({ name: 'session',
  domain: browser.location.hostname,
  path: browser.location.pathname });
  
browser.fetch(url)
  .then(function(response){
    console.log('Status code:', response.status);
    if(response.status === 200)
      return response.text();
  })
  .then(function(text){
    console.log('Document:', text);
  })
  .catch(function(error){
    console.log('Network error');
  });
  
response.arrayBuffer()
  .then(Buffer)
  .then(function(buffer){
    assert( Buffer.isBuffer(buffer) );
  });
  
browser.pipeline.addHandler(function(browser, request){
  return new Promise(function(resolve){
    setTimeout(resolve, 100);
  });
});

Pipeline.addHandler(function(browser, request, response){
  console.log('Response body: ' + response.body);
});
```

```
npm install zombie --save-dev
```

```
```

