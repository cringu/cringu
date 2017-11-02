# Cringu

[![Join the chat at https://gitter.im/cringu/cringu](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cringu/cringu?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) 

A game framework for libSDL2 on crystal, inspired by ippa/chingu.

![Cringu Header Image](https://github.com/cringu/cringu/blob/master/assets/cringu-50.png?raw=true)

## Installation
Will be here soon.

Add this to your application's `shard.yml`:

```yaml
dependencies:
  cringu:
    github: cringu/cringu
```

## Usage

```crystal
require "cringu"
```

```crystal
require "../cringu"

WWIDTH = 800_f64
WHEIGHT = 600_f64
LAYERS_ENABLED = true

class Square < GameObject
  property size = 80_f64
  def update
    f = rand(0.1..0.9)
    Graphics.draw_block(@pos.x * f, @pos.y * f, @size * f, BasicColor.sample);
  end
end
5.times do
s = Square.new
s.pos.x = (WWIDTH / 2 - s.size / 2) * rand(0.1..0.9)
s.pos.y = (WHEIGHT / 2 - s.size / 2) * rand(0.1..0.9)
s.manage
end
NGine.setup WWIDTH, WHEIGHT
NGine.start
```

## Development

TODO: Write development instructions here

## Contributing

1. Fork it ( https://github.com/cringu/cringu/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [[jamiepirie]](https://github.com/jamiepirie) Jamie - creator, maintainer
