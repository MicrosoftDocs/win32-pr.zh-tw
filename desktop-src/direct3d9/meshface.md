---
description: 由網狀範本用來定義網格的臉部。 NFaceVertexIndices 陣列的每個元素都會參考用來建立臉部的網格頂點。
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563528"
---
# <a name="meshface"></a>MeshFace

由 [**網狀**](mesh.md) 範本用來定義網格的臉部。 NFaceVertexIndices 陣列的每個元素都會參考用來建立臉部的網格頂點。

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

其中：

-   nFaceVertexIndices-索引的數目。
-   陣列 DWORD faceVertexIndices \[ nFaceVertexIndices \] -索引的陣列。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



