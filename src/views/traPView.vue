<template>
  <!--<h1>{{ message }}</h1>
  <button @click="showMessage">ボタンを押してね</button>-->
  <div class="text-box">
    <h2>traQおすすめのチャンネル</h2>
    <br/>
    <p>
      多分このチャンネルには通知つけておいた方がいいよってチャンネルを挙げていきます
    </p>
    <table class="center-table">
      <thead>
        <tr>
          <th>#gps/ogiri</th>
          <th>みんなが大喜利をしていく場所です。センスが爆発してておもろい</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>#gps/ogiri</td>
          <td>みんなが大喜利をしていく場所です。センスが爆発してておもろい</td>
        </tr>
        <tr>
          <td>#gps/onair</td>
          <td>イベントごとなどがあれば大体ここに書き込まれます。</td>
        </tr>
        <tr>
          <td>#times/24/zoi_dayo</td>
          <td>現代表のTimes.フランクなのでとりあえず突撃していいんじゃね（？）</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
h2 {
  color: orange;
}
h4 {
  color: blueviolet;
}

.header {
  position: fixed; /* 画面の最上部に固定 */
  top: 0; /* 上端に配置 */
  left: 0; /* 左端に配置 */
  width: 100%; /* 横幅いっぱいに広げる */
  z-index: 1000; /* 他の要素より前面に表示 */

  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem 4rem;
  gap: 2rem;
  flex-wrap: wrap; /* 狭い画面で折り返し */
  background-color: #fee9c0; /* 任意：背景色 */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* optional：少し影をつける */
}

.header-left {
  display: flex;
  justify-content: flex-start; /* タイトルは左寄せ */
  flex: 1; /* 左側を広げて中央寄せっぽく */
}

.header-title {
  margin: 0;
  font-size: 2rem;
  margin-left: 1rem;
}

.header-right {
  display: flex; /* ここが必須 */
  align-items: center;
  gap: 1rem; /* 間隔を広げたい */
}

.home-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  text-decoration: none;
  color: inherit;
  margin-right: 1rem;
}

.home-icon {
  width: 24px;
  height: 24px;
  display: inline-block; /* ブロックではなくインラインに */
}

main {
  padding-top: 80px; /* ヘッダーの高さ分余白を空ける */
}

.textCenterizer {
  text-align: center;
  margin-top: 5vh;
  margin-bottom: 10vh;
}

.text-box {
  width: 85%; /* 横幅を画面の85%に設定（広げました） */
  max-width: 1100px; /* 余裕があれば最大幅も設定 */
  margin: 2rem auto; /* 左右中央揃え、上下に余白 */
  padding: 1.5rem; /* 内側の余白 */
  background-color: #f9f9f9; /* 背景色（任意） */
  border-radius: 10px; /* 角を丸める */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* 影をつける（任意） */
  text-align: left; /* テキストは左揃え（変更可能） */
  line-height: 1.6; /* 行間を広げて読みやすく */
}

.center-table {
  margin: 0 auto; /* 左右中央寄せ */
  border-collapse: collapse; /* 枠線をまとめる */
  width: 78%; /* 任意で表の横幅を指定 */
  text-align: center; /* セル内の文字を中央揃え */
}

.center-table th,
.center-table td {
  border: 1px solid #ccc; /* 枠線 */
  padding: 0.5rem;
}

/* ここからボタン関連 */
.button-grid {
  display: flex;
  gap: 2rem; /* ボタン間の間隔 */
  justify-content: center; /* 中央寄せ */
  align-items: center;
  margin-bottom: 5vh;
}

.category-button {
  width: 200px; /* 正方形の大きさ */
  height: 200px;
  display: flex;
  flex-direction: column; /* 画像と文字を縦並び */
  justify-content: center;
  align-items: center;
  background-color: #f0f0f0; /* 背景色 */
  border-radius: 12px; /* 角丸 */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

/* ホバー時のエフェクト */
.category-button:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
}

.button-image {
  width: 80%;
  height: auto;
  border-radius: 8px;
  margin-bottom: 0.5rem;
}

.button-text {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
}

a {
  text-decoration: none;
}
/* ここまでボタン関連 */

.buttons {
  margin-top: 15vh;
}

h2 {
  text-align: center;
}
</style>

<script setup lang="ts">
import { ref } from "vue";

const message = ref("");

const showMessage = () => {
  message.value = "Hello World!";
};
</script>
