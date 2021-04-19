---
description: 會話或撥號狀態表示會話的目前狀態，例如 &\# 0034; 提供&\# 0034; 或 &\# 0034; connected. &\# 0034;適當處理狀態資訊對於大部分 TAPI 應用程式正常運作而言很重要。
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981684"
---
# <a name="state"></a>狀態

會話或撥號狀態表示會話的目前狀態，例如「供應」或「已連線」。 適當處理狀態資訊對於大部分 TAPI 應用程式正常運作而言很重要。 例如，回應作業只能在提供的會話上執行，但是如果會話處於該狀態，則傳輸將會失敗。

會話的狀態會因為事件的結果而變更。 事件可以是要求或未經要求的。 *請求事件* 是由控制會話的應用程式所造成，例如叫用 TAPI 會話操作時。 *未經* 要求的事件是由交換器、電話網絡、使用者按下本機電話上的按鈕，或是遠端方的動作所造成。

每當服務提供者偵測到會話狀態變更時，就會報告 TAPI 和 TAPI 的變更，對所有擁有者和監視應用程式發出事件通知。 應用程式必須適當地回應這些通知。 請參閱 [TAPI 初始化](tapi-initialization.md) 下的事件通知，以取得有關控制哪些事件會回報給應用程式的資訊。

應用程式應該一律處理狀態事件通知。 針對某個實體設定有效的狀態轉換可能對另一個實體設定無效。 例如，假設有一條線在電腦和不同的電話組上實際終止，在電腦與電話組間建立合作物件線設定。 在電腦上執行的應用程式可能不知道電話設定活動。 也就是說，在沒有服務提供者察覺的情況下，可能會使用這一行。 嘗試撥出呼叫的應用程式將會成功從 TAPI 配置呼叫外觀，但這會導致在行上共用使用中的呼叫。 在不先檢查撥號音的情況下，盲目傳送 DTMF 撥號字串，可能不會導致預期的 (或有禮貌) 的行為。

應用程式不應假設從某個狀態到另一個狀態的固定進展。 狀態事件會抵達並以非同步方式轉送，且通知可能無法以可預測的順序接收。 因此，您應該將撥號狀態通知視為告知應用程式呼叫的新狀態，而不是報告兩個狀態之間的轉換。

所有電話語音服務提供者都必須提供此資訊。

* * TAPI 2.x： * *[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus)、 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 [**行 \_ CALLSTATE**](./line-callstate.md) 訊息、 [LINECALLSTATE \_ 常數](./linecallstate--constants.md)

**TAPI 3.x： **[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_** [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 、 [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) notification、 [**CALL \_ STATE**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state)列舉值的 CIL CALLID 成員

 

 
