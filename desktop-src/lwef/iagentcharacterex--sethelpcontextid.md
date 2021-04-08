---
title: IAgentCharacterEx SetHelpCoNtextID
description: IAgentCharacterEx SetHelpCoNtextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672175"
---
# <a name="iagentcharacterexsethelpcontextid"></a>IAgentCharacterEx::SetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

設定字元 [**的提供。**](helpcontextid-property.md)

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

與字元相關聯之說明主題的內容編號;用來為字元提供即時線上說明。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 設定此檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者選取該字元時，Microsoft Agent 會自動呼叫 Help。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **字元的 [值] 的值** 。 如果 **[值** ] 屬性中有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。

這項設定僅適用于您的用戶端應用程式為最頂端字元的作用中用戶端時。 它不會影響用戶端應用程式所使用之字元或其他字元的其他用戶端。

> [!Note]  
> 建立說明檔需要 Microsoft Windows 說明編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： GetHelpCoNtextID**](iagentcharacterex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




