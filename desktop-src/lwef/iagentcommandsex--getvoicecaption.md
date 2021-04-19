---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966445"
---
# <a name="iagentcommandsexgetvoicecaption"></a><span data-ttu-id="bb798-103">IAgentCommandsEx::GetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="bb798-103">IAgentCommandsEx::GetVoiceCaption</span></span>

<span data-ttu-id="bb798-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bb798-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

<span data-ttu-id="bb798-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**VoiceCaption**](voicecaption-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="bb798-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="bb798-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="bb798-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bb798-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="bb798-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="bb798-108">接收針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="bb798-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="bb798-109">傳回的文字是針對 [**命令**](/windows/desktop/lwef/the-command-object) 物件設定的文字，而且當您的用戶端應用程式為輸入-主動時，會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="bb798-109">The text returned is that set for your [**Command**](/windows/desktop/lwef/the-command-object) object and appears in the Voice Commands window when your client application is input-active.</span></span>

<span data-ttu-id="bb798-110">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="bb798-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb798-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb798-111">See Also</span></span>

[<span data-ttu-id="bb798-112">**IAgentCommandsEx::SetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="bb798-112">**IAgentCommandsEx::SetVoiceCaption**</span></span>](iagentcommandsex--setvoicecaption.md)


 

 