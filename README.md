jquery-scrollstop
=================

The plugin fires two events on `window` when scrolling starts and stops:
`scrollstart` and `scrollstop`.

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

### jQuery Version Support

The plugin is tested in jQuery 1.2.3+ and jQuery 2.0.3+.

### Attribution

James Padolsey's jQuery scrollstop plugin that fires an event when scrolling
stops for minimum amount of time.

Originally code copied from
http://james.padolsey.com/javascript/special-scroll-events-for-jquery/
