# 使用

## Node.js

1. 在papackage.json的scripts中声明

    ```json
    "scripts": {
        "dev": "cross-env NODE_ENV=development ... index.js"
    },
    ```

2. 可跨平台使用该变量

    ```javascript
    const env = process.env.NODE_ENV;
    console.log('env:', env);
    // env:development
    ```