Katacoda is setting up a new React application for you. You'll be ready to code once the server starts and you can see "Edit src/App.js and save to reload." on the lower pane.

## Task
A card is a flexible element for containing any kind of content. Cards are used on dashboards, in data displays (e.g. Card View), or for positioning content on a page. In this exercise, we'll be creating a card with an image, action, header, body, and footer.

In PatternFly 4, separate components are used to demarcate the different regions of a card so it can be fully customized. For example, images are placed in CardHead, actions in CardActions, and the header in CardHeader.

1) Navigate to myapp/src and open App.js

2) Set up the imports we'll need and the general structure of the card. 

Copy the following code into the App.js file:

<pre class="file" data-filename="App.js" data-target="replace">
import React from 'react';
import &quot;@patternfly/react-core/dist/styles/base.css&quot;;
import {
  Brand,
  Button,
  Card,
  CardActions,
  CardHead,
  CardHeader,
  CardBody,
  CardFooter,
  Split,
  SplitItem,
  Text,
  TextContent,
  TextVariants
} from '@patternfly/react-core';
import {
  TimesIcon
} from '@patternfly/react-icons';

function App() {
  return (
    &lt;Card&gt;
      &lt;CardHead&gt;
        &lt;CardActions&gt;
        &lt;/CardActions&gt;
      &lt;/CardHead&gt;
      &lt;CardHeader&gt;
      &lt;/CardHeader&gt;
      &lt;CardBody&gt;
        PatternFly is an open source design system created to enable consistency and usability across a wide range of applications and use cases. PatternFly provides clear standards, guidance, and tools that help designers and developers work together more efficiently and build better user experiences.
      &lt;/CardBody&gt;
      &lt;CardFooter&gt;
      &lt;/CardFooter&gt;
    &lt;/Card&gt;
  );
}

export default App;
</pre>

3) Add a text component to the CardHeader component

The text component can wrap any static HTML content you want to place on your page to provide correct formatting when using standard HTML tags. It comes in several variations, such as `h1`, `p`, `a`, `small`, `blockquote`, and `pre`. In this exercise, we'll be using the `p` variation. Add the following code to the CardHeader component and specify the variant using `component={TextVariants.p}`.

<pre class="file" data-target="clipboard">
&lt;Text component={TextVariants.p}&gt;
  Patternfly
&lt;/Text&gt;
</pre>

4) Add a brand to the CardHead component

The brand component is used to place a product logotype on a screen. All you need to provide are the source image or svg and alt text.

<pre class="file" data-target="clipboard">
&lt;Brand src=&quot;https://pf4.patternfly.org/assets/images/pf-logo-small.svg&quot; alt=&quot;Patternfly Logo&quot; /&gt;
</pre>

5) Add a Split layout to the CardFooter component

PatternFly 4 offers several layout options, including grid, bullseye, and split layouts. In this exercise, we'll be using a split layout to separate a pair of buttons in the footer of our card. We'll be adding a `<SplitItem>` component inside `<Split>` for each item in the layout.

<pre class="file" data-target="clipboard">
&lt;Split&gt;
  &lt;SplitItem&gt;
  &lt;/SplitItem&gt;
  &lt;SplitItem&gt;
  &lt;/SplitItem&gt;
&lt;/Split&gt;
</pre>

6) Add a button to the first SplitItem

Buttons communicate and trigger actions a user can take in an application or website. They come in several variations, such as primary, secondary, danger, plain, and link.

We'll be using the "link" variant and adding an isInline prop so that the buttons are inline rather than block elements.

<pre class="file" data-target="clipboard">
&lt;Button variant=&quot;link&quot; isInline>Link to PatternFly&lt;/Button&gt;
</pre>

7) Add a second button to the second SplitItem:

<pre class="file" data-target="clipboard">
&lt;Button variant=&quot;link&quot; isInline>Link to home&lt;/Button&gt;
</pre>

8) Add a gutter prop to the Split components to add more spacing between the buttons:

<pre class="file" data-target="clipboard">
gutter="md"
</pre>

9) Add a close button to the Card component in the CardAction component

PatternFly React provides a variety of icons as well as components, layouts, charts, and demos. They're just as easy to use and compile into svgs.

<pre class="file" data-target="clipboard">
&lt;Button variant=&quot;plain&quot;&gt;
  &lt;TimesIcon /&gt;
&lt;/Button&gt;
</pre>

10) Add a subhead below the "PatternFly" Text component in the CardHeader component

TextContent is used to wrap Text components and provides text with extra spacing and styling.

<pre class="file" data-target="clipboard">
&lt;TextContent&gt;
&lt;Text component={TextVariants.small}&gt;
  Provided by Red Hat
&lt;/Text&gt;
&lt;/TextContent&gt;
</pre>