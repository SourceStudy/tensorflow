### `tf.nn.quantized_avg_pool(input, min_input, max_input, ksize, strides, padding, name=None)` {#quantized_avg_pool}

Produces the average pool of the input tensor for quantized types.

##### Args:


*  <b>`input`</b>: A `Output`. Must be one of the following types: `qint8`, `quint8`, `qint16`, `quint16`, `qint32`.
    4-D with shape `[batch, height, width, channels]`.
*  <b>`min_input`</b>: An `Output` of type `float32`.
    The float value that the lowest quantized input value represents.
*  <b>`max_input`</b>: An `Output` of type `float32`.
    The float value that the highest quantized input value represents.
*  <b>`ksize`</b>: A list of `ints`.
    The size of the window for each dimension of the input tensor.
    The length must be 4 to match the number of dimensions of the input.
*  <b>`strides`</b>: A list of `ints`.
    The stride of the sliding window for each dimension of the input
    tensor.  The length must be 4 to match the number of dimensions of the input.
*  <b>`padding`</b>: A `string` from: `"SAME", "VALID"`.
    The type of padding algorithm to use.
*  <b>`name`</b>: A name for the operation (optional).

##### Returns:

  A tuple of `Output` objects (output, min_output, max_output).

*  <b>`output`</b>: A `Output`. Has the same type as `input`.
*  <b>`min_output`</b>: An `Output` of type `float32`. The float value that the lowest quantized output value represents.
*  <b>`max_output`</b>: An `Output` of type `float32`. The float value that the highest quantized output value represents.

