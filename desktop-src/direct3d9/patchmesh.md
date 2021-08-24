---
description: PatchMesh 會定義貝塞爾修補程式所定義的網格，包括頂點清單以及網格的補充程式，方法是在頂點陣列中編制索引。
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3bc3c243fb42014ba18aac134ea008d5818e249a601858be6724d5a0fd7310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746918"
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

 

 



