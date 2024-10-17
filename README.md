# eslint-prettier-react

# 1 - Instalar os ESLint

```
npm install eslint --save-dev
```

```
npx install-peerdeps --dev eslint-config-airbnb
```

```
npx eslint --init
```

# 2 - Integrar com Prettier

```
npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier -D
```

# 3 - .eslintrc

```
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": ["plugin:react/recommended", "airbnb", "prettier"],
    "overrides": [],
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "plugins": ["react"],
    "rules": {
        "react/jsx-filename-extension": [
            "warn",
            {
                "extensions": [".js", ".jsx"]
            }
        ],
        "react/react-in-jsx-scope": "off",
        "comma-dangle": "off"
    }
}
```

# 4 - .prettierrc

```
{
    "arrowParens": "always",
    "bracketSpacing": true,
    "jsxBracketSameLine": false,
    "jsxSingleQuote": false,
    "printWidth": 100,
    "proseWrap": "always",
    "quoteProps": "as-needed",
    "semi": true,
    "singleQuote": true,
    "tabWidth": 2,
    "trailingComma": "es5",
    "useTabs": false,
    "endOfLine": "auto",
    "overrides": [
  ]
}

```

# 5 - Pasta .vscode (extesions.json, settings.json )

## extesions.sjon
```
{
    "recommendations": [
      "esbenp.prettier-vscode",
      "dbaeumer.vscode-eslint",
      "streetsidesoftware.code-spell-checker",
      "streetsidesoftware.code-spell-checker-portuguese-brazilian"
    ]
}
```
## settings.json

```
{
    "[javascriptreact]": {
      "editor.codeActionsOnSave": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "source.organizeImports": "explicit"
      }
    },
    "editor.formatOnSave": true,
    "cSpell.enableFiletypes": ["javascript"],
    "cSpell.language": "en,pt,pt_BR"
  }

```
