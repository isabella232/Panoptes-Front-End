# Feedback Strategy: Radial

Determines whether a point is within a given tolerance.

## Subject metadata fields

A single subject can have multiple feedback rules. To group the metadata fields for a single feedback rule together, `N` should be an integer that is identical for each rule, e.g.:

```
#feedback_1_id,#feedback_1_x,#feedback_1_y,#feedback_2_id,#feedback_2_x,#feedback_2_y...
```

- `#feedback_N_id` (**required**) - ID of the corresponding workflow task rule.
- `#feedback_N_x` (**required**) - x value of the target circle.
- `#feedback_N_y` (**required**) - y value of the target circle.
- `#feedback_N_tolerance` (optional) - radius of the target circle. Overrides the default tolerance set on the workflow task rule.
- `#feedback_N_successMessage` (optional) - message to show when the target is correctly annotated. Overrides the default success message set on the workflow task rule.
- `#feedback_N_failureMessage` (optional) - message to show when the target is incorrectly annotated. Overrides the default failure message set on the workflow task rule.
- `#feedback_N_falsePosMode` (optional) - if `true`, specifies that a click within the specified tolerance region should be interpreted as a false positive and no failure message will be displayed. False positives will render as red circles in the modal feedback window if a click is registered within tolerance on and will not render otherwise. The default is `false`.
- `#feedback_N_falsePosMode` (optional) - if `true`, specifies that a click within the specified circular region should be interpreted as a false positive and no failure message will be displayed. False positives will render as red circles in the modal feedback window if clicked on and will not render otherwise. The default is `false`.
