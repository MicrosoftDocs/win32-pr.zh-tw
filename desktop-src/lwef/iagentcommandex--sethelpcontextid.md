---
title: IAgentCommandEx SetHelpCoNtextID
description: IAgentCommandEx SetHelpCoNtextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966457"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="0d720-103">IAgentCommandEx::SetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="0d720-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="0d720-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0d720-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="0d720-105">設定 [**Command**](/windows/desktop/lwef/the-command-object)物件 [**的提供物件**](helpcontextid-property-com.md)。</span><span class="sxs-lookup"><span data-stu-id="0d720-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="0d720-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0d720-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d720-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span><span class="sxs-lookup"><span data-stu-id="0d720-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="0d720-108">與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="0d720-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="0d720-109">如果您已為您的應用程式建立 Windows 說明檔，並在字元的 [協助工具 [**] 屬性中**](helpfile-property.md) 進行設定。</span><span class="sxs-lookup"><span data-stu-id="0d720-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="0d720-110">當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，Microsoft Agent 會自動呼叫 Help。</span><span class="sxs-lookup"><span data-stu-id="0d720-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="0d720-111">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property-com.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="0d720-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="0d720-112">目前的內容編號是 **命令的值** 為的值。</span><span class="sxs-lookup"><span data-stu-id="0d720-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="0d720-113">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="0d720-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0d720-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d720-114">See Also</span></span>

<span data-ttu-id="0d720-115">[**IAgentCommandEx：： GetHelpCoNtextID**](iagentcommandex--gethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="0d720-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 