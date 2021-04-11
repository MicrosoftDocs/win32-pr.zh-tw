---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023310"
---
# <a name="iagentcommandexsetvoicecaption"></a><span data-ttu-id="26ec7-103">IAgentCommandEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="26ec7-103">IAgentCommandEx::SetVoiceCaption</span></span>

<span data-ttu-id="26ec7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="26ec7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="26ec7-105">設定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示的 [**VoiceCaption**](voicecaption-property.md)文字。</span><span class="sxs-lookup"><span data-stu-id="26ec7-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="26ec7-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="26ec7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="26ec7-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="26ec7-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="26ec7-108">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**VoiceCaption**](voicecaption-property.md)屬性文字的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="26ec7-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="26ec7-109">如果您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="26ec7-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="26ec7-110">當您的用戶端應用程式為輸入使用中時，此文字會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="26ec7-110">This text will appear in the Voice Commands Window when your client application is input active.</span></span> <span data-ttu-id="26ec7-111">如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="26ec7-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="26ec7-112">未設定 **VoiceCaption** 或屬性時，命令不會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="26ec7-112">When neither the **VoiceCaption** or property is set, the command does not appear in the Voice Commands Window.</span></span>

[<span data-ttu-id="26ec7-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="26ec7-113">**Caption**</span></span>](caption-property.md)

## <a name="see-also"></a><span data-ttu-id="26ec7-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26ec7-114">See Also</span></span>

<span data-ttu-id="26ec7-115">[**IAgentCommand：： GetCaption**](iagentcommand--getcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommandsEx：： AddEx**](iagentcommandsex--addex.md)、 [**IAgentCommandsEx：： InsertEx**](iagentcommandsex--insertex.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="26ec7-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 