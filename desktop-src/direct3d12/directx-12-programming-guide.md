---
title: Direct3D 12 程式設計指南
description: Direct3D 12 提供的 API 和平臺可讓應用程式利用配備一或多個 Direct3D 12 相容 Gpu 之電腦的圖形和運算功能。
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: bf6a52b91604d8a9432bf646097e3f31e44967d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/06/2019
ms.locfileid: "104548444"
---
# <a name="direct3d-12-programming-guide"></a>Direct3D 12 程式設計指南

Direct3D 12 提供的 API 和平臺可讓應用程式利用配備一或多個 Direct3D 12 相容 Gpu 之電腦的圖形和運算功能。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [什麼是 Direct3D 12？](what-is-directx-12-.md) | DirectX 12 引進了下一版的 Direct3D，也就是 DirectX 核心的3D 圖形 API。 這個版本的 Direct3D 比之前的版本更快且更有效率。 Direct3D 12 提供更豐富的場景、更多物件、更複雜的效果，以及新式 GPU 硬體的完整使用率。  |
| [Direct3D 12 的新功能](new-releases.md) | 描述最新 SDK 版本所提供的最重要新檔。 |
| [瞭解 Direct3D 12](directx-12-getting-started.md) | 若要撰寫適用于 Windows 10 和 Windows 10 行動裝置版的3D 遊戲和應用程式，您必須瞭解 Direct3D 12 技術的基本概念，以及如何準備在您的遊戲和應用程式中使用它。 |
| [在 Direct3D 12 中提交工作](command-queues-and-command-lists.md) | 為了改善 Direct3D 應用程式的 CPU 效率，Direct3D 12 不再支援與裝置相關聯的立即內容。 相反地，應用程式會記錄並提交包含繪圖和資源管理呼叫的 *命令清單*。 您可以從多個執行緒將這些命令清單提交至一或多個命令佇列，以管理命令的執行。 這項基本變更可讓應用程式預先計算轉譯工作以供稍後重複使用，以增加單一執行緒的效率，並且藉由將轉譯工作分散到多個執行緒來利用多核心系統。  |
| [Direct3D 12 中的資源繫結](resource-binding.md) | 系結是將資源物件連結至圖形管線著色器的程式。  |
| [Direct3D 12 中的記憶體管理](memory-management.md) | 移至 D3D12 牽涉到適當的同步處理和管理記憶體存放區。 管理記憶體存放區表示需要進行更多的同步處理。 本節涵蓋記憶體管理原則，以及在堆積和緩衝區內的子分配。  |
| [多個介面卡系統](multi-engine.md) | 說明在安裝多個介面卡的系統中，Direct3D 12 的支援，其中涵蓋了應用程式明確以多個 GPU 介面卡為目標的案例，以及驅動程式會代表您的應用程式隱含使用多個 GPU 介面卡的案例。 |
| [多引擎同步處理](user-mode-heap-synchronization.md) | 本主題討論如何同步處理在大部分新式 Gpu 中找到之多個獨立引擎的存取。 |
| [轉譯](rendering.md) | 本章節包含 Direct3D 12 (和 Direct3D 11.3) 的新轉譯功能的相關資訊。 |
| [計數器、查詢和效能測量](performance-measurement.md) | 下列各節說明在效能測試和改進（例如查詢、計數器、計時和 predication）中使用的功能。 |
| [使用 Direct3D 11、Direct3D 10 和 Direct2D](direct3d-12-interop.md) | 本節涵蓋使用舊版 Direct3D 和 Direct2D 的 interop 技術、Direct3D 11on12 API，以及從 Direct3D 11 到 Direct3D 12 的移植指導方針。 |
| [工作範例](working-samples.md) | 可供下載的工作範例可供下載，以顯示一些 Direct3D 12 功能的使用方式。 |
| [D3D12 程式碼逐步解說-解說](d3d12-code-walk-throughs.md) | 本節提供範例案例的程式碼。 許多解說都提供詳細資料，說明如何將程式碼新增至基本範例，以避免針對每個案例重複基本的元件程式碼。 |
| [使用 Direct3D 12 進行偵錯工具和診斷](understanding-the-d3d12-debug-layer.md) | 包含的主題說明如何使用以 GPU 為基礎的驗證來充分利用 Direct3D 12 Debug 層 (GBV) ，以及如何使用裝置移除擴充的資料 (DR) 。 |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 圖形](direct3d-12-graphics.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
* [DirectX advanced learning 影片教學課程](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
