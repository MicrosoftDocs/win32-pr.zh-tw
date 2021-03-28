---
title: SV_GroupID
description: 計算著色器在其中執行之執行緒群組的索引。
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092805"
---
# <a name="sv_groupid"></a>SV \_ GroupID

計算著色器在其中執行之執行緒群組的索引。 索引會指向整個群組，而不是個別的執行緒。 可能的值會在以參數形式傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)的範圍內變更。 例如，呼叫分派 (2，1，1) 會產生可能的值0、0、0和1、0、0。

定義 [**分派呼叫**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) 內的群組位移，每個分派呼叫的維度。

## <a name="type"></a>類型



|       |
|-------|
| 類型  |
| uint3 |



 

## <a name="remarks"></a>備註

這個系統值是選擇性的。

下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、sv \_ GroupID) 。

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

下列著色器類型支援此函數：



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 