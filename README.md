# ipyvizzu

Jupyter notebook integration for vizzu.

ipyvizzu only works in jupiter notebook environment. A notebook cell may
contain the following code snippet.

```python
import ipyvizzu

data = ipyvizzu.Data()
data.add_serie("Foo", ["Alice", "Bob", "Ted"])
data.add_serie("Bar", [15, 32, 12])
data.add_serie("Baz", [5, 2, 2])

chart = ipyvizzu.Chart()
chart.set_data(data)

chart.animate(x="Foo", y="Bar", color="Foo")
chart.animate(geometry="circle")
chart.animate(x="Foo", y="Baz", color="Foo")
chart.animate(geometry="rectangle")

chart.show()
```

## Installation

ipyvizzu requires only `IPython` package, but you can use it only in jupyter
notebook therefore `notebook` project has to be installed.

```sh
pip install -e .
pip install notebook
```

## Documentation

Documentation can be build with the `doc` make target.

```sh
make doc
```

Online version can be read at [vizzuhq.github.io/ipyvizzu](https://vizzuhq.github.io/ipyvizzu/index.html).
