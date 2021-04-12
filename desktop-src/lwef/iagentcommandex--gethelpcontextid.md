---
title: IAgentCommandEx GetHelpCoNtextID
description: IAgentCommandEx GetHelpCoNtextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375269"
---
# <a name="iagentcommandexgethelpcontextid"></a><span data-ttu-id="66411-103">IAgentCommandEx::GetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="66411-103">IAgentCommandEx::GetHelpContextID</span></span>

<span data-ttu-id="66411-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="66411-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

<span data-ttu-id="66411-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)[**物件的比對。**](helpcontextid-property-com.md)</span><span class="sxs-lookup"><span data-stu-id="66411-105">Retrieves the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="66411-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="66411-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66411-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span><span class="sxs-lookup"><span data-stu-id="66411-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span></span>
</dt> <dd>

<span data-ttu-id="66411-108">變數的位址，此變數會接收與 [**命令**](/windows/desktop/lwef/the-command-object) 物件相關聯之說明主題的內容編號。</span><span class="sxs-lookup"><span data-stu-id="66411-108">Address of a variable that receives the context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="66411-109">如果您已為您的應用程式建立 Windows 說明檔，並將您的字元的 [檔案協助 [**] 屬性設定**](helpfile-property.md) 為這個檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，Microsoft Agent 會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="66411-109">If you've created a Windows Help file for your application and set your character's [**HelpFile**](helpfile-property.md) property to this file, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="66411-110">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property-com.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="66411-110">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="66411-111">目前的內容編號是 **命令的值** 為的值。</span><span class="sxs-lookup"><span data-stu-id="66411-111">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="66411-112">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="66411-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="66411-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66411-113">See Also</span></span>

<span data-ttu-id="66411-114">[**IAgentCommandEx：： SetHelpCoNtextID**](iagentcommandex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="66411-114">[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 