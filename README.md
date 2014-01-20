jquery-scrollstop
=================

This plugin fires two events on `window` when scrolling starts and stops:
`scrollstart` and `scrollstop`.

## Example

The example shows a small box in the upper left that says "SCROLLING" and
colors the body different colors when scrolling: http://ssorallen.com/jquery-scrollstop/

## Usage

`scrollstart` fires after the first scroll event and won't fire again until
after a `scrollstop` event is fired.

`scrollstop` fires after no `scroll` events have fired for 250 milliseconds.

```js
$(window)
  .on("scrollstart", function() {
    // Paint the world yellow when scrolling starts.
    $(document.body).css({background: "yellow"});
  })
  .on("scrollstop", function() {
    // Paint it all green when scrolling stops.
    $(document.body).css({background: "green"});
  })
```

### Configuration

#### latency

`latency` is the minimum time between the last scroll event and when the
`scrollstop` event fires. Set `$.event.special.scrollstop.latency` to the
desired number of milliseconds (default: 250).

```js
// Configure time between final scroll event and `scrollstop` event to 650ms (default is 250ms).
$.event.special.scrollstop.latency = 650;
```

### jQuery Version Support

The plugin is tested in jQuery 1.2.3+ and jQuery 2.0.3+.

### Attribution

James Padolsey's jQuery scrollstop plugin that fires an event when scrolling
stops for minimum amount of time.

Originally code copied from
http://james.padolsey.com/javascript/special-scroll-events-for-jquery/
