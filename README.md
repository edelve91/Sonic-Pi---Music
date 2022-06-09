# Sonic-Pi---Music

In these notes I will put some code written in Sonic Pi.

## :Idea => Application

```ruby
12.times do
  with_octave 5 do
    puts p
    play p.reverse.tick
    sleep 1
  end
end
```
