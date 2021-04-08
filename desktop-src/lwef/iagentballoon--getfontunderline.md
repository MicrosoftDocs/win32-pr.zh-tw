---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022035"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="b873e-103">IAgentBalloon::GetFontUnderline</span><span class="sxs-lookup"><span data-stu-id="b873e-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="b873e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b873e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="b873e-105">指出文字氣球中使用的字型是否已設定底線樣式。</span><span class="sxs-lookup"><span data-stu-id="b873e-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="b873e-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="b873e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b873e-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span><span class="sxs-lookup"><span data-stu-id="b873e-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="b873e-108">如果設定字型底線樣式，則為值的位址，如果不是 **，則為** **False** 。</span><span class="sxs-lookup"><span data-stu-id="b873e-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="b873e-109">字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="b873e-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b873e-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="b873e-110">It cannot be changed by an application.</span></span> <span data-ttu-id="b873e-111">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="b873e-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




