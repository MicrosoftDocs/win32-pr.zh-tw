---
title: IAgentCommandEx GetHelpCoNtextID
description: IAgentCommandEx GetHelpCoNtextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375269"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)[**物件的比對。**](helpcontextid-property-com.md)

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

變數的位址，此變數會接收與 [**命令**](/windows/desktop/lwef/the-command-object) 物件相關聯之說明主題的內容編號。

</dd> </dl>

如果您已為您的應用程式建立 Windows 說明檔，並將您的字元的 [檔案協助 [**] 屬性設定**](helpfile-property.md) 為這個檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，Microsoft Agent 會自動呼叫說明。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property-com.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **命令的值** 為的值。

> [!Note]  
> 建立說明檔需要 Microsoft Windows 說明編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommandEx：： SetHelpCoNtextID**](iagentcommandex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 