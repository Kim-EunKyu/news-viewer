# News Viewer

## Languages and Frameworks Used:

- [ReactJs](https://reactjs.org/)

## What is this?

ReactJs를 이용하여 api를 이용하여 News Viewer 앱을 만들었습니다.

## 실행 방법

```
npm install
```

node_moduels를 설치 후, [NewsAPI](https://newsapi.org/)에 접속합니다. 가입을 하고 api키를 발급받아 다음 NewsList.js의 해당 부분을 수정합니다.

```
const query = category === "all" ? "" : `&category=${category}`;
const response = await axios.get(`
    https://newsapi.org/v2/top-headlines? country=kr${query}&apiKey=[YOUR-APIKEY]`);
setArticles(response.data.articles);
```

[YOUR-APIKEY] 부분에 자신의 apikey를 삽입한 후 npm start를 통해 실행 할 수 있습니다.

### 주요기능

1.  카테고리별 뉴스 보기 가능
