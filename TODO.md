To Update:
1) (Need to update `Capybara` restrictions to something less old!)
2) Generic Update of dependencies
4) Update of Ruby Version to supported version

Next Up:
1) Figure out why the loadable spec isn't playing nicely with code-coverage
One line to tidy up for full compliance: `spec/page_spec.rb:91`
2) Fix `page_element_interaction_steps.rb`: Triple Expectations and non-Helper expectation
3) Fix `page_section_steps.rb` - Triple expectations
4) Generic Features are sometimes hard to understand. Look to rework the Gherkin
5) `page_element_interaction_steps.rb:49` Shouldn't be there as its performing Actions
6) After Capybara dependency is 2.6+
- capybara 2.5 was the first Capybara to introduce `default_max_wait_time`
- Once we get pre-reqs up to there we can massively simplify `./lib/site_prism/waiter.rb`
- This will basically make the entire class a 2/3liner
7) `site_prism/addressable_url_matcher.rb` - Just needs a bit of a spring clean
8) `SitePrism::Page#wait_until_displayed` - Re-call existing method and re-raise
9) Begin to refactor displayed?(*args), to remove enumerable args (Shouldn't be enumerable)
10) iFrame helper methods - Potential bug to fix (Assumed to be broken) (Issue #66)
11) New feature `SitePrism::Section#native` returning `root_element.native` To help with
people wanting to access the base native object (Honouring what maintainers said)
12) Exceptions Spec needs writing
13) element/s spec need a slight rename / tidy
14) sections_spec.rb needs moving
15) Version spec primitive needs making 

To monitor (Assumed fixed elsewhere)
1) Capybara compatibility around iFrames
2) SitePrism anonymous sections
