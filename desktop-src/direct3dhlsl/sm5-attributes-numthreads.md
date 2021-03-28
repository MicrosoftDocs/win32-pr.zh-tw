---
title: numthreads
description: 定義在分派計算著色器時，要在單一線程群組中執行的執行緒數目 (查看 >id3d11devicecoNtext 分派) 。
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382737"
---
# <a name="numthreads"></a>numthreads

定義在分派計算著色器時，要在單一線程群組中執行的執行緒數目 (請參閱 [**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)) 。


```
numthreads(X, Y, Z)    
```



X、Y 和 Z 值表示特定方向的執行緒群組大小，X Y z 的總計會 \* \* 提供群組中的執行緒數目。 在三個維度上指定執行緒群組大小的功能，可讓您以邏輯2D 和3D 資料結構的方式存取個別的執行緒。

例如，如果計算著色器正在進行4x4 矩陣加法，則 numthreads 可以設定為 numthreads (4，4，1) 而且個別執行緒中的索引會自動符合矩陣專案。 計算著色器也可以使用 numthreads (16，1，1) ，宣告具有相同執行緒數目 (16) 的執行緒群組，不過它接著必須根據目前的執行緒編號來計算目前的矩陣專案。

**Numthreads** 可允許的參數值取決於計算著色器版本。



| 計算著色器 | 最大 Z | 最大執行緒 (X \* Y \* Z)  |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

下圖顯示傳遞至 >id3d11devicecoNtext 的參數之間的關聯性 [**：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)、分派 (5、3、2) 、numthreads 屬性中指定的值、numthreads (10、8、3) 以及將傳遞給執行緒相關系統值的計算著色器的值 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

下列著色器類型支援此屬性：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 