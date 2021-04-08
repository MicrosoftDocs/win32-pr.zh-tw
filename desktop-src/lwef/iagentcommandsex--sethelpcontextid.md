---
title: IAgentCommandsEx SetHelpCoNtextID
description: IAgentCommandsEx SetHelpCoNtextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682013"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

設定 [**Command**](/windows/desktop/lwef/the-command-object)物件 [**的提供物件**](helpcontextid-property.md)。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 進行設定。 當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，代理程式會自動呼叫 Help。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **命令的值** 為的值。 如果所選 **命令的 [值] 屬性中** 有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 建立說明檔需要 Microsoft Windows 說明編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： GetHelpCoNtextID**](iagentcommandsex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 