---
title: IAgentCommandsEx GetHelpCoNtextID
description: IAgentCommandsEx GetHelpCoNtextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023394"
---
# <a name="iagentcommandsexgethelpcontextid"></a><span data-ttu-id="1165c-103">IAgentCommandsEx::GetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="1165c-103">IAgentCommandsEx::GetHelpContextID</span></span>

<span data-ttu-id="1165c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1165c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

<span data-ttu-id="1165c-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)[**物件的比對。**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="1165c-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="1165c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1165c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1165c-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="1165c-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="1165c-108">接收 [**命令**](/windows/desktop/lwef/the-command-object) 物件說明主題之內容編號的變數位址。</span><span class="sxs-lookup"><span data-stu-id="1165c-108">Address of a variable that receives the context number of the help topic for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="1165c-109">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md) 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取您的 [**命令**](/windows/desktop/lwef/the-command-object) 物件時，Microsoft Agent 會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="1165c-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects your [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="1165c-110">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="1165c-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="1165c-111">目前的內容編號是 **Command** **物件的 [值] 的值**。</span><span class="sxs-lookup"><span data-stu-id="1165c-111">The current context number is the value of **HelpContextID** for the **Command** object.</span></span>

<span data-ttu-id="1165c-112">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1165c-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="1165c-113">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="1165c-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1165c-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1165c-114">See Also</span></span>

<span data-ttu-id="1165c-115">[**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="1165c-115">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 