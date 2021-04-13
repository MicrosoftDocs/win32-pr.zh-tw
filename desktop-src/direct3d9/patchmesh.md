---
description: 定義貝塞爾修補程式所定義的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的修補程式。
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509884"
---
# <a name="patchmesh"></a>PatchMesh

定義貝塞爾修補程式所定義的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的修補程式。

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

其中：

-   nVertices-頂點數目。
-   頂點 \[ nVertices \] -頂點的陣列。 請參閱 [**Vector**](vector.md)。
-   nPatches-修補程式的數目。
-   修補程式 \[ nPatches \] -修補程式陣列。 請參閱 [**Patch**](patch.md)。
-   \[ ... \] -您可以在這裡使用任何的. x 檔案範本。 這可讓架構成為可擴充的。

修補程式會使用頂點陣列中的頂點做為每個修補程式的控制點。 這是舊版的範本。 最新的修補程式網狀範本是 [**PatchMesh9**](patchmesh9.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



