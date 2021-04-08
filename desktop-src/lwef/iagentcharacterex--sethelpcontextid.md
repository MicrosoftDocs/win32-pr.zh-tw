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
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="0d420-103">IAgentCharacterEx::SetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="0d420-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="0d420-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0d420-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="0d420-105">設定字元 [**的提供。**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="0d420-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="0d420-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0d420-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d420-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="0d420-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="0d420-108">與字元相關聯之說明主題的內容編號;用來為字元提供即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="0d420-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0d420-109">如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 設定此檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者選取該字元時，Microsoft Agent 會自動呼叫 Help。</span><span class="sxs-lookup"><span data-stu-id="0d420-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="0d420-110">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="0d420-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="0d420-111">目前的內容編號是 **字元的 [值] 的值** 。</span><span class="sxs-lookup"><span data-stu-id="0d420-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="0d420-112">如果 **[值** ] 屬性中有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。</span><span class="sxs-lookup"><span data-stu-id="0d420-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="0d420-113">這項設定僅適用于您的用戶端應用程式為最頂端字元的作用中用戶端時。</span><span class="sxs-lookup"><span data-stu-id="0d420-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="0d420-114">它不會影響用戶端應用程式所使用之字元或其他字元的其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="0d420-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="0d420-115">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="0d420-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0d420-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d420-116">See Also</span></span>

<span data-ttu-id="0d420-117">[**IAgentCharacterEx：： GetHelpCoNtextID**](iagentcharacterex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="0d420-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




