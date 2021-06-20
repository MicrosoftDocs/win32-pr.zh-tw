---
description: PatchMesh9 會定義貝塞爾修補程式所定義的網格，包括頂點清單以及網格的補充程式，方法是在頂點陣列中編制索引。
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404701"
---
# <a name="patchmesh9"></a>PatchMesh9

定義貝塞爾修補程式所定義的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的修補程式。

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

其中：

-   類型-修補程式網格類型：矩形、三角形或 N 修補程式。
-   曲線方程式中的變數程度。
-   高序位修補程式介面的基礎型別。
-   nVertices-頂點數目。
-   頂點 \[ nVertices \] -頂點的陣列。 請參閱 [**Vector**](vector.md)。
-   nPatches-修補程式的數目。
-   修補程式 \[ nPatches \] -修補程式陣列。 請參閱 [**Patch**](patch.md)。
-   \[ ... \] -您可以在這裡使用任何的. x 檔案範本。 這可讓架構成為可擴充的。

修補程式會使用頂點陣列中的頂點做為每個修補程式的控制點。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



