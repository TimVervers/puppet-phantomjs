require 'rake'
require 'puppet-lint/tasks/puppet-lint'
require 'puppetlabs_spec_helper/rake_tasks'

PuppetSyntax.future_parser = true

namespace :puppet do
  desc 'Lint Puppet files'
  PuppetLint::RakeTask.new :lint do |config|
    # Define the whitelist for the linter
    config.pattern = [
      'manifests/**/*.pp'
    ]

    # Should the task fail if there were any warnings, defaults to false
    config.fail_on_warnings = true

    # Compare module layout relative to the module root
    config.relative = true
  end
end
