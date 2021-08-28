---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ba168fa538cf176de57a8638d7603fd5bc6e990a1b83837ba603b3a62c4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961508"
---
# <a name="iagentnotifysinkvisiblestate"></a>IAgentNotifySink::VisibleState

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

當字元的可見度狀態變更時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

變更其可見度狀態之字元的識別碼。

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

可見度旗標。 當字元變成可見時，此布林值為 **True** ，當字元變成隱藏時為 **False** 。

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

上次變更字元可見度狀態的原因。 參數可以是下列其中一項：



| 值                                                                   | 描述                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const 不帶正負號短** **NeverShown = 0;**<br/>                 | 未顯示字元。                                                               |
| **const 不帶正負號短** **UserHid = 1;**<br/>                    | 使用者以字元的工作列圖示快顯功能表或語音輸入來隱藏字元。 |
| **const 不帶正負號短** **UserShowed = 2;**<br/>                 | 使用者顯示字元。                                                                  |
| **const 不帶正負號短** **ProgramHid = 3;**<br/>                 | 您的應用程式會隱藏該字元。                                                         |
| **const 不帶正負號短** **ProgramShowed = 4;**<br/>              | 您的應用程式會顯示該字元。                                                      |
| **const 不帶正負號短** **OtherProgramHid = 5;**<br/>            | 另一個應用程式會將字元隱藏。                                                      |
| **const 不帶正負號短** **OtherProgramShowed = 6;**<br/>         | 另一個應用程式會顯示該字元。                                                   |
| **const 不帶正負號短** **UserHidViaCharacterMenu = 7**<br/>     | 使用者會在字元的快顯功能表中隱藏該字元。                                    |
| **const 不帶正負號的短** **UserHidViaTaskbarIcon = UserHid**<br/> | 使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。 |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetVisible**](iagentcharacter--getvisible.md)、 [ **IAgentCharacter：： GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)


 

 





