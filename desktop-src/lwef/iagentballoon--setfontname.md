---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022033"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="513f0-103">IAgentBalloon::SetFontName</span><span class="sxs-lookup"><span data-stu-id="513f0-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="513f0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="513f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="513f0-105">設定出現在文字提示字元中的字型。</span><span class="sxs-lookup"><span data-stu-id="513f0-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="513f0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="513f0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="513f0-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="513f0-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="513f0-108">設定文字氣球中所顯示字型的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="513f0-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="513f0-109">字元的文字氣球中使用的預設字型是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="513f0-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="513f0-110">您可以使用 **IAgentBalloon：： SetFontName** 來變更它。</span><span class="sxs-lookup"><span data-stu-id="513f0-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="513f0-111">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="513f0-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="513f0-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="513f0-112">See Also</span></span>

[<span data-ttu-id="513f0-113">**IAgentBalloon：： GetVisible**</span><span class="sxs-lookup"><span data-stu-id="513f0-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




