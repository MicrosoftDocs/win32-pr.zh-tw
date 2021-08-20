---
title: Direct2D 程式設計指南
description: 本節包含描述如何使用 Direct2D API 的概念程式設計主題。
ms.assetid: 428cc2f2-524a-4330-8916-7fa3c8c7c9b7
keywords:
- Direct2D，程式設計手冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef71662cc5cce02379fa0586630208edf1b82e37acaa289de6afc8d69d029c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002440"
---
# <a name="direct2d-programming-guide"></a>Direct2D 程式設計指南

本節包含描述如何使用 Direct2D API 的概念程式設計主題。



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct2D API 概觀](the-direct2d-api.md)<br/>                                          | 提供 Direct2D 物件模型的總覽。<br/>                                                                                                                                                                                                                                                                                                   |
| [Direct2D 和高 DPI](direct2d-and-high-dpi.md)<br/>                                     | 描述 Direct2D 如何容納高 DPI 顯示器。<br/>                                                                                                                                                                                                                                                                                                |
| [Direct2D 錯誤處理原則](direct2d-error-handling-policies.md)<br/>               | 描述 Direct2D 中的錯誤處理原則。<br/>                                                                                                                                                                                                                                                                                                   |
| [裝置和裝置內容](devices-and-device-contexts.md)<br/>                         |                                                                                                                                                                                                                                                                                                                                                                 |
| [改善 Direct2D 應用程式的效能](improving-direct2d-performance.md)<br/>       | 描述改善 Direct2D 效能的技術。<br/>                                                                                                                                                                                                                                                                                             |
| [圖層總覽](direct2d-layers-overview.md)<br/>                                        | 描述 Direct2D 圖層的基本概念。<br/>                                                                                                                                                                                                                                                                                                             |
| [列印和命令清單](printing-and-command-lists.md)<br/>                           | [Direct2D](./direct2d-portal.md) [**列印控制項**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)是 Windows 8 之 Direct2D 模組中的新元件。 此元件可讓 Direct2D apps 重複使用其 Direct2D 繪圖呼叫 (的狀態變更和轉譯基本) ，以提供類似您在螢幕上所看到的列印結果。 <br/> |
| [多執行緒 Direct2D 應用程式](multi-threaded-direct2d-apps.md)<br/>                        | 描述建立多執行緒 Direct2D 應用程式的最佳做法。<br/>                                                                                                                                                                                                                                                                                   |
| [分析 DirectX 應用程式](profiling-directx-applications.md)<br/>                   | 示範如何使用隨附于 Windows 效能工具組一部分的 **XPerf** 和 **GPUView** 工具，測量 [DirectX](/previous-versions/windows/apps/jj262109(v=win.10))應用程式的一些最重要效能時間度量。 <br/>                                                                                                |
| [區塊壓縮](block-compression.md)<br/>                                             | 描述區塊壓縮的運作方式，以及如何在 WIC 和 Direct2D 中使用它。<br/>                                                                                                                                                                                                                                                                         |
| [影響](effects-overview.md)<br/>                                                        | Direct2D 效果的總覽。<br/>                                                                                                                                                                                                                                                                                                                     |
| [筆刷](brushes.md)<br/>                                                                 | 描述如何使用 Direct2D 筆刷，也就是您用來繪製填滿和外框的物件。<br/>                                                                                                                                                                                                                                                                  |
| [幾何](geometries.md)<br/>                                                           | 描述如何使用 Direct2D 幾何來代表、操作及分析圖案。 <br/>                                                                                                                                                                                                                                                              |
| [互通性](interoperability.md)<br/>                                               | 描述 Direct2D 如何與其他系統交互操作。<br/>                                                                                                                                                                                                                                                                                             |
| [轉換](transforms.md)<br/>                                                           | 描述會將的基本概念，以及如何將各種轉換套用至物件。<br/>                                                                                                                                                                                                                                                                    |
| [操作說明主題](how-to-topics.md)<br/>                                                     | 提供範例，示範如何使用 Direct2D 完成各種工作。<br/>                                                                                                                                                                                                                                                                      |
| [使用 Direct2D 和 DirectWrite 的文字轉譯](direct2d-and-directwrite.md)<br/>           | 與其他 api （例如[GDI](/windows/desktop/gdi/windows-gdi)、GDI+ 或 WPF）不同的是， [Direct2D](./direct2d-portal.md)可與另一個 api （ [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)）交互操作，以操作和轉譯文字。 本主題說明這些個別元件的優點和互通性。 <br/>                                          |
| [不透明度遮罩概觀](opacity-masks-overview.md)<br/>                                   | 描述如何使用點陣圖和筆刷來定義不透明度遮罩。<br/>                                                                                                                                                                                                                                                                                    |
| [資源總覽](resources-and-resource-domains.md)<br/>                               | 描述 Direct2D 資源，以及如何共用這些資源。<br/>                                                                                                                                                                                                                                                                                             |
| [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)<br/> | 描述每個呈現目標型別所支援的像素格式和 Alpha 模式。<br/>                                                                                                                                                                                                                                                                    |
| [使用 Direct2D 進行 Server-Side 轉譯](server-side-rendering-overview.md)<br/>         | 描述如何使用 Direct2D 進行伺服器端轉譯。<br/>                                                                                                                                                                                                                                                                                                  |
| [轉譯目標總覽](render-targets-overview.md)<br/>                                 | 描述不同類型的 Direct2D 轉譯目標，以及如何使用它們。<br/>                                                                                                                                                                                                                                                                        |
| [相容的 A8 轉譯目標總覽](/windows/desktop/Direct2D/compatible-a8-rendertargets)<br/>          | 描述相容 A8 轉譯目標的基本概念，並提供示範如何使用它們的範例。<br/>                                                                                                                                                                                                                                                   |



 

 

