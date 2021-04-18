---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f367a7956d1029eae47064a0778264e3b77f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314731"
---
# <a name="iagentcommandexgetvoicecaption"></a><span data-ttu-id="519ce-103">IAgentCommandEx::GetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="519ce-103">IAgentCommandEx::GetVoiceCaption</span></span>

<span data-ttu-id="519ce-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="519ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

<span data-ttu-id="519ce-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**VoiceCaption**](voicecaption-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="519ce-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="519ce-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="519ce-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="519ce-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="519ce-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="519ce-108">接收針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="519ce-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="519ce-109">當您的用戶端應用程式為輸入-主動時， [**VoiceCaption**](voicecaption-property.md) 是在 [語音命令] 視窗中針對 [**命令**](/windows/desktop/lwef/the-command-object) 物件顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="519ce-109">The [**VoiceCaption**](voicecaption-property.md) is the text that appears for a [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="519ce-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="519ce-110">See Also</span></span>

<span data-ttu-id="519ce-111">[**IAgentCommandEx：： SetVoiceCaption**](iagentcommandex--setvoicecaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommandsEx：： AddEx**](iagentcommandsex--addex.md)、 [**IAgentCommandsEx：： InsertEx**](iagentcommandsex--insertex.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="519ce-111">[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 