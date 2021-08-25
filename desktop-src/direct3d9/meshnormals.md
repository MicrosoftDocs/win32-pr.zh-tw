---
description: 定義網格的法線。
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a261dd8dbd46cf26116657b983eca4f693603869a80bf2fb110c0f165221ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846458"
---
# <a name="meshnormals"></a>MeshNormals

定義網格的法線。 向量的第一個陣列是一般向量本身，而第二個數組是索引的陣列，用來指定要套用至指定臉部的法線。 NFaceNormals 成員的值應等於網格中的臉部數目。

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

其中：

-   nNormals：法線數目。
-   陣列向量法線 \[ nNormals \] -法線的陣列。 請參閱 [**Vector**](vector.md)。
-   nFaceNormals-臉部法線的數目。
-   陣列 MeshFace faceNormals \[ nFaceNormals \] -網狀臉部法線的陣列。 請參閱 [**MeshFace**](meshface.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



