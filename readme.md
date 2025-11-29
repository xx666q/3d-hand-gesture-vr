# 🌌 3D Hand-Gesture Particle System

> 基于 Three.js 与 MediaPipe 的沉浸式手势粒子交互实验。无需 VR 设备，仅需摄像头即可体验“指尖魔法”。

[![Three.js](https://img.shields.io/badge/Three.js-r128-black)](https://threejs.org/)

## ✨ 项目简介 (Introduction)

这是一个运行在浏览器中的 3D 粒子系统，通过计算机视觉（MediaPipe）识别双手动作。用户可以通过**双手**像操作 VR 界面一样，对粒子模型进行旋转、缩放和打散。

核心体验在于将 2D 的摄像头输入映射为 3D 空间的交互逻辑，配合平滑的阻尼算法，带来类似液体的丝滑操控感。

**[🔴 点击这里查看在线演示 (Live Demo)]
![Demo Preview](nartsuki.online)

## 🎮 交互指南 (Controls)

系统支持 **单手** 与 **双手 (VR模式)** 自动切换。

### 👐 双手模式 (VR Mode) - *推荐*
当摄像头识别到两只手时，自动进入此模式：
* **旋转视角**：双手同时向左/右移动，物体沿 Y 轴旋转。
* **俯仰视角**：双手同时向上/下移动，物体沿 X 轴旋转。
* **粒子爆发**：双手快速**拉开距离**，粒子炸裂扩散；**合拢**则凝聚复原。

### 🖐️ 单手模式 (Single Hand)
* **呼吸控制**：捏合拇指与食指，控制粒子的局部微动与呼吸感。

## 🛠️ 技术栈 (Tech Stack)

* **渲染引擎**: [Three.js](https://threejs.org/) - 处理 18,000+ 粒子的实时渲染与物理运动。
* **视觉识别**: [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) - 实时手部关键点检测（支持多手追踪）。
* **核心算法**:
    * 自定义粒子形状生成器（土星、爱心、螺旋星系等）。
    * 手势坐标到 3D 欧拉角 (Euler Angles) 的平滑映射算法 (Lerp)。

