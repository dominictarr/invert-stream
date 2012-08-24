# invert-stream

Create a pair of streams (A, B) such that `A.write(X) -> B.emit('data', X)`
and `B.write(X) -> A.emit('data', X)`

``` js

var invert = require('invert-stream')

var A = invert()

in_steam.pipe(A).pipe(out_stream)

var B = A.b

B.write(data_for_outstream)
B.on('data', data_from_in_stream)

## License

MIT
