---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671639"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="11554-103">IAgentCommandsEx::SetFontName</span><span class="sxs-lookup"><span data-stu-id="11554-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="11554-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="11554-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="11554-105">設定在字元的快顯功能表中顯示的字型。</span><span class="sxs-lookup"><span data-stu-id="11554-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="11554-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="11554-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="11554-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="11554-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="11554-108">設定字元快顯功能表中所顯示字型的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="11554-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="11554-109">這個屬性會決定在字元的快顯功能表中用來顯示文字的字型。</span><span class="sxs-lookup"><span data-stu-id="11554-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="11554-110">字型設定的預設值是以字元語言識別項設定的功能表字型設定為基礎，如果未設定則為-使用者預設語言識別項設定。</span><span class="sxs-lookup"><span data-stu-id="11554-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="11554-111">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="11554-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="11554-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11554-112">See Also</span></span>

<span data-ttu-id="11554-113">[**IAgentCommandsEx：： GetFontName**](iagentcommandsex--getfontname.md)、 [**IAgentCommandsEx：： GetFontSize**](iagentcommandsex--getfontsize.md)、 [**IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="11554-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




