---
# 使用seriph主題
theme: seriph
# 設定背景
background: https://cover.sli.dev
# 簡報資訊
title: AI Agent：從被動到自主的智慧實體
info: |
  ## AI Agent 簡報
  2025/04/29 孫既仁
# 文字置中
class: text-center
# 啟用繪圖功能
drawings:
  persist: false
# 幻燈片過渡效果
transition: fade-out
# 啟用MDC語法
mdc: true
---

# <span class="text-teal-500">AI Agent</span>

## 從被動到自主的智慧實體

<br/>
2025.04.29 孫既仁

<div @click="$slidev.nav.next" class="mt-12 py-1 hover:text-teal-300 transition-colors duration-300">
  點擊 空白鍵 進入下一頁 <carbon:arrow-right />
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/sjenwork" target="_blank" alt="GitHub" title="我的GitHub"
    class="text-xl slidev-icon-btn opacity-75 !border-none !hover:text-white !hover:opacity-100 transition-opacity duration-300">
    <carbon-logo-github />
  </a>
</div>

<!--
-->

---

# 內容涵蓋

<div class="grid grid-cols-1 gap-6 mt-12">
<div v-click>

### <carbon-ai-results class="inline-block mr-2" /> AI 與 Agent 的概念與範例

</div>
<div v-click>

### <carbon-chart-line-data class="inline-block mr-2" /> 結合 LLMs 發展時間軸，講解 AI Agent 的發展脈絡

</div>
<div v-click>

### <carbon-code class="inline-block mr-2" /> 實作簡單的 AI Agent 範例

</div>
</div>

---

## transition: fade-out

# 什麼是 AI？

<div class="grid grid-cols-1 gap-4 mt-6">
<div v-click>

## 廣義的定義

<div class="flex items-start gap-4 my-4">
  <div class="text-3xl"><carbon:machine-learning /></div>
  <div>具備<span class="text-blue-400 font-bold">模仿、展現甚至超越</span>人類智慧行為的系統或過程，特別是那些能夠執行需要「思考」、「學習」而非僅僅遵循固定規則的任務。</div>
</div>

</div>

<div v-click>

## 這包含了

<div class="grid grid-cols-2 gap-4 mt-4">
  <div class="flex items-start gap-2">
    <carbon-text-mining class="mt-1" />
    <span><strong>大型語言模型 (LLMs)：</strong><br/>理解、生成、甚至初步的推理人類語言</span>
  </div>
  <div class="flex items-start gap-2">
    <carbon-image-medical class="mt-1" />
    <span><strong>圖像辨識：</strong><br/>例如醫療影像分析（識別惡性腫瘤）</span>
  </div>
  <div class="flex items-start gap-2">
    <carbon-Image-search class="mt-1" />
    <span><strong>影像行為分析：</strong><br/>例如監控畫面中的異常行為辨識</span>
  </div>
  <div class="flex items-start gap-2">
    <carbon-game-console class="mt-1" />
    <span><strong>專業領域 AI：</strong><br/>如 AlphaGo（棋類）、特定領域的預測模型</span>
  </div>
  <div class="flex items-start gap-2 col-span-2">
    <carbon-car class="mt-1" />
    <span><strong>複雜決策系統：</strong><br/>如自動駕駛技術</span>
  </div>
</div>

</div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
本頁講解AI的基本定義和範圍，是整個演講的基礎
-->

---

## transition: fade-out

---

# 什麼是 Agent (代理人)？

<div v-click>
  <span class="text-2xl font-medium text-teal-600 dark:text-teal-400">Agent vs. Proxy</span>
</div>

<div class="grid grid-cols-1 gap-4 mt-6">
<div v-click>

## Agent

<div class="flex items-start gap-4 my-4">
  <div class="text-3xl"><carbon-bot /></div>
  <div>
    一個具有<span class="text-green-400 font-bold">自主性</span>的實體，能夠<span class="text-green-400 font-bold">感知</span>其所處的環境，並基於感知和內部的決策邏輯<span class="text-green-400 font-bold">採取行動</span>，以達成某個目標或維持某種狀態。
    <div class="pl-4 mt-2 text-sm opacity-75">
      <carbon-arrow-right class="inline" /> 想像：電影《MIB星際戰警》中的 Agent K 或 Agent J，他們主動調查、應對環境變化、獨立採取行動。
    </div>
  </div>
</div>

</div>

<div v-click>

## Proxy

<div class="flex items-start gap-4 my-4">
  <div class="text-3xl"><carbon-delivery /></div>
  <div>
    一個相對<span class="text-red-400 font-bold">被動</span>的實體。它接收請求，並依據預設的規則將請求轉發出去。它本身通常不進行複雜的決策或主動感知環境變化來調整行為。
    <div class="pl-4 mt-2 text-sm opacity-75">
      <carbon-arrow-right class="inline" /> 想像：系統架構中的反向代理 (Reverse Proxy)，只負責將外部請求轉發給後端的伺服器，自己不處理業務邏輯。
    </div>
  </div>
  </div>

</div>

</div>

---
## transition: fade-out
---

# 什麼是 Agent (代理人)？

<div>
<span class="text-2xl font-medium text-teal-600 dark:text-teal-400">Agent vs. Proxy</span>
</div>

<div v-click>

<div style="height: 30px;"></div>

## 圖解比較

<div class="flex justify-center items-center gap-16 mt-10">
  <div class="text-center">
    <div class="flex justify-center">
      <carbon-mail-all class="text-6xl text-blue-400" />
    </div>
    <div class="mt-2 font-bold">Proxy</div>
    <div class="text-sm opacity-75">像個郵差，只管轉發</div>
  </div>
  
  <div class="text-center">
    <div class="flex justify-center">
      <carbon-bot class="text-6xl text-green-400" />
    </div>
    <div class="mt-2 font-bold">Agent</div>
    <div class="text-sm opacity-75">會思考、會觀察、會行動的小機器人</div>
  </div>
</div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
這頁介紹Agent的概念，並對比Proxy更加被動的特性，通過圖示直觀地表現兩者區別
-->

---
## transition: fade-out
---

# 什麼是 AI Agent？

<div class="grid grid-cols-1 gap-4 mt-6">

<div v-click>

  <div>
  <span class="text-2xl font-medium text-teal-600 dark:text-teal-400">定義：</span>
  </div>

  <div class="flex items-start gap-4 my-4">
    <div class="text-3xl"><carbon-machine-learning-model /></div>
    <div>
      是 Agent 的一種形式，但其核心決策能力由<span class="text-purple-500 font-bold">人工智慧</span>來賦予。它不僅能感知和行動，更能運用 AI 的智慧來進行更複雜的<span class="text-purple-500 font-bold">思考</span>、<span class="text-purple-500 font-bold">學習</span>、<span class="text-purple-500 font-bold">規劃</span>與<span class="text-purple-500 font-bold">決策</span>，以更有效或智慧的方式達成目標。
      <div class="pl-4 mt-2 text-sm opacity-75">
        <carbon-arrow-right class="inline" /> 可以理解為：Agent 的<strong>執行力</strong> 結合了 AI 的<strong>智慧決策力</strong>。
      </div>
    </div>
  </div>

  </div>
</div>

<div v-click>


  <div>
  <span class="text-2xl font-medium text-teal-600 dark:text-teal-400">從簡單到複雜的 Agent / AI Agent 演進：</span>
  </div>

<div class="grid grid-cols-3 gap-4 mt-4">
  <div class="border border-gray-200 dark:border-gray-700 p-3 rounded-lg">
    <div class="flex justify-center">
      <carbon-temperature-hot class="text-4xl text-orange-400" />
    </div>
    <div class="mt-2 font-bold text-center mb-2">簡單 Agent</div>
    <div class="text-sm">
      <strong>恆溫器：</strong><br/>
      <div class="grid grid-cols-5 gap-1 mt-2">
        <div class="col-span-1 text-cyan-500"><carbon-view /></div>
        <div class="col-span-4">偵測室內溫度</div>
        <div class="col-span-1 text-amber-500"><carbon-Task-asset-view /></div>
        <div class="col-span-4">基於規則的簡單決策</div>
        <div class="col-span-1 text-green-500"><carbon-run /></div>
        <div class="col-span-4">控制空調開關</div>
      </div>
    </div>
  </div>  


  <div class="border border-gray-200 dark:border-gray-700 p-3 rounded-lg">
    <div class="flex justify-center">
      <carbon-email class="text-4xl text-blue-400" />
    </div>
    <div class="mt-2 font-bold text-center mb-2">模型增強型 Agent</div>
    <div class="text-sm">
      <strong>智能垃圾郵件篩選器：</strong><br/>
      <div class="grid grid-cols-5 gap-1 mt-2">
        <div class="col-span-1 text-cyan-500"><carbon-view /></div>
        <div class="col-span-4">讀取郵件內容、發送者等</div>
        <div class="col-span-1 text-amber-500"><carbon-machine-learning /></div>
        <div class="col-span-4">運用ML模型判斷郵件類型</div>
        <div class="col-span-1 text-green-500"><carbon-run /></div>
        <div class="col-span-4">移至收件匣或垃圾郵件夾</div>
      </div>
    </div>
  </div>
  
  <div class="border border-gray-200 dark:border-gray-700 p-3 rounded-lg">
    <div class="flex justify-center">
      <carbon-car class="text-4xl text-green-400" />
    </div>
    <div class="mt-2 font-bold text-center mb-2">高級 AI Agent</div>
    <div class="text-sm">
      <strong>特斯拉自動駕駛：</strong><br/>
      <div class="grid grid-cols-5 gap-1 mt-2">
        <div class="col-span-1 text-cyan-500"><carbon-view /></div>
        <div class="col-span-4">多感測器實時觀察複雜環境</div>
        <div class="col-span-1 text-amber-500"><carbon-ai-status /></div>
        <div class="col-span-4">基於複雜AI模型做實時決策</div>
        <div class="col-span-1 text-green-500"><carbon-run /></div>
        <div class="col-span-4">精確控制油門、煞車、方向盤</div>
      </div>
    </div>
  </div>  
</div>  

</div>

---
## transition: fade-out
---

# 什麼是 AI Agent？


<div v-click>

  <div class="mt-6">
  <span class="text-2xl font-medium text-teal-600 dark:text-teal-400">生活中的例子：</span>
  </div>

  <div style="height: 100px;"></div>

  <div class="grid grid-cols-2 gap-8 mt-4">
    <div class="flex items-center gap-4">
      <carbon-voice-activate class="text-4xl text-blue-400" />
      <div>
        <div class="font-bold">智慧語音助理</div>
        <div class="text-sm">Siri, Hey Google, 小愛同學</div>
      </div>
    </div>
    <div class="flex items-center gap-4">
      <carbon-home class="text-4xl text-green-400" />
      <div>
        <div class="font-IoT-connect">智能家居中心</div>
        <div class="text-sm">Google Nest, Amazon Echo</div>
      </div>
    </div>
  </div>
</div>