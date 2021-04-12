---
description: 指定網格的頂點色彩，而不是套用每個臉部或每個網格的材質。
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385632"
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

 

 



