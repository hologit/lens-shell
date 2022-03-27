# lens-shell

Run an arbitrary shell script with arbitrary Habitat packages

## Usage

```toml
[hololens]
package = "holo/lens-shell/1.0"
before = "cert-manager"

[hololens.shell]
script = '''
mv -v Chart.template.yaml Chart.yaml
'''

[hololens.input]
root = "cert-manager/helm-chart"
files = "**"

[hololens.output]
merge = "replace"
```
