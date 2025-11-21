# Prototyping Constraints & Trade-offs

## Rendering splits
- Full page: `/tasks` returns layout + list + pager.
- Fragment: `/tasks/fragment` returns nothing - this shows an error

## URL & History
- `hx-push-url="true"` on filter and pager links keeps Back/Forward meaningful.
- If this is removed then the back/fordward wouldn't work as well

## Accessibility hooks
- Live region `#status` announces changes.
- Result count associated with list via `aria-describedby`.

## Performance notes
- Page size: 10 items; consider server time vs client cost.
- Fragments avoid re-sending the full layout.

## Future risks
- Template duplication between full page and fragments.
- Focus management after deletes (ensure next focusable target).

## Accessibility verification

### Keyboard testing
- Can tab through the page in a logical order
- Can click on all buttons using keyboard
- Can not click on links when using keyboard

### Screen reader testing
- Just announced that it is the filter button 

### No-JS parity
- Filter doesn't work without JS enabled 