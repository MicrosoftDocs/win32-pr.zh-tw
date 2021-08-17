---
title: IAgentCommandEx GetHelpCoNtextID
description: IAgentCommandEx GetHelpCoNtextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80f259b10adbdd1460f319b6fda4e5097c11136a5bf7ffde00a11d40a99656a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750183"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpCoNtextID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

如果您已為應用程式建立 Windows 說明檔，並將您的字元 [**的 [**](helpfile-property.md)內容] 內容設定為這個檔案，則當 [**HelpModeOn**](helpmodeon-property.md)設定為 **True** ，且使用者選取命令時，Microsoft 代理程式會自動呼叫 help。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property-com.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **命令的值** 為的值。

> [!Note]  
> 建立說明檔需要 Microsoft Windows help 編譯器。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommandEx：： SetHelpCoNtextID**](iagentcommandex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 