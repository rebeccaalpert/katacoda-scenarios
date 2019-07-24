Katacoda is setting up a new React application for you. You'll be ready to code once the server starts and you can see "Edit src/App.js and save to reload." on the lower pane.

## Task
1) Navigate to myapp/src and open App.js

2) Copy the following code into the App.js file:
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
  Grid,
  GridItem,
  Page,
  PageSection,
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
    &lt;Page&gt;
      &lt;PageSection&gt;
        &lt;Grid&gt;
          &lt;GridItem&gt;
          &lt;/GridItem&gt;
          &lt;GridItem&gt;
          &lt;/GridItem&gt;
          &lt;GridItem&gt;
          &lt;/GridItem&gt;
        &lt;/Grid&gt;
      &lt;/PageSection&gt;
    &lt;/Page&gt;
  );
}

export default App;
</pre>

3) Add the following Card to each GridItem:

<pre class="file" data-target="clipboard">
&lt;Card&gt;
  &lt;CardHead&gt;
  &lt;/CardHead&gt;
  &lt;CardHeader&gt;
    &lt;Text component={TextVariants.p}&gt;
      Patternfly
    &lt;/Text&gt;
  &lt;/CardHeader&gt;
  &lt;CardBody&gt;
    PatternFly is an open source design system created to enable consistency and usability across a wide range of applications and use cases. PatternFly provides clear standards, guidance, and tools that help designers and developers work together more efficiently and build better user experiences.
  &lt;/CardBody&gt;
  &lt;CardFooter&gt;
  &lt;/CardFooter&gt;
&lt;/Card&gt;
</pre>

4) Add a gutter prop to the Grid component:

<pre class="file" data-target="clipboard">
gutter="md"
</pre>

5) Add a brand to the CardHead components:

<pre class="file" data-target="clipboard">
&lt;Brand src=&quot;https://pf4.patternfly.org/assets/images/pf-logo-small.svg&quot; alt=&quot;Patternfly Logo&quot; /&gt;
</pre>

6) Add two buttons to the CardFooter components:

<pre class="file" data-target="clipboard">
&lt;Split&gt;
  &lt;SplitItem&gt;
    &lt;Button variant=&quot;link&quot; isInline>Link to PatternFly&lt;/Button&gt;
  &lt;/SplitItem&gt;
  &lt;SplitItem&gt;
    &lt;Button variant=&quot;link&quot; isInline>Link to home&lt;/Button&gt;
  &lt;/SplitItem&gt;
&lt;/Split&gt;
</pre>

7) Add a gutter prop to the Split components:

<pre class="file" data-target="clipboard">
gutter="md"
</pre>

8) Add a close button to the Card component in the CardHead components:

<pre class="file" data-target="clipboard">
&lt;CardActions&gt;
&lt;Button variant=&quot;plain&quot;&gt;
  &lt;TimesIcon /&gt;
&lt;/Button&gt;
&lt;/CardActions&gt;
</pre>

9) Add a subhead below the "PatternFly" Text component in the CardHeader components:

<pre class="file" data-target="clipboard">
&lt;TextContent&gt;
&lt;Text component={TextVariants.small}&gt;
  Provided by Red Hat
&lt;/Text&gt;
&lt;/TextContent&gt;
</pre>