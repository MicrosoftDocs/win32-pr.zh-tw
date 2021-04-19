---
title: IAgentCommandEx SetHelpCoNtextID
description: IAgentCommandEx SetHelpCoNtextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966457"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

設定 [**Command**](/windows/desktop/lwef/the-command-object)物件 [**的提供物件**](helpcontextid-property-com.md)。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 進行設定。 當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，Microsoft Agent 會自動呼叫 Help。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property-com.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **命令的值** 為的值。

> [!Note]  
> 建立說明檔需要 Microsoft Windows 說明編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommandEx：： GetHelpCoNtextID**](iagentcommandex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 