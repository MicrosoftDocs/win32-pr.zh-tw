---
title: IAgentCharacterEx GetHelpCoNtextID
description: IAgentCharacterEx GetHelpCoNtextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674987"
---
# <a name="iagentcharacterexgethelpcontextid"></a><span data-ttu-id="a62ee-103">IAgentCharacterEx::GetHelpCoNtextID</span><span class="sxs-lookup"><span data-stu-id="a62ee-103">IAgentCharacterEx::GetHelpContextID</span></span>

<span data-ttu-id="a62ee-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a62ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

<span data-ttu-id="a62ee-105">抓取字元 [**的提供。**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="a62ee-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="a62ee-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="a62ee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a62ee-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="a62ee-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="a62ee-108">接收字元的說明主題內容編號之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="a62ee-108">Address of a variable that receives the context number of the help topic for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a62ee-109">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md) 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取該字元時，Microsoft Agent 會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="a62ee-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="a62ee-110">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="a62ee-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="a62ee-111">目前的內容編號是 **字元的 [值] 的值** 。</span><span class="sxs-lookup"><span data-stu-id="a62ee-111">The current context number is the value of **HelpContextID** for the character.</span></span>

<span data-ttu-id="a62ee-112">**IAgentCharacterEx：： GetHelpCoNtextID** 會傳回您為字元設定的使用者 [**id**](helpcontextid-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="a62ee-112">**IAgentCharacterEx::GetHelpContextID** returns the [**HelpContextID**](helpcontextid-property.md) you set for the character.</span></span> <span data-ttu-id="a62ee-113">它不會傳回其他用戶端 **所設定的** 比。</span><span class="sxs-lookup"><span data-stu-id="a62ee-113">It does not return the **HelpContextID** set by other clients.</span></span>

> [!Note]  
> <span data-ttu-id="a62ee-114">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="a62ee-114">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a62ee-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a62ee-115">See Also</span></span>

<span data-ttu-id="a62ee-116">[**IAgentCharacterEx：： SetHelpCoNtextID**](iagentcharacterex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="a62ee-116">[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




