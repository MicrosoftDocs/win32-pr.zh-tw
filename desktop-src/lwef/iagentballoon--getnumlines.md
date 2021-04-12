---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372597"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="0d482-103">IAgentBalloon::GetNumLines</span><span class="sxs-lookup"><span data-stu-id="0d482-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="0d482-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0d482-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="0d482-105">抓取文字氣球中顯示的行數值。</span><span class="sxs-lookup"><span data-stu-id="0d482-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="0d482-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0d482-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d482-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span><span class="sxs-lookup"><span data-stu-id="0d482-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="0d482-108">接收所顯示的行數之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="0d482-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="0d482-109">Microsoft 代理程式伺服器會自動將顯示在文字氣球中的語音輸出行滾動。</span><span class="sxs-lookup"><span data-stu-id="0d482-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="0d482-110">字元文字氣球的行數是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="0d482-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0d482-111">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="0d482-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d482-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d482-112">See Also</span></span>

[<span data-ttu-id="0d482-113">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="0d482-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




