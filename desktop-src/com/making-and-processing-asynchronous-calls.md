---
title: 製作和處理非同步呼叫
description: COM 物件可支援非同步呼叫。
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106995154"
---
# <a name="making-and-processing-asynchronous-calls"></a>製作和處理非同步呼叫

COM 物件可支援非同步呼叫。 當用戶端進行非同步呼叫時，控制權會立即返回用戶端。 當伺服器處理呼叫時，用戶端可以自由執行其他工作。 當用戶端無法在沒有呼叫結果的情況下繼續進行時，它可以在該時間取得呼叫的結果。

例如，大型或複雜記錄集的要求可能相當耗時。 用戶端可以透過非同步呼叫來要求記錄集，然後再執行其他工作。 當記錄集可供使用時，用戶端可以快速取得，而不會封鎖。

用戶端不會直接在伺服器物件上進行非同步呼叫。 相反地，它們會取得呼叫物件，以在伺服器物件上執行同步介面的非同步版本。 呼叫物件上的非同步介面具有形式為 Async *介面名稱* 的名稱。 例如，如果伺服器物件會執行名為 IMyInterface 的同步介面，則會有一個呼叫物件來執行名為 AsyncIMyInterface 的非同步介面。

> [!Note]  
> 不提供適用于 **idispatch** 的非同步支援，或繼承 **IDispatch** 的介面。

 

支援非同步呼叫的伺服器物件會執行 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) 介面。 這個介面會公開單一方法 [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)，它會建立指定之呼叫物件的實例。 用戶端可以查詢 **ICallFactory** ，以判斷物件是否支援非同步呼叫。

針對同步介面上的每個方法，對應的非同步介面會執行兩個方法。 這些方法會將開頭和結尾的前置詞附加 \_ \_ 至同步方法的名稱。 例如，如果名為 ISimpleStream 的介面有 Read 方法，AsyncISimpleStream 介面將會有開始 \_ 讀取和完成 \_ 讀取方法。 若要開始非同步呼叫，用戶端會呼叫 Begin \_ 方法。

當您執行伺服器物件時，您不需要為該物件所執行的每個介面提供呼叫物件。 如果伺服器物件會執行 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) 介面並使用標準封送處理，即使伺服器端沒有呼叫物件，封送處理的用戶端仍然可以取得 proxy 呼叫物件。 此 proxy 會將 Begin 方法封送 \_ 處理為同步呼叫，伺服器將會同步處理呼叫，而用戶端可以藉由呼叫完成方法來取得 out 參數 \_ 。

相反地，如果用戶端在伺服器端上有呼叫物件的介面上進行封送處理的同步呼叫，伺服器一律會以非同步方式處理呼叫。 用戶端將不會察覺到這種行為，因為用戶端會收到相同的 out 參數和從同步方法收到的相同傳回值。

無論是哪一種情況，用戶端與伺服器之間的互動都會被封送處理，就像呼叫是同步的一樣：同步和非同步 proxy 的輸出並不區分，如同對應的存根的輸出。 此行為可大幅簡化用戶端和伺服器的程式設計模型。 如果伺服器物件會執行 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)，則已封送處理的用戶端不需要嘗試建立可能無法使用的呼叫物件，而是一律可使用 call 物件。

當用戶端和伺服器位於相同的單元時，伺服器物件將會處理用戶端所進行的任何呼叫。 如果無法使用呼叫物件，用戶端必須明確取得同步介面並進行同步呼叫。

如需詳細資訊，請參閱下列主題：

-   [進行非同步呼叫](making-an-asynchronous-call.md)
-   [取消非同步呼叫](canceling-an-asynchronous-call.md)
-   [取消方法呼叫](canceling-method-calls.md)
-   [呼叫同步處理](call-synchronization.md)

 

 