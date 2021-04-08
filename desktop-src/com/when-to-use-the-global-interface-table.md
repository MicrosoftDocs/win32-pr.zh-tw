---
title: 使用全域介面資料表的時機
description: 使用全域介面資料表的時機
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024137"
---
# <a name="when-to-use-the-global-interface-table"></a>使用全域介面資料表的時機

如果您要在進程中的單元之間多次封送處理介面指標，您可以使用 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面。 使用其他技術時，您必須 remarshal 每次。

> [!Note]  
> 如果介面指標只是取消封送一次，您可能會想要使用 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 函數。 它也可以用來將介面指標從某個執行緒傳遞至相同進程中的另一個執行緒。

 

[**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)介面也會讓程式設計人員更容易發生另一個困難的問題。 當下列條件成立時，就會發生此問題：

-   同進程 agile 物件會匯總無限制執行緒封送處理器。
-   這個相同的 agile 物件也會將 (做為成員變數，) 介面指標指向其他不是 agile 的物件，而且不會匯總無限制執行緒封送處理器。

在這種情況下，如果外部物件被封送處理至另一個單元，而應用程式呼叫它，而物件嘗試在其任何不是無限制執行緒的成員變數介面指標上呼叫，或為其他單元中的物件 proxy，則可能會得到不正確的結果或錯誤 RPC E 錯誤的 \_ \_ \_ 執行緒。 發生此錯誤的原因是，內部介面設計為只能從第一次儲存在成員變數中的單元中呼叫。

若要解決這個問題，匯總無限制執行緒封送處理器的外部物件應該在內部介面上呼叫 [**IGlobalInterfaceTable：： RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) ，並將產生的 cookie 儲存在其成員變數中，而不是儲存實際的介面指標。 當外部物件要在內建物件的介面指標上呼叫時，它應該呼叫 [**IGlobalInterfaceTable：： GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)，使用傳回的介面指標，然後釋放它。 當外部物件消失時，它應該呼叫 [**IGlobalInterfaceTable：： RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) 來移除全域介面資料表中的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立全域介面資料表](creating-the-global-interface-table.md)
</dt> </dl>

 

 