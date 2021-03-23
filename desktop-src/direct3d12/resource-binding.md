---
title: 資源系結
description: 系結是將資源物件連結至圖形管線著色器的程式。
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548421"
---
# <a name="resource-binding"></a>資源系結

系結是將資源物件連結至圖形管線著色器的程式。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [資源系結總覽](resource-binding-flow-of-control.md) | DirectX 12 中資源系結的關鍵是 *描述* 項、 *描述中繼資料表*、 *描述* 元堆積和 *根* 簽章的概念。 |
| [來自 Direct3D 11 的系結模型差異](binding-model.md) | DirectX12 系結背後的主要設計決策之一，是將它與其他管理工作分開。 這會在應用程式上放置一些需求，以管理特定潛在的風險。 |
| [描述項](descriptors.md) | 描述項是 D3D12 中單一資源的系結主要單位。 |
| [描述元堆積](descriptor-heaps.md) | 描述元堆積是描述項連續配置的集合，每個描述項的一個配置。 |
| [描述中繼資料表](descriptor-tables.md) | 描述項資料表在邏輯上是描述項的陣列。 |
| [根簽章](root-signatures.md) | 根簽章會定義要系結至圖形管線的資源類型。 |
| [功能查詢](capability-querying.md) | 您的應用程式可以透過呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)，探索資源系結的支援層級以及許多其他功能。 |
| [HLSL 中的資源系結](resource-binding-in-hlsl.md) | 本主題說明使用高階著色器語言 (HLSL) [著色器模型 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) 與 Direct3D 12 的一些特定功能。 所有 Direct3D 12 硬體都支援著色器模型5.1，因此對此模型的支援不會相依于硬體功能層級。 |
| [UMA 優化：可存取 CPU 的材質和標準 Swizzle](default-texture-mapping.md) | 通用記憶體架構 (UMA) Gpu 可提供比離散 Gpu 更高的效率，尤其是在針對行動裝置進行優化的情況下。 當 GPU 為 UMA 時提供資源 CPU 存取權，可減少在 CPU 與 GPU 之間發生的複製量。 雖然我們不建議應用程式盲目將 CPU 存取權提供給 UMA 設計上的所有資源，但有機會藉由提供正確的資源 CPU 存取來提高效率。 與離散 Gpu 不同的是，CPU 可以有 GPU 可存取的所有資源指標。 |
| [具類型的未排序存取視圖載入](typed-unordered-access-view-loads.md) | 未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)的 UAV 讀取的能力。 |
| [磁片區磚資源](volume-tiled-resources.md) | 磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。 |
| [子資源](subresources.md) | 說明如何將資源分割成子資源，以及如何參考子資源的單一、多重或配量。 |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 程式設計指南](directx-12-programming-guide.md)
* [DirectX advanced learning 影片教學課程： DirectX 12 中的資源系結](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [記憶體管理](memory-management.md)