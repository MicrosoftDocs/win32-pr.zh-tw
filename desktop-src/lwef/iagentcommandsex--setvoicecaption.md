---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968281"
---
# <a name="iagentcommandsexsetvoicecaption"></a><span data-ttu-id="18e45-103">IAgentCommandsEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="18e45-103">IAgentCommandsEx::SetVoiceCaption</span></span>

<span data-ttu-id="18e45-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="18e45-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="18e45-105">設定針對 [**命令**](/windows/desktop/lwef/the-command-object)物件顯示的 [**VoiceCaption**](voicecaption-property.md)文字。</span><span class="sxs-lookup"><span data-stu-id="18e45-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="18e45-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="18e45-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="18e45-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="18e45-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="18e45-108">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**VoiceCaption**](voicecaption-property.md)屬性文字的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="18e45-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="18e45-109">如果您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="18e45-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="18e45-110">當您的用戶端應用程式為輸入-使用中且字元可見時，此文字會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="18e45-110">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="18e45-111">如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="18e45-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="18e45-112">當 **VoiceCaption** 或 **Caption** 屬性都未設定時，命令不會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="18e45-112">When neither the **VoiceCaption** or **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

## <a name="see-also"></a><span data-ttu-id="18e45-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18e45-113">See Also</span></span>

[<span data-ttu-id="18e45-114">**IAgentCommandsEx::GetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="18e45-114">**IAgentCommandsEx::GetVoiceCaption**</span></span>](iagentcommandsex--getvoicecaption.md)


 

 