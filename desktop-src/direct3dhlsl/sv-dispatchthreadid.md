---
title: SV_DispatchThreadID
description: 計算著色器所執行之合併執行緒和執行緒群組的索引。
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996515"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

計算著色器所執行之合併執行緒和執行緒群組的索引。 SV \_ DispatchThreadID 是 sv \_ GroupID \* numthreads 和 GroupThreadID 的總和。 它會隨著 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) 與 [numthreads](sm5-attributes-numthreads.md)中指定的範圍而有所不同。 例如，如果分派 (2，2，2) 在具有 numthreads (3，3，3) SV DispatchThreadID 的計算著色器上呼叫，則 \_ 每個維度的範圍為0到5。

## <a name="type"></a>類型



|       |
|-------|
| 類型  |
| uint3 |



 

## <a name="remarks"></a>備註

這個系統值是選擇性的。

下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、sv \_ DispatchThreadID、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
