---
title: 反標記
description: OLE 會提供一種特殊類型的標記來執行，稱為反標記。
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021587"
---
# <a name="anti-monikers"></a>反標記

OLE 會提供一種特殊類型的標記來執行，稱為 *反標記*。 您可以在建立新的「標記」類別時使用這個標記。 您可以使用它做為它所組成之標記的反向，有效地取消該標記，與「...」運算子在檔案系統命令中的目錄層級上移動的方式大致相同。

必須有反標記可供使用，因為一旦建立複合的標記，就無法刪除部分的標記（例如，物件移動）。 相反地，您可以使用反標記來移除複合標記中的一或多個專案。

反標記是明確要作為反向使用的標記類別。 COM 會定義名為 [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) 的函式，此函式會傳回反標記。 您通常會使用這個函數來執行 [**IMoniker：：反向**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) 方法。

反標記只是對這些標記類型的反向，這些類型是實為了將反標記視為反向的。 例如，如果您想要移除複合標記的最後一個部分，則不應建立反標記，並將它撰寫至複合結尾。 您無法確定複合的最後一個部分會將反標記視為反向。 相反地，您應該在複合的標記上呼叫 [**IMoniker：： Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) ，並指定 **FALSE** 做為第一個參數。 這會建立一個列舉值，以反向順序傳回元件的名字。 您可以使用列舉值來取出複合的最後片段，並在該名字標記上呼叫 [**反向**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) 。 **反向** 傳回的標記是您需要移除複合最後一部分的結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[類別名字標記](class-monikers.md)
</dt> <dt>

[複合的名字](composite-monikers.md)
</dt> <dt>

[檔案名字](file-monikers.md)
</dt> <dt>

[專案的名字](item-monikers.md)
</dt> <dt>

[指標標記](pointer-monikers.md)
</dt> </dl>

 

 




