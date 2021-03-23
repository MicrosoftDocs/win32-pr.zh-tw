---
title: 在 Direct3D 12 中提交工作
description: 為了改善 Direct3D 應用程式的 CPU 效率，Direct3D 12 不再支援與裝置相關聯的立即內容。
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103867"
---
# <a name="work-submission-in-direct3d-12"></a>在 Direct3D 12 中提交工作

為了改善 Direct3D 應用程式的 CPU 效率，從第12版開始，Direct3D 不再支援與裝置相關聯的立即內容。 相反地，您的應用程式會記錄並提交包含繪圖和資源管理呼叫的 *命令清單*。 您可以從多個執行緒將這些命令清單提交至一或多個命令佇列，以管理命令的執行。 這項基本變更可讓您的應用程式預先計算轉譯工作以供稍後重複使用，以增加單一執行緒的效率，並且透過將轉譯工作分散到多個執行緒來利用多核心系統。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [命令佇列和命令清單的設計原理](design-philosophy-of-command-queues-and-command-lists.md) | 啟用轉譯工作和多執行緒調整的目標，需要對 Direct3D 應用程式如何將轉譯工作提交至 GPU 的基本變更。 |
| [建立和記錄命令清單和組合](recording-command-lists-and-bundles.md) | 本主題說明如何在 Direct3D 12 應用程式中錄製命令清單和組合。 命令清單和套件組合都可讓應用程式記錄繪圖或狀態變更呼叫，以供稍後在圖形處理單元上執行 (GPU) 。 |
| [執行和同步處理命令清單](executing-and-synchronizing-command-lists.md) | 在 Microsoft Direct3D 12 中，不再有舊版的立即模式。 相反地，應用程式會建立命令清單和套件組合，然後記錄 GPU 命令集。 命令佇列可用來提交要執行的命令清單。 此模型可讓開發人員更充分掌控 GPU 和 CPU 的使用效率。 |
| [管理 Direct3D 12 中的圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md) | 本主題說明如何在 Direct3D 12 中設定圖形管線狀態。 |
| [在 Direct3D 12 中使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | 為了降低整體 CPU 使用率並啟用驅動程式多執行緒處理和預先處理，Direct3D 12 會將每個資源狀態管理的責任從圖形驅動程式移至應用程式。 |
| [使用 Direct3D 12 的管線和著色器](pipelines-and-shaders-with-directx-12.md) | 相較于上一代圖形程式設計介面，Direct3D 12 程式化管線可大幅提高轉譯效能。 |
| [可變速率陰影 (VRS) ](vrs.md) | 變動率陰影 &mdash; 或粗圖元陰影 &mdash; 是一種機制，可讓您以不同于轉譯影像的速率配置轉譯效能/電源。 |
| [轉譯階段](direct3d-12-render-passes.md) | 轉譯傳遞功能可減少進出晶片記憶體的記憶體流量，協助您的轉譯器改善 GPU 效率;它的做法是讓您的應用程式更清楚地識別資源轉譯順序需求和資料相依性。 |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 程式設計指南](directx-12-programming-guide.md)
