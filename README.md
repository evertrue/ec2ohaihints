# ec2ohaihints

The sole purpose of this cookbook is to be included in the run lists of _other_ cookbooks when you need those cookbooks to pick up `ec2` metadata. This is mainly useful when building a node with the [kitchen-ec2](https://github.com/test-kitchen/kitchen-ec2) test-kitchen plugin.

## Usage

Add a reference to your Berkshelf file:

```ruby
# ./Berkshelf
group :integration do
  cookbook 'ec2ohaihints'
end
```

Then add it to your run list:

```yaml
# ./.kitchen.yml
suites:
  - name: default
    run_list:
      - recipe[ec2ohaihints::default]
```

## License

[WTFPL](http://www.wtfpl.net/)
