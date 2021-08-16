---
title: IAgentCharacterEx GetHelpCoNtextID
description: IAgentCharacterEx GetHelpCoNtextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750792"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx::GetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

抓取字元 [**的提供。**](helpcontextid-property.md)

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

接收字元的說明主題內容編號之變數的位址。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md)則當 [**HelpModeOn**](helpmodeon-property.md)設定為 **True** 且使用者選取該字元時，Microsoft Agent 會自動呼叫說明。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **字元的 [值] 的值** 。

**IAgentCharacterEx：： GetHelpCoNtextID** 會傳回您為字元設定的使用者 [**id**](helpcontextid-property.md) 。 它不會傳回其他用戶端 **所設定的** 比。

> [!Note]  
> 建立說明檔需要 Microsoft Windows help 編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： SetHelpCoNtextID**](iagentcharacterex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




