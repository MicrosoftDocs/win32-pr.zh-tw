---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183677"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="7116b-103">IAgentBalloon::GetFontBold</span><span class="sxs-lookup"><span data-stu-id="7116b-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="7116b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7116b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="7116b-105">指出文字氣球中使用的字型是否為粗體。</span><span class="sxs-lookup"><span data-stu-id="7116b-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="7116b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="7116b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7116b-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span><span class="sxs-lookup"><span data-stu-id="7116b-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="7116b-108">值的位址，如果字型為粗體，則會收到 **True** ，如果不是粗體，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="7116b-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="7116b-109">字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="7116b-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7116b-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="7116b-110">It cannot be changed by an application.</span></span> <span data-ttu-id="7116b-111">不過，使用者可以透過 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="7116b-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




