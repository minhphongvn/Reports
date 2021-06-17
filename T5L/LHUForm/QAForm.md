# MỘT SỐ THÔNG TIN VỀ COMPONENT 

## Cài đặt

### sử dụng NPM hoặc YARN

```bash
yarn add fpform

npm i -S fpform
```

### sử dụng CDN
```html

<script src="https://unpkg.com/fpform@1.x/dist/lhuform.min.js"></script>

```

[Live Demo](https://minhphongvn.github.io/Reports/T5L/)

## VueJS 2.0
Cách sử dụng component:

### Sử dụng với `.vue` file:

``` html
    <template>
      <div id="app">
        ...
        <QAForm v-model="template"/>
        ...
      </div>
    </template>
```
``` js
  import LhuForm from 'fpform'
  ...
  export default {
        components: {
            LhuForm,
        },
  ...
```

### Sử dụng với  `CDN `:
``` html
<!DOCTYPE html>
<html>
<head>
  <link href="https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900" rel="stylesheet">
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, minimal-ui">
</head>
<body>
  <div id="app">
    <Lhuform v-model="template"></Lhuform>
  </div>
  <script src="https://cdn.jsdelivr.net/npm/vue@2.x/dist/vue.js"></script>
  <script src="https://unpkg.com/fpform@1.x/dist/lhuform.min.js"></script>
  <script>
    new Vue({
      el: '#app',
      components: { Lhuform }
      data: ()=>({
        template: {...}
      })
    })
  </script>
</body>
</html>
```

### Props
#### value
Type: `Object`<br>
Required: `true`<br>
Default: 
```json
{
  "templateID": "cuu-sv-demo2",
  "logo_org": "https://lhu.edu.vn/ViewPage/LHUVN/_default/image/truong_dai_hoc_lac_hong_logo.png",
  "name_org": "Trường Đại học Lạc Hồng",
  "url_finishRedirect": "https://lhu.edu.vn",
  "Title": "TÊN PHIẾU KHẢO SÁT",
  "Des": "Xin chào anh/chị",
  "url_login": "",
  "url_template": "",
  "Part": [
    {
      "Name": "TÊN PHẦN",
      "Des": "Mô tả",
      "Question": []
    }
  ]
}
```

#### width
Type: `String`<br>
Required: `false`<br>
Default: `100%`
Là chiều rộng của component, lưu ý component chỉ khuyên dùng trên màn hình rộng  nên sẽ không hỗ trợ responsive. 

#### height
Type: `String`<br>
Required: `false`<br>
Default: `98vh`
Là chiều cao của component.
