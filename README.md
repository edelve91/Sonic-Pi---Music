# Sonic-Pi---Music

In these notes I will put some code written in Sonic Pi.

## Creativity = {:Mathematical Music Theory => Computer Application }

```ruby

## DJ_Edelve

define :parabolic_harmony do |ring_field, k, h, a|
    x = (0...ring_field).to_a
    y = []
    for i in (0...ring_field).to_a
      parabola_equation = ((a*(i - h) ** 2 + k) % ring_field)
      y.push(parabola_equation)
    end
    points = x.zip(y)
end

p = parabolic_harmony(12,3,7,1)

12.times do
  with_octave 5 do
    puts p
    synth :dsaw, note: p.shuffle.tick
    sleep 1
  end
end
```
