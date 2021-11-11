# Front-end Developer Exercise

Copyright 2021 Kin Workplace Software, LLC

## Objective

Update homepage and build a brand new pricing page that will allow users to choose a pricing plan.

## Requirements

- Fork this repository and submit your finished work as a pull request.

### Homepage

- Provide a visual representation as to what the current active page is being viewed within the navigation links.
- Reduce the size of the website title, _Company Inc._ on smaller viewports.

### Pricing Page

- Create a `PricingCard` component in a `components` directory to match visual style of screenshots provided within `static` directory.
- Utilize [Vuex](https://vuex.vuejs.org/) store for `PricingCard` data.
- Create a series of `PricingCard` components that display all options.
- Create single globally accessible modal and display when new `PricingCard` is chosen.
- Update chosen plan globally within Vuex.
- Stack pricing cards vertically on smaller viewports to match visual style of screenshots provided.

## Success Criteria

- The markup should be semantic and accessible.
- The design should match screenshots provided.
- No additional external libraries or plugins should be installed.
- **Bonus** Create a standalone stylesheet within the overall framework that provides a dark mode that can be optionally toggled with a UI component

## Tips

- Feel free to utilize as much of [Boostrap Vue](https://bootstrap-vue.org/) as desired
- Example was scaffolded using Node 14.18
