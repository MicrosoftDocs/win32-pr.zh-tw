---
description: 指定網格的頂點色彩，而不是套用每個臉部或每個網格的材質。
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035f8d51ae692b0edd20f7b06b5ab8e756ff73d9cd8265d64700ce5374f9a15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628328"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

指定網格的頂點色彩，而不是套用每個臉部或每個網格的材質。

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

其中：

-   nVertexColors-色彩數目。 這符合網格中的頂點數目。
-   陣列 IndexColor vertexColors \[ nVertexColors \] -索引色彩的陣列。 請參閱 [**IndexedColor**](indexedcolor.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



