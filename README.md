# UX Experiment: Locking Suggestion List

This is a demonstration of an auto-complete / type-ahead suggestion list which is populated asynchronously
to improve the perceived performance, but also addresses a big drawback of this auto-refining solution
where items are added to the list as soon as they become available (or prove inapplicable) and where the
list may re-sort multiple times as the items within refine:

The keyboard and mouse navigation experience.

With such controls, when pressing key up / down to go to prev/next item, or hovering over an item to click,
it is possible for the underlying item to change or disappear resulting in an incorrect selection being
made from the user's point of view.

Due to this concern this design is often rejected in favor or longer loading but once rendered
delayed item collection, which doesn't suffert from this because it doesn't change unless the user
continues to type, where it is an expected and easily understandable / discoverable behavior.

My solution to this problem is to lock prev / next items to the selected and hovered-over items in place
disregarding any update signals from the underlying data source (which is an iterable and gets sorted
with each addition).

Please note this is applicable to any UI list, but I believe is most applicable to these suggestion lists.

## Running

So far there's no work done.
