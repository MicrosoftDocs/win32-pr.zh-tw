---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692604"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

在接聽模式變更時通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

接聽狀態變更的字元。

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

接聽模式的狀態。 **True** 表示接聽模式已啟動; **False**，表示接聽模式已結束。

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

事件的原因，可能是下列其中一個值。



| 值                                                                             | 描述                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ PROGRAMDISABLED = 1;**<br/>    | 程式碼已關閉接聽模式。                                 |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ PROGRAMTIMEDOUT = 2;**<br/>    | 程式碼 (開啟接聽模式) 超時。                          |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERTIMEDOUT = 3;**<br/>       | 接聽 (開啟接聽模式) 超時。                     |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERRELEASEDKEY = 4;**<br/>    | 因為使用者放開接聽金鑰，所以已關閉接聽模式。     |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERUTTERANCEENDED = 5;**<br/> | 因為使用者已完成說話，所以已關閉接聽模式。              |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ CLIENTDEACTI加值稅ED = 6;**<br/>  | 因為已停用輸入作用中用戶端，所以已關閉接聽模式。 |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ DEFAULTCHARCHANGE = 7**<br/>   | 因為預設字元已變更，所以已關閉接聽模式。       |
| **const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERDISABLED = 8**<br/>        | 因為使用者停用語音輸入，所以已關閉接聽模式。          |



 

</dd> </dl>

當使用者按下接聽鍵或其超時時間結束時，或當輸入-主動用戶端使用 **True** 或 **False** 呼叫 [**IAgentCharacterEx：：接聽**](iagentcharacterex--listen.md)方法時，就會將此事件傳送至所有用戶端。

此事件會將值傳回給目前已載入此字元的用戶端。 所有其他用戶端都會收到 null 字元， (空的字串) 。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：：接聽**](iagentcharacterex--listen.md)


 

 





