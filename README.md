# Flatiron Process / Scenarios Matching Game

## Introduction

Let's make sure you understand how to apply the Flatiron Process. We'll provide
a series of scenarios. Match where that scenario fits into the Flatiron
Process.

## Scenario 1

"Every morning at the CoffeBux on Broadway, people cross in front of me in the
line to get to the sugar and stirrer station. Surely there's a way to help flow
in this store much better."

## Scenario 2

At McVegan's, if we want to show diners when their order is ready we need:

* A TV
* An order tracking system
* A way to change the order from "in progress" to "done"
* A way to mark the order from "done" to "received" and remove it from the
  board that the TV shows

## Scenario 3

I want to create a way to create templates.

<pre>
For each word in a string
  If the word starts with `${` and we can find a "closing" `}`
    Grab the word inside the `${` and `}`
      Use that word as a key in a hash and add that value to the `output` string
  If the word doesn't start with `${`, put the word in the `output` string
</pre>

## Scenario 4

Lauren writes the following in a file called `we_love_dogs.rb`:

```ruby
attributes = {
  "name" => "Byron",
  "adjective" => "wonderful",
  "breed" => "poodle"
}

template_string = "I love my dog ${name}, he is a ${adjective} ${breed}."
translated_words = template_string.split.map do |token|
  !token.match(/\$\{(.*)\}/) ? token : attributes[$1]
end
p translated_words.join(" ")
```

