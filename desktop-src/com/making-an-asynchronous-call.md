---
title: 進行非同步呼叫
description: 進行同步呼叫的程式很簡單，用戶端會在伺服器物件上取得介面指標，並透過該指標呼叫方法。 非同步呼叫涉及 call 物件，因此它包含幾個步驟。
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a153b826e570920fca2a92f5b53ed2079c561cbcda899b793cef1f39473bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755988"
---
# <a name="making-an-asynchronous-call"></a>進行非同步呼叫

進行同步呼叫的程式很簡單：用戶端會取得伺服器物件上的介面指標，並透過該指標呼叫方法。 非同步呼叫涉及 call 物件，因此它包含幾個步驟。

針對同步介面上的每個方法，對應的非同步介面會執行兩個方法。 這些方法會將開頭和結尾的前置詞附加 \_ \_ 至同步方法的名稱。 例如，如果名為 ISimpleStream 的介面有 Read 方法，AsyncISimpleStream 介面將會有開始 \_ 讀取和完成 \_ 讀取方法。 若要開始非同步呼叫，用戶端會呼叫 Begin \_ 方法。

**開始非同步呼叫**

1.  查詢 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) 介面的伺服器物件。 如果 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 傳回 E \_ NOINTERFACE，則伺服器物件不支援非同步呼叫。

2.  呼叫 [**ICallFactory：： CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) 來建立對應至所需介面的呼叫物件，然後將指標釋放至 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)。

3.  如果您未要求呼叫 [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)的非同步介面指標，請查詢非同步介面的呼叫物件。

4.  呼叫適當的 Begin \_ 方法。

伺服器物件現在正在處理非同步呼叫，用戶端可以自由地執行其他工作，直到需要呼叫的結果為止。

呼叫物件一次只能處理一個非同步呼叫。 如果相同或第二個用戶端在 \_ 暫止的非同步呼叫完成之前呼叫 Begin 方法，begin \_ 方法會傳回「RPC \_ E \_ 呼叫擱置」 \_ 。

如果用戶端不需要 Begin 方法的結果 \_ ，它可以在此程式的結尾釋放呼叫物件。 COM 會偵測此狀況，並清除呼叫。 \_不會呼叫 Finish 方法，用戶端也不會取得任何 out 參數或傳回值。

當伺服器物件已準備好從 Begin 方法傳回時 \_ ，它會對呼叫物件發出信號，表示它已完成。 當用戶端就緒時，它會檢查呼叫物件是否已收到信號。 如果是，用戶端可以完成非同步呼叫。

在用戶端與伺服器之間進行此信號和檢查的機制是呼叫物件上的 [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) 介面。 呼叫物件通常會藉由匯總系統提供的同步處理物件來執行這個介面。 同步處理物件會包裝事件控制碼，而伺服器會 \_ 呼叫 [**ISynchronize：：信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)，就會在從 Begin 方法傳回之前發出信號。

**完成非同步呼叫**

1.  查詢 [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) 介面的呼叫物件。

2.  呼叫 [**ISynchronize：： Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait)。

3.  如果 [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) 傳回 RPC \_ E \_ TIMEOUT，則 Begin \_ 方法未完成處理。 用戶端可以繼續執行其他工作，稍後再呼叫 **等候** 。 它無法呼叫完成 \_ 方法，直到 **等候** 返回 S \_ OK。

    如果 [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) 傳回 S \_ OK，就會 \_ 傳回 Begin 方法。 呼叫適當的完成 \_ 方法。

完成方法會將 \_ 任何 out 參數傳遞給用戶端。 非同步方法的行為（包括完成方法的傳回值 \_ ）應該完全符合對應的同步方法。

當完成方法傳回時，用戶端就可以釋出呼叫物件 \_ ，也可以保留呼叫物件的指標以進行其他呼叫。 無論是哪一種情況，當不再需要物件時，用戶端都會負責釋放呼叫物件。

如果您在 \_ 沒有任何呼叫進行時呼叫 COMPLETE 方法，則方法會傳回 RPC \_ E \_ 呼叫 \_ 完成。

> [!Note]  
> 如果用戶端和伺服器物件位於相同的單元中，則不保證對 [**ICallFactory：： CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) 的呼叫會成功。 如果伺服器物件不支援對特定介面進行非同步呼叫，則嘗試建立呼叫物件將會失敗，而且用戶端必須使用同步介面。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取消非同步呼叫](canceling-an-asynchronous-call.md)
</dt> <dt>

[非同步呼叫期間的用戶端安全性](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[模擬和非同步呼叫](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 