# NEUMA · 脑波音乐实验室

使用 Web Audio 原生 FM Pad 与一阶马尔可夫链生成慢速音乐的纯前端 Demo。

## 使用
选择“模拟脑波”，点击“开启声音”；也可手动调整专注度和放松度。

## 数据接口
选择“实时接入”后，同页调用 `window.NeumaEEG.update({attention:55, relaxation:70, signalQuality:100})`，或连接发送同格式 JSON 的 WebSocket。两个指标为0–100，质量可选且越高越好。HTTPS 页面需 wss://。

原始EEG采集与指标计算由第一部分负责；本项目的音乐参数映射为创作规则，尚未验证专注或情绪改善效果。

数据在浏览器内存处理，导出记录为 JSON 指标/音符事件日志。
