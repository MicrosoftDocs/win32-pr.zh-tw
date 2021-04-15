---
description: 定義簡單的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的臉部。
ms.assetid: vs|directx_sdk|~\mesh.htm
title: 網狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467436"
---
# <a name="mesh"></a>網狀

定義簡單的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的臉部。

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

其中：

-   nVertices-頂點數目。
-   陣列向量頂點 \[ nVertices \] -頂點的陣列，每個型別向量。 請參閱 [**Vector**](vector.md)。
-   nFaces-臉部數目。
-   陣列 MeshFace 臉部 \[ nFaces \] -臉部的陣列，每個類型都 MeshFace。 請參閱 [**MeshFace**](meshface.md)。
-   \[ ... \] -您可以在這裡使用任何的. x 檔案範本。 這可讓架構成為可擴充的。 通常會使用 [**材質**](material.md)和 [**TextureFilename**](texturefilename.md)範本。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



