---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9852e5909410f7e51789dd92419af4ef12f11ab0ae7ad0729a26b96a06fe34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477946"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx::SetHelpFileName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

設定字元的 HelpFileName。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

字元的說明文件名。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md)則當 [**HelpModeOn**](helpmodeon-property.md)設定為 **True** ，且使用者按一下該字元或從快顯功能表中選取命令時，Microsoft Agent 會自動呼叫 help。 如果所選 [**命令的 [值] 屬性中**](helpcontextid-property.md) 有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 建立說明檔需要 Microsoft Windows help 編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




