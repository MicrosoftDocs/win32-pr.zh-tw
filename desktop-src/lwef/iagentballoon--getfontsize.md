---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184146"
---
# <a name="iagentballoongetfontsize"></a><span data-ttu-id="e7d47-103">IAgentBalloon::GetFontSize</span><span class="sxs-lookup"><span data-stu-id="e7d47-103">IAgentBalloon::GetFontSize</span></span>

<span data-ttu-id="e7d47-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e7d47-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

<span data-ttu-id="e7d47-105">抓取文字氣球中所顯示字型大小的值。</span><span class="sxs-lookup"><span data-stu-id="e7d47-105">Retrieves the value for the size of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="e7d47-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="e7d47-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e7d47-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="e7d47-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="e7d47-108">接收字型大小之值的位址。</span><span class="sxs-lookup"><span data-stu-id="e7d47-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="e7d47-109">在「Microsoft 代理程式字元編輯器」中定義字元字組氣球中使用的預設字型大小。</span><span class="sxs-lookup"><span data-stu-id="e7d47-109">The default font size used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e7d47-110">您可以使用 [**IAgentBalloon：： SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**)來變更它。</span><span class="sxs-lookup"><span data-stu-id="e7d47-110">You can change it with [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span></span> <span data-ttu-id="e7d47-111">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型大小設定。</span><span class="sxs-lookup"><span data-stu-id="e7d47-111">However, the user can override the font size settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




