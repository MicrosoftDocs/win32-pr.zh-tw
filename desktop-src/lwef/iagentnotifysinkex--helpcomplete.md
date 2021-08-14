---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749560"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

當使用者選取命令或字元來完成說明模式時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

說明模式完成之字元的識別碼。

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

使用者選取之命令的識別碼。

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

事件的原因可能是下列值：



| 值                                                                         | 描述                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const 不帶正負號的 short** **CSHELPCAUSE \_ 命令 = 1;**<br/>             | 使用者選取了您的應用程式所提供的命令。                            |
| **const 不帶正負號的 short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | 使用者選取了另一個用戶端的 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件。 |
| **const 不帶正負號的 short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | 使用者選取了 [開啟語音命令] 命令。                                   |
| **const 不帶正負號的 short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | 使用者選取了 [關閉語音命令] 命令。                                  |
| **const 不帶正負號的 short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | 使用者已選取 [顯示 *CharacterName* ] 命令。                                  |
| **const 不帶正負號的 short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | 使用者選取了 [隱藏 *CharacterName* ] 命令。                                  |
| **const 不帶正負號的短** **CSHELPCAUSE \_ 字元 = 7;**<br/>           | 選取的使用者 (按一下) 字元。                                           |



 

</dd> </dl>

當使用者按一下或拖曳字元，或從字元的快顯功能表中選取命令時，[說明] 模式通常會完成。 按一下其他字元或螢幕上的其他位置，並不會取消說明模式。 設定字元說明模式的用戶端可以將 [**IAgentCharacter：： HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) 設定為 **False**，以取消說明模式。  (這不會觸發 **IAgentNotifySinkEx：： HelpComplete** 事件。 ) 

當使用者從 [說明] 模式中的字元快顯功能表選取命令時，伺服器會移除功能表、使用 [**命令指定的**](helpcontextid-property.md)協助工具來呼叫說明，並傳送此事件。 與內容相關的 (也稱為「這是什麼？ ) 說明視窗會顯示在指標位置。 如果使用者選取語音輸入的命令，則會在字元上顯示 [說明] 視窗。 如果字元是在螢幕上，視窗會在畫面上顯示最接近字元的目前位置。

如果伺服器以空字串的形式傳回 *dwCommandID* ( "" ) ，表示使用者已選取伺服器提供的命令。

此事件只會傳送至用戶端應用程式，以將字元放入說明模式。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)、 [**IAgentCharacterEx：： SetHelpCoNtextID**](iagentcharacterex--sethelpcontextid.md)、 [**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)


 

