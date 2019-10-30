npx react-native init nativetests

yarn add @testing-library/react-native -D <br/>
no packagejson substituir "preset": "react-native" por "preset": "@testing-library/react-native" <br/>
"jest": {
    "preset": "@testing-library/react-native",
    "setupFilesAfterEnv": [
      "@testing-library/jest-native/extend-expect"
    ],
    "testMatch": [
      "**/__tests__/**/*.test.js"
    ],
    "collectCoverageFrom": [
      "!src/services/api.js"
    ],
    "coverageDirectory": "__tests__/coverage",
    "moduleNameMapper": {
      "^~/(.*)": "<rootDir>/src/$1"
    }
  }

yarn add @types/jest -D //para adicioanr o intellisense do jest <br/>

yarn add @testing-library/jest-native -D //lib para extender as expectations do jest para o react-native - add o toHaveProp por exemplo <br/>
adicionar ao package.json: <br/>
"setupFilesAfterEnv": [
  "@testing-library/jest-native/extend-expect"
],

yarn test --watchAll //para rodar o teste o tempo todo ouvindo todos os testes --watch funciona se tiver o git para rodar somente os que foram alterados



