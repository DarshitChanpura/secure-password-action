# Secure Password Generator Action

![GitHub release](https://img.shields.io/github/v/release/DarshitChanpura/secure-password-action)
![GitHub license](https://img.shields.io/github/license/DarshitChanpura/secure-password-action)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/DarshitChanpura/secure-password-action/test.yml)

A GitHub Action to **generate a strong password securely** without exposing it in logs.

## 🚀 Usage

```yaml
jobs:
  generate-password:
    runs-on: ubuntu-latest
    steps:
      - name: Use Secure Password Generator
        id: generate-password
        uses: DarshitChanpura/secure-password-action@main

      - name: Print Masked Password (for example usage)
        run: echo "Password has been securely generated!"
```

## 🔑 Outputs

| Output    | Description |
|-----------|------------|
| `password` | The generated secure password (masked in logs) |

## ⚙️ Inputs (Optional)

| Input  | Default | Description |
|--------|---------|-------------|
| `length` | `24` | Length of the generated password |

Example:
```yaml
- uses: DarshitChanpura/secure-password-action@main
  with:
    length: 32
```

## 🛠 Development & Testing

To test the action locally, run:

```bash
act -W .github/workflows/test.yml
```

## 📜 License
This project is licensed under the [Apache License 2.0](LICENSE).
