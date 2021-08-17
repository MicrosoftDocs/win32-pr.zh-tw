---
title: Direct3D 12 Raytracing HLSL 內建函式
description: 查看描述高階著色器語言 (HLSL) 內建函式（支援 Direct3D 12 raytracing 管線）之文章的連結。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce12f90233dee05bb4959498d3cb366aa88f1140182384bc26f5b017ee2bf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733781"
---
# <a name="raytracing-hlsl-intrinsics"></a>Raytracing HLSL 內建函式

下列 HLSL 內建函式函數支援 Direct3D 12 raytracing 管線。 

## <a name="in-this-section"></a>本節內容



| 主題 | 描述 |
|-|-|
| [**AcceptHitAndEndSearch 函式**](accepthitandendsearch-function.md) | 用於任何命中的著色器，以認可目前的點擊次數，然後停止搜尋光線的更多叫用。 |
| [**CallShader 函式**](callshader-function.md) | 從著色器中叫用另一個著色器。 |
| [**IgnoreHit 函式**](ignorehit-function.md) | 從任何命中的著色器呼叫，以拒絕點擊並結束著色器。 |
| [**PrimitiveIndex 函式**](primitiveindex.md) | 抓取下層加速結構實例內幾何內的基本類型自動產生索引。 |
| [**ReportHit 函式**](reporthit-function.md) | 由交集著色器呼叫以報告光線交集。 |
| [**TraceRay 函式**](traceray-function.md) | 在加速結構中將光線傳送到搜尋中。 |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
