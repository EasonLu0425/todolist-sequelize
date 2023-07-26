#todolist-sequelize

## getting Start

- 請先用 git clone 下載檔案: gitclone: https://github.com/EasonLu0425/todolist-sequelize.git
- 使用終端機進入檔案資料夾，並且於終端機輸入: `$ npm install`
- 由於本專案有使用 Facebook 登入功能，請於專案根目錄建立`.env`檔案，並且加入
  FACEBOOK_ID=SKIP
  FACEBOOK_SECRET=SKIP
  FACEBOOK_CALLBACK=http://localhost:3000/auth/facebook/callback

- 建立種子資料，請於終端機輸入`npx sequelize db:seed:all`，種子資料就會一次建立完成。
  - 會建立一個使用者，帳號:root@example.com 密碼:12345678。
  - 會在此帳號底下建立隨機 10 個 todo item。

## 產品功能

- 註冊帳號: 可以註冊一個帳號，密碼會做亂數打散後才存到資料庫中。會確認輸入資訊是否正確才會成功註冊。
- 登入驗證: 驗證登入資訊是否正確輸入，正確則進入主頁面，錯則會阻擋進入。
- 登出機制: 可登出帳號，登出後須重新登入才可再次使用。
- 可建立、查閱、刪除、修改 todo 清單，自己只能看到自己的內容，保有隱私性。
