---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372295"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="5a5da-103">IAgentCommandsEx::GetFontSize</span><span class="sxs-lookup"><span data-stu-id="5a5da-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="5a5da-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5a5da-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="5a5da-105">抓取字元的快顯功能表中所顯示字型的大小值。</span><span class="sxs-lookup"><span data-stu-id="5a5da-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="5a5da-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="5a5da-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5a5da-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="5a5da-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="5a5da-108">接收字型大小之值的位址。</span><span class="sxs-lookup"><span data-stu-id="5a5da-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="5a5da-109">當您的用戶端為輸入-主動時，所傳回字型的點大小會對應到在字元的快顯功能表中顯示文字的大小。</span><span class="sxs-lookup"><span data-stu-id="5a5da-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="5a5da-110">字型設定的預設值是根據字元語言識別項設定的功能表字型設定，如果未設定，則是使用者預設語言設定。</span><span class="sxs-lookup"><span data-stu-id="5a5da-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="5a5da-111">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5a5da-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a5da-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a5da-112">See Also</span></span>

<span data-ttu-id="5a5da-113">[**IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)、 [ **IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="5a5da-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




