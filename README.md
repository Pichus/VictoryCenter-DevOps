# VictoryCenter DevOps

Infrastructure and deployment configuration for VictoryCenter.

## Submodules

This repo includes two submodules:

| Folder | Repo | Branch |
|--------|------|--------|
| `VictoryCenter-Client` | [VictoryCenter-Client](https://github.com/ita-social-projects/VictoryCenter-Client) | `release/1.0.0` |
| `VictoryCenter-Back` | [VictoryCenter-Back](https://github.com/ita-social-projects/VictoryCenter-Back) | `release/1.0.0` |

### Clone with submodules

```bash
git clone --recurse-submodules https://github.com/Pichus/VictoryCenter-DevOps.git
```

If already cloned without submodules:

```bash
git submodule update --init --recursive
```

### Update submodules to latest commits on their branch

```bash
git submodule update --remote --merge
```

Or update a single submodule:

```bash
git submodule update --remote --merge VictoryCenter-Client
git submodule update --remote --merge VictoryCenter-Back
```

After updating, commit the new submodule pointers:

```bash
git add VictoryCenter-Client VictoryCenter-Back
git commit -m "chore: update submodules to latest"
```
