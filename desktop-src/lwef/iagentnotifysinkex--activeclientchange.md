---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961498"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

如果用戶端應用程式的作用中用戶端不再是字元的作用中用戶端，則會通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

作用中用戶端狀態變更之字元的識別碼。

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

用戶端的作用中狀態變更，可以是下列任何一個值的組合：



| 值                                                              | 描述                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const 不帶正負號的 short** **ACTI加值稅E \_ NOTACTIVE = 0;**<br/>   | 您的用戶端不是字元的作用中用戶端。                |
| **const 不帶正負號短****啟用使用中 \_ = 1;**<br/>      | 您的用戶端是字元的作用中用戶端。                    |
| **const 不帶正負號的 short** **ACTI加值稅E \_ INPUTACTIVE = 2;**<br/> | 您的用戶端是輸入-主動 (最上層字元) 的作用中用戶端。 |



 

</dd> </dl>

當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。 同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md) 事件。

當使用中用戶端的字元變更時，此事件會傳回該字元的識別碼，如果您的應用程式已成為字元的作用中用戶端， **則為 True** ; 如果不再是字元的作用中用戶端，則為 **False** 。

當使用者在字元的快顯功能表中選取其他用戶端應用程式的專案，或使用 [語音] 命令、用戶端應用程式變更其作用中狀態，或其他用戶端應用程式結束其與 Microsoft Agent 的連接時，用戶端應用程式可能會收到此事件。 代理程式只會將此事件傳送給直接受影響的用戶端應用程式，這些應用程式會變成作用中用戶端或停止成為作用中用戶端。

您可以使用 [**啟動**](iagentcharacter--activate.md) 方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入-主動用戶端 (也會讓字元) 最上層。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： Activate**](iagentcharacter--activate.md)、 [**IAgentCharacterEx：： GetActive**](iagentcharacterex--getactive.md)、 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





