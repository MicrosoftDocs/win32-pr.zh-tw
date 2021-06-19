---
title: Direct3D 12 raytracing HLSL 系統值內建函式
description: 查看描述高階著色器語言 (HLSL) 系統值內建函式（支援 Direct3D 12 raytracing 管線）的文章連結。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396433"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Direct3D 12 raytracing HLSL 系統值內建函式

系統值是使用特殊內建函式來抓取，而不是在著色器函式簽章中包含具有特殊語義的參數。 

## <a name="in-this-section"></a>本節內容

### <a name="ray-dispatch-system-values"></a>光線分派系統值

| 主題 | 描述 |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | 取得以 **DispatchRaysDimensions** 系統值內建的寬度和高度取得的目前 x 和 y 位置。 |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | 原始 **DispatchRays** 呼叫中所指定之 **D3D12 \_ 分派 \_ 放射放射 \_** 值結構的寬度、高度和深度值。 |

### <a name="ray-system-values"></a>光線系統值

| 主題 | 描述 |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | 目前光線的世界空間原點。 |
| [**WorldRayDirection**](worldraydirection.md) | 目前光線的世界空間方向。 |
| [**RayTMin**](raytmin.md) | 表示光線目前參數起點的 float。 |
| [**RayTCurrent**](raytcurrent.md) | 浮點數，代表光線目前的參數結束點。  |
| [**RayFlags**](rayflags.md) | 包含目前 **ray_flag** 旗標的不帶正負號的整數。 |

### <a name="primitiveobject-space-system-values"></a>基本/物件空間系統值

| 主題 | 描述 |
|-|-|
| [**InstanceIndex**](instanceindex.md) | 最上層 raytracing 加速結構中目前實例的自動產生索引。 |
| [**Id**](instanceid.md) | 最上層結構中最下層加速結構實例上實例的使用者提供識別碼。 |
| [**PrimitiveIndex**](primitiveindex.md) | 下層加速結構實例內幾何內的基本類型自動產生索引。 |
| [**ObjectRayOrigin**](objectrayorigin.md) | 目前光線的物件空間原點。 |
| [**ObjectRayDirection**](objectraydirection.md) | 目前光線的物件空間方向。 |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | 從物件空間轉換成世界空間的矩陣。 |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | 從物件空間轉換成世界空間的矩陣。 |
| [**WorldToObject3x4**](worldtoobject3x4.md) | 從世界空間轉換成物件空間的矩陣 |
| [**WorldToObject4x3**](worldtoobject4x3.md) | 從世界空間轉換成物件空間的矩陣 |
### <a name="hit-specific-system-values"></a>點擊特定系統值

| 主題 | 描述 |
|-|-|
| [**HitKind**](hitkind.md) | 傳回作為 **HitKind** 參數傳遞至 [**ReportHit**](reporthit-function.md)的值。 |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
