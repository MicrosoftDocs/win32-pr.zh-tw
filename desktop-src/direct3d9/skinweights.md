---
description: 此範本會以每個網狀架構為基礎來具現化。
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627908"
---
# <a name="skinweights"></a>SkinWeights

此範本會以每個網狀架構為基礎來具現化。 在網狀架構中，會顯示此範本的 n 個實例序列，其中 n 是 (X 檔案框架的數目，這是影響網格中頂點的) 。 範本的每個實例基本上會定義特定骨骼在網格上的影響。 其中有一個頂點索引清單，以及一個相對應的加權清單。

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

其中：

-   要定義其影響的骨骼名稱是 transformNodeName，而 nWeights 是受此骨骼影響的頂點數目。
-   此骨骼受影響的頂點會包含在 vertexIndices 中，而且此骨骼所影響之每個頂點的權數都會包含在加權中。
-   矩陣 matrixOffset 會將網格頂點轉換成骨骼的空間。 當串連至骨骼的轉換時，這會提供與骨骼所影響之網格的世界空間座標。 請參閱 [**Matrix4x4**](matrix4x4.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



