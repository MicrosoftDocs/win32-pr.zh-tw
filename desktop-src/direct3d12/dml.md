---
title: Direct Machine Learning (DirectML)
description: 直接機器學習 (DirectML) 是適用于機器學習的低層級 API。 它具有 DirectX 12 樣式的熟悉 (原生C++，nano-COM) 程式設計介面和工作流程。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103856"
---
# <a name="direct-machine-learning-directml"></a>Direct Machine Learning (DirectML)

直接機器學習 (DirectML) 是適用于機器學習的低層級 API。 它具有 DirectX 12 樣式的熟悉 (原生C++，nano-COM) 程式設計介面和工作流程。 您可以將機器學習推斷工作負載整合到您的遊戲、引擎、中介軟體、後端或其他應用程式中。 所有 DirectX 12 相容硬體都支援 DirectML。

DirectML 是在 Windows 10 1903 版和對應版本的 Windows SDK 中引進。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [DirectML 簡介](dml-intro.md) | 直接機器學習 (DirectML) 是適用于機器學習 (ML) 的低層級 API。 |
| [在 DirectML 中繫結](dml-binding.md) | 在 DirectML 中 *，系* 結指的是在初始化和執行機器學習運算子期間，要用於 GPU 的管線附加資源。 例如，這些資源可以是輸入和輸出張量，以及操作員需要的任何暫存或持續性資源。 |
| [DirectML 中的 UAV 障礙和資源狀態阻礙](dml-barriers.md) | 描述阻礙的正確性優點，以及如何在 DirectML 中使用它們。 |
| [使用進展來表示填補和記憶體版面配置](dml-strides.md) | DirectML 張量是由稱為 *大小* 的屬性和 *tensor 的進展* 所描述。 |
| [資源存留期和同步處理](dml-resource-lifetime.md) | 為了避免未定義的行為，您的 DirectML 應用程式必須正確地管理 CPU 與 GPU 之間的物件存留期和同步處理。 |
| [使用 DirectML debug layer](dml-debug-layer.md) | DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。 |
| [處理錯誤和裝置移除](dml-errors.md) | 本主題討論如何將 DirectML 裝置移除和其他錯誤情況進行調試。 |
| [DirectML helper 函式](dml-helper-functions.md) | 基本 DirectML helper 函數的程式代碼清單。 |
| [DirectML 範例應用程式](dml-min-app.md) | DirectML 範例應用程式的連結，包括基本 DirectML 應用程式的範例。 |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 程式設計指南](directx-12-programming-guide.md)
