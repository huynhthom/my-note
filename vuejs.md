# Create a new project with Vuejs
- With Vuejs
>npm init vue@latest
- With Vue-CLI
>vue creata `name-project`

## Config Format vue
- F1 -> Find `Preferences: Open Default Settings (JSON)`
- Add code
```
    "vetur.validation.template": false,
    "vetur.validation.script": false,
    "vetur.validation.style": false,
```

# Lifecycle Hooks
https://vuejs.org/guide/essentials/lifecycle.html

# Note
- `event.prevent`: Hủy bỏ event mặc định của element 
Ví dụ: click `submit`, page sẽ reload. Nếu click.prevent `submit` thì page sẽ không reload.
- `debounce`: set time delay