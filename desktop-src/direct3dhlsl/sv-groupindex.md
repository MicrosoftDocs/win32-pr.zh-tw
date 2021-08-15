---
title: SV_GroupIndex
description: '\ 0034; 壓平合併 \ 0034;執行緒群組中計算著色器執行緒的索引，會將多維度的 SV GroupThreadID 變成 \_ 1d 值。 SV \_ GroupIndex 從0變化 (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211;單.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508248"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

執行緒群組中計算著色器執行緒的「壓平合併」索引，可將多維度的 SV \_ GroupThreadID 變成1d 值。 SV \_ GroupIndex 從0變化 (numthreadsX \* numthreadsY \* numThreadsZ) –1。

## <a name="type"></a>類型



| 類型 |
|------|
| uint |



 

## <a name="remarks"></a>備註


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



其中 dimx 和 dimy 是進入點的 [numthreads](sm5-attributes-numthreads.md) 屬性所指定的維度。

這個系統值是選擇性的。 不過，其用途可確保執行緒只會寫入至其在 groupshared 變數中指派的記憶體區域。

下圖顯示傳遞至 >id3d11devicecoNtext 的參數之間的關聯性 [**：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中所指定的值、numthreads (10、8、3) ，以及將傳遞給執行緒相關系統值的計算著色器的值 (SV \_ GroupIndex、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 