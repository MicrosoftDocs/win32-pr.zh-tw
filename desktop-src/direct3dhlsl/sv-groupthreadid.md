---
title: SV_GroupThreadID
description: 在中執行計算著色器之執行緒群組內個別執行緒的索引。
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316267"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

在中執行計算著色器之執行緒群組內個別執行緒的索引。 SV \_ GroupThreadID 在 [numthreads](sm5-attributes-numthreads.md) 屬性中為計算著色器指定的範圍內會有所不同。 例如，如果 numthreads (3，2，1) 指定了 SV GroupThreadID 輸入值的可能值， \_ 就會有此範圍的值 (0-2、0-1、0) 。

## <a name="type"></a>類型



|       |
|-------|
| 類型  |
| uint3 |



 

## <a name="remarks"></a>備註

這個系統值是選擇性的，且一律在傳遞至 [numthreads](sm5-attributes-numthreads.md) 屬性的值範圍內。

下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、sv \_ GroupThreadID、[sv \_ GroupID](sv-groupid.md)) 。

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

 

 