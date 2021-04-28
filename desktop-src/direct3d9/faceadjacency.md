---
description: FaceAdjacency-此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090506"
---
# <a name="faceadjacency"></a>FaceAdjacency

此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。 當頂點位於平滑群組或材質界限時，會產生重複的結果。 此範本的目的是要讓載入器判斷哪些頂點的不同周邊參數實際上是模型中的相同頂點。 某些應用程式 (網狀簡化，例如) 可以利用這項資訊。

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

其中：

-   nIndices-網格中的索引數目。
-   索引 \[ nIndices \] -索引的陣列。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



