Now we'll use props to further customize our components.

## Task
1) Add a hover effect to the `Card` component

Cards can be customized using several props.

In this exercise, we'll be using the `isHoverable` prop to add a cool hover effect to the card.

<pre class="file" data-target="clipboard">

</pre>

2) Change the button variants

Buttons have a lot of possible variants.

To explore some more of them, let's remove the `isInline` prop and change our first footer button to a `primary` button.

<pre class="file" data-target="clipboard">
&lt;SplitItem&gt;
  &lt;Button variant=&quot;primary&quot;>Link to PatternFly&lt;/Button&gt;
&lt;/SplitItem&gt;
</pre>

3) Now let's see what a `danger` variant looks like on the second footer button:

<pre class="file" data-target="clipboard">
&lt;SplitItem&gt;
  &lt;Button variant=&quot;danger&quot;>Link to home&lt;/Button&gt;
&lt;/SplitItem&gt;
</pre>

When these steps are complete - the finished card should look like this on hover:
<img src="module-1/assets/final-card-with-customizations.png" alt="Completed card component with hover effect and modified buttons" style="box-shadow: rgba(3, 3, 3, 0.2) 0px 1.25px 2.5px 0px;" />
