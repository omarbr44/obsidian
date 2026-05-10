# Problem: Achieve expand collapse folder transition not working

**Date:** {{date}}

## Context
(Where did this happen? Project, environment, etc.)

## Problem
Used `<Transition>` with `transform: translateY`, but the expand/collapse felt not right.

## Solution
The solution as to transition max-height and give an overflow of hidden (so max height of 0 and max height for large number )

The code
```
<Transition name="collapse">

<div v-show="isOpen" class="overflow-hidden">

<SidebarSubFilesStrucureComponent

v-for="file in item.items"

:key="file.label"

:item="file"

/>

</div>

</Transition>


/* Active state: transition applies */

.collapse-enter-active,

.collapse-leave-active {

transition: max-height 0.3s ease;

overflow: hidden;

}

  

/* Start collapsed */

.collapse-enter-from,

.collapse-leave-to {

max-height: 0;

}

  

/* End expanded */

.collapse-enter-to,

.collapse-leave-from {

max-height: 500px; /* pick a safe upper bound */

}
```

## Lessons Learned
Animating `max-height` + `overflow: hidden` creates a natural slide effect.

## Tags
#problem #fix #transition #vue
