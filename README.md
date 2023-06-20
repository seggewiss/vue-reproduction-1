# vue-project

This project illustrates a problem with Vue 2.7 and 3 where TypeScript types no longer match after being in a data property.

## Setup

1. Clone this repository
2. Cd into it
3. `npm i`

## Problem

See `src/components/Problem.vue@19`. Although the criteria is being created by the same import that is expected for the type, the fact that one saves this in a data property at line 17 breaks the type check. See the examples after line 21 to see that there is no general problem with the type definition.