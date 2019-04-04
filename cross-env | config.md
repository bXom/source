# cross-env 与 config

1. 在papackage.json的scripts中声明

    ```json
    "scripts": {
        "dev": "cross-env NODE_ENV=development PORT=80 ... index.js",
        "test": "cross-env NODE_ENV=test PORT=8081 ... index.js",
    },
    ```

2. 可跨平台使用的环境变量

    ```javascript
    const env = process.env.NODE_ENV;
    console.log('env:', env);
    // env:development
    const port = process.env.PORT;
    console.log('port:', port);
    // port:8080
    ```

3. 根据环境变量自动加载不同的config文件

    ```JavaScript
    //
    // ./config
    //      development.js
    //      test.js
    //
    // 1. npm run dev
    // 加载 development.js
    //
    // 2. npm run test
    // 加载 test.js
    ```