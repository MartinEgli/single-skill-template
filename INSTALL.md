# Install

This template is designed for repositories that publish one skill.

Replace `MartinEgli/single-skill-template` with your real repository after you
create a derived skill repo.

## Codex

```powershell
npx -y skills add MartinEgli/single-skill-template --skill * -a codex --yes
```

## Cursor

```powershell
npx -y skills add MartinEgli/single-skill-template --skill * -a cursor --yes
```

## Windsurf

```powershell
npx -y skills add MartinEgli/single-skill-template --skill * -a windsurf --yes
```

## Cline

```powershell
npx -y skills add MartinEgli/single-skill-template --skill * -a cline --yes
```

## Local Development

Run validation before publishing:

```powershell
npm run validate
npm run test
```

Package:

```powershell
npm run package
```

Output:

```text
dist/example-skill.skill
```
