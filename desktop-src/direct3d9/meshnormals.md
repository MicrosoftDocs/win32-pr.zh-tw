---
description: 定義網格的法線。
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187498"
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

 

 



