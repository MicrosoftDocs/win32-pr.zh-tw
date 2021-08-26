---
title: D3D9 和 D3D8 宣告之間的對應
description: 此資料表會將 D3DVERTEXELEMENT9 宣告的成員對應至 Direct3D 8 宣告。
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069028"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>D3D9 和 D3D8 宣告之間的對應

此資料表會將 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 宣告的成員對應至 Direct3D 8 宣告。



| Direct3D 9 使用量           | Direct3D 9 使用方式索引 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| D3DDECLUSAGE \_ 位置     | 0                      | D3DVSDE \_ 位置     |
| D3DDECLUSAGE \_ 位置     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ 正常       | 0                      | D3DVSDE \_ 正常       |
| D3DDECLUSAGE \_ 正常       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| D3DDECLUSAGE \_ 色彩        | 0                      | D3DVSDE \_ 擴散      |
| D3DDECLUSAGE \_ 色彩        | 1                      | D3DVSDE \_ 反光     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

當搭配 Direct3D 7 驅動程式上的硬體頂點處理使用宣告時，Direct3D runtime 會將它轉換為具有下列規則的 FVF：

-    (從 MaxStreams cap) 看出，只應使用串流0。
-   頂點元素的順序應該與 FVF 位的順序相同。
-   不允許材質座標中的間隙。
-   未描述資料表的任何頂點元素都無法轉換成所有預先 DirectX 8 驅動程式的有效 FVF，因此無法用於這些驅動程式。
-   \_ \_ 如果裝置未設定 D3DPTEXTURECAPS \_ 投射或 D3DPTEXTURECAPS 立方體貼圖 caps，則只有 D3DDECLTYPE FLOAT2 可供具有 D3DDECLUSAGE TEXCOORD 的頂點元素使用 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點宣告](vertex-declaration.md)
</dt> </dl>

 

 



