---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372296"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="1f8e2-103">IAgentCommandsEx::GetFontName</span><span class="sxs-lookup"><span data-stu-id="1f8e2-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="1f8e2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1f8e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="1f8e2-105">抓取字元快顯功能表中所顯示字型的值。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="1f8e2-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1f8e2-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="1f8e2-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="1f8e2-108">接收字元快顯功能表中所顯示字型名稱的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="1f8e2-109">當您的用戶端應用程式為輸入-主動時，所傳回的字型名稱會對應至在字元的快顯功能表中用來顯示文字的字型。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="1f8e2-110">字型設定的預設值是根據字元語言識別項設定的功能表字型設定，如果未設定，則是使用者預設語言識別項設定。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="1f8e2-111">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1f8e2-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f8e2-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f8e2-112">See Also</span></span>

<span data-ttu-id="1f8e2-113">[**IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)、 [ **IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="1f8e2-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




