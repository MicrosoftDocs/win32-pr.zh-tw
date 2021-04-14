---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375036"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="f98d0-103">IAgentCommands::SetCaption</span><span class="sxs-lookup"><span data-stu-id="f98d0-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="f98d0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f98d0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="f98d0-105">設定針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合顯示的 [**標題**](caption-property.md)文字。</span><span class="sxs-lookup"><span data-stu-id="f98d0-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="f98d0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f98d0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f98d0-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="f98d0-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="f98d0-108">指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Caption**](caption-property.md)屬性值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="f98d0-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="f98d0-109">設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性，可定義當其 [**Visible**](visible-property.md)屬性設定為 **True** ，且您的應用程式不是輸入-主動用戶端時，它會在字元的快顯功能表上顯示的方式。</span><span class="sxs-lookup"><span data-stu-id="f98d0-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="f98d0-110">若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。</span><span class="sxs-lookup"><span data-stu-id="f98d0-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="f98d0-111">如果您針對已設定 [**標題**](caption-property.md)的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合定義命令，您通常也會定義其 **命令** 集合的 **標題**。</span><span class="sxs-lookup"><span data-stu-id="f98d0-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="f98d0-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f98d0-112">See Also</span></span>

<span data-ttu-id="f98d0-113">[**IAgentCommands：： GetCaption**](iagentcommands--getcaption.md)、 [**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)、 [**IAgentCommands：： SetVoice**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="f98d0-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 