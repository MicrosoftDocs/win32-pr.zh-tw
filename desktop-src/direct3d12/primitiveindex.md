---
description: 抓取下層加速結構實例內幾何內的基本類型自動產生索引。
ms.assetid: ''
title: PrimitiveIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972781"
---
# <a name="primitiveindex-function"></a>PrimitiveIndex 函式

抓取下層加速結構實例內幾何內的基本類型自動產生索引。

## <a name="syntax"></a>語法

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>備註

針對 **D3D12 \_ RAYTRACING \_ geometry \_ 類型 \_ 三角形**，這是 geometry 物件內的三角形索引。

針對 **D3D12 \_ RAYTRACING \_ GEOMETRY \_ 類型程式性 \_ \_ 基本 \_ AABBS**，這是定義 GEOMETRY 物件之 AABB 陣列中的索引。

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)

## <a name="see-also"></a>另請參閱

* [Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
