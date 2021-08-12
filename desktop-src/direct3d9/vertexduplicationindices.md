---
description: VertexDuplicationIndices-此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ac9b43e0aa05d75727e24bb4677ef0b21fcb41366800185551c48f5fb76f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290333"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。 當頂點位於平滑群組或材質界限時，會產生重複的結果。 此範本的目的是要讓載入器判斷哪些頂點的不同周邊參數實際上是模型中的相同頂點。 某些應用程式 (網狀簡化，例如) 可以利用這項資訊。

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

其中：

-   nIndices-頂點索引的數目。 這是網格中的頂點數目。
-   nOriginalVertices：發生任何重複之前，網格中的頂點數目。
-   \[如果未發生重複，值索引 n 會保存頂點的頂點 \] \[ n \] 在網格的頂點陣列中的頂點。 因此，這個陣列中的索引是相同的，因此會指出重複的頂點。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



