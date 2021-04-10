---
title: IAgentCharacterEx GetHelpFileName
description: IAgentCharacterEx GetHelpFileName
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932415"
---
# <a name="iagentcharacterexgethelpfilename"></a><span data-ttu-id="8a638-103">IAgentCharacterEx::GetHelpFileName</span><span class="sxs-lookup"><span data-stu-id="8a638-103">IAgentCharacterEx::GetHelpFileName</span></span>

<span data-ttu-id="8a638-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8a638-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

<span data-ttu-id="8a638-105">抓取字元的 HelpFileName。</span><span class="sxs-lookup"><span data-stu-id="8a638-105">Retrieves the HelpFileName for a character.</span></span>

-   <span data-ttu-id="8a638-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8a638-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8a638-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="8a638-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="8a638-108">接收字元之說明文件名的變數位址。</span><span class="sxs-lookup"><span data-stu-id="8a638-108">Address of a variable that receives the Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="8a638-109">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md) 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者按一下該字元或從快顯功能表中選取命令時，Microsoft Agent 會自動呼叫 Help。</span><span class="sxs-lookup"><span data-stu-id="8a638-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="8a638-110">如果所選 [**命令的 [值] 屬性中**](helpcontextid-property.md) 有內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。</span><span class="sxs-lookup"><span data-stu-id="8a638-110">If there is a context number in the selected command's [**HelpContextID**](helpcontextid-property.md) property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="8a638-111">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="8a638-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="8a638-112">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="8a638-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8a638-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a638-113">See Also</span></span>

<span data-ttu-id="8a638-114">[**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)、 [**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="8a638-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




