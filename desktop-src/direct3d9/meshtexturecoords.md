---
description: 定義網格的材質座標。
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: MeshTextureCoords
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5854d4a3a7f602d560845874c3af6339ff1d5e9ebbae0f79f35f4298591ee06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628428"
---
# <a name="meshtexturecoords"></a>MeshTextureCoords

定義網格的材質座標。

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

其中：

-   nTextureCoords-材質座標的數目。
-   陣列 Coords2d textureCoords \[ nTextureCoords \] -2d 材質座標的陣列。 請參閱 [**Coords2d**](coords2d.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



