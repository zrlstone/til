# Feature and Scenario DSL

The feature and scenario DSL correspond to `describe` and `it`.

```ruby
  require "rails_helper"

  RSpec.feature "Widget management", type: :feature do
    scenario "User creates a new widget" do
      visit "/widgets/new"

      click_button "Create Widget"

      expect(page).to have_text("Widget was successfully created.")
    end
  end
```

See [the
docs](https://rspec.info/features/6-0/rspec-rails/feature-specs/feature-spec/)
for more details.