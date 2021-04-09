---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022034"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="a35c8-103">IAgentBalloon::GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="a35c8-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="a35c8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a35c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="a35c8-105">抓取文字球中顯示的每一行字元平均字元數的值。</span><span class="sxs-lookup"><span data-stu-id="a35c8-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="a35c8-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="a35c8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a35c8-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="a35c8-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="a35c8-108">接收每行字元數的變數位址。</span><span class="sxs-lookup"><span data-stu-id="a35c8-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="a35c8-109">Microsoft 代理程式伺服器會自動將顯示在文字氣球中的語音輸出行滾動。</span><span class="sxs-lookup"><span data-stu-id="a35c8-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="a35c8-110">在 Microsoft Agent 字元編輯器中，會定義字元字提示字元的每一行字元平均字元數。</span><span class="sxs-lookup"><span data-stu-id="a35c8-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a35c8-111">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="a35c8-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="a35c8-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a35c8-112">See Also</span></span>

[<span data-ttu-id="a35c8-113">**IAgentBalloon::GetNumLines**</span><span class="sxs-lookup"><span data-stu-id="a35c8-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




