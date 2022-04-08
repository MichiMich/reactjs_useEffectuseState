# useState useEffect Example ReactJs
Since I got a lot of trouble by using and triggering the useState, useEffect I wanted to share a little example here.
It is meant as simple as effective to dynamically change the webconent by different events.
I fell for multiple renders and too much rendering as well, so I hope you can learn from this.

I highly recommend reading this: [reactjs using the effect](https://reactjs.org/docs/hooks-effect.html) and turning back here than and trying out the useState, useEffect.

# Requirements

<ul dir="auto">
<li><a href="https://git-scm.com/book/en/v2/Getting-Started-Installing-Git" rel="nofollow">git</a>
<ul dir="auto">
<li>You'll know you did it right if you can run <code>git --version</code> and you see a response like <code>git version x.x.x</code></li>
</ul>
</li>
<li><a href="https://nodejs.org/en/" rel="nofollow">Nodejs</a>
<ul dir="auto">
<li>You'll know you've installed nodejs right if you can run:
<ul dir="auto">
<li><code>node --version</code> and get an ouput like: <code>vx.x.x</code></li>
</ul>
</li>
</ul>
</li>
<li><a href="https://classic.yarnpkg.com/lang/en/docs/install/" rel="nofollow">Yarn</a> instead of <code>npm</code>
<ul dir="auto">
<li>You'll know you've installed yarn right if you can run:
<ul dir="auto">
<li><code>yarn --version</code> and get an output like: <code>x.x.x</code></li>
<li>You might need to install it with npm</li>
</ul>
</li>
</ul>
</li>
</ul>
</li>
</ul>

# Getting Started with Create React App
go to the directory UseStateUseEffectExample and run `npm start`
this runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes and save them.\
**fire up your console using F12 and going to console**
Observer what the console tells you everytime you click the 'ChangeElement' button

**remove the `[getHtml]` from line 14, save file and check the console output now**
you will see that the useEffect ran is now fired twice everytime you push the 'ChangeElement' button.
This is because you trigger the `setElement()` in line 18 -> this means useEffect run and
you trigger the  `setHtml()` in line 19 -> this means useEffect run.
**so with the `[getHtml]` we optimized our script**

# Play with it
The sense of this is to have a change of one variable which results on the change of a content on the website.
I personally used this to display different svgs depending on results of triggered functions.

****

# Description
Here we have to useStates:
`const [getElement, setElement] = useState('');
 const [getHtml, setHtml] = useState();`

## const [getElement, setElement] = useState('')
the setElement sets a new value(values change between 'connect', 'joinRaffle', 'error', 'success') which can be get by getElement.
so we have a variable which changes its string between this 4 values.

## const [getHtml, setHtml] = useState();
this is the interesting part: the setHtml changes the div element which we **want to show at the webpage**:
`<div>my htmlElement {getHtml}</div>` 
**So our content after "my htmlElment " changes depending on the 4 values from the getElement **
**this means we change our webcontent every time we trigger the 'timeout' button**