---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969043"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="b61fe-103">IAgentBalloon::GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="b61fe-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="b61fe-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b61fe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="b61fe-105">指出文字氣球中使用的字型是否為斜體。</span><span class="sxs-lookup"><span data-stu-id="b61fe-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="b61fe-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="b61fe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b61fe-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span><span class="sxs-lookup"><span data-stu-id="b61fe-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="b61fe-108">值的位址，如果字型為斜體，則為 **True** ，如果不是斜體，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="b61fe-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="b61fe-109">字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="b61fe-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b61fe-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="b61fe-110">It cannot be changed by an application.</span></span> <span data-ttu-id="b61fe-111">不過，使用者可以透過 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="b61fe-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




