---
title: IAgentCommandsEx SetHelpCoNtextID
description: IAgentCommandsEx SetHelpCoNtextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682013"
---
# <a name="iagentcommandsexsethelpcontextid"></a><span data-ttu-id="91ab2-103">IAgentCommandsEx::SetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="91ab2-103">IAgentCommandsEx::SetHelpContextID</span></span>

<span data-ttu-id="91ab2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="91ab2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="91ab2-105">設定 [**Command**](/windows/desktop/lwef/the-command-object)物件 [**的提供物件**](helpcontextid-property.md)。</span><span class="sxs-lookup"><span data-stu-id="91ab2-105">Sets the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="91ab2-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="91ab2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="91ab2-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="91ab2-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="91ab2-108">與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="91ab2-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="91ab2-109">如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 進行設定。</span><span class="sxs-lookup"><span data-stu-id="91ab2-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="91ab2-110">當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，代理程式會自動呼叫 Help。</span><span class="sxs-lookup"><span data-stu-id="91ab2-110">Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="91ab2-111">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="91ab2-111">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="91ab2-112">目前的內容編號是 **命令的值** 為的值。</span><span class="sxs-lookup"><span data-stu-id="91ab2-112">The current context number is the value of **HelpContextID** for the command.</span></span> <span data-ttu-id="91ab2-113">如果所選 **命令的 [值] 屬性中** 有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。</span><span class="sxs-lookup"><span data-stu-id="91ab2-113">If there is a context number in the selected command's **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="91ab2-114">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="91ab2-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="91ab2-115">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="91ab2-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="91ab2-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91ab2-116">See Also</span></span>

<span data-ttu-id="91ab2-117">[**IAgentCommandsEx：： GetHelpCoNtextID**](iagentcommandsex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="91ab2-117">[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 