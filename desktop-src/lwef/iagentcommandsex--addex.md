---
title: IAgentCommandsEx AddEx
description: IAgentCommandsEx AddEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682016"
---
# <a name="iagentcommandsexaddex"></a>IAgentCommandsEx::AddEx

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

將 [**命令**](/windows/desktop/lwef/the-command-object) 加入至 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

指定針對 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR。

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字設定值的 BSTR。

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

指定針對 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**VoiceCaption**](voicecaption-property.md)文字值的 BSTR。

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

布林運算式，指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)的 [**啟用**](enabled-property.md)設定。 如果參數為 **True**，則會啟用並選取 **命令** ;如果 **為 False**，則表示 **命令** 已停用。

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)之 [**可見**](visible-property.md)設定的布林運算式。 如果參數為 **True**，則在字元的快顯功能表中會顯示 **命令** (如果 [**Caption**](caption-property.md) 屬性也設定為) 。

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

接收已新增 [**命令**](/windows/desktop/lwef/the-command-object)之識別碼的變數位址。

</dd> </dl>

[**IAgentCommandsEx：： AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**)藉由包含 [[**上下文**](helpcontextid-property.md)屬性] 來擴充 [**IAgentCommands：： Add**](iagentcommands--add.md) 。 您也可以使用 [ **IAgentCommandsEx：： SetHelpCoNtextID** 來設定屬性。](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommandsEx：： InsertEx**](iagentcommandsex--insertex.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)


 

 