---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301803"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="a78be-103">IAgentBalloonEx::SetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="a78be-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="a78be-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a78be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="a78be-105">設定可在字元的文字氣球中顯示的每行字元數。</span><span class="sxs-lookup"><span data-stu-id="a78be-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="a78be-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="a78be-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="a78be-107">\_如果參數小於8，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="a78be-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="a78be-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="a78be-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="a78be-109">要在文字提示中顯示的行數。</span><span class="sxs-lookup"><span data-stu-id="a78be-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="a78be-110">最小設定為8，最大值為255。</span><span class="sxs-lookup"><span data-stu-id="a78be-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="a78be-111">如果 [**說話**](speak-method.md) 或 [**考慮**](think-method.md) 方法中指定的文字超過目前的球標大小，則代理程式會自動滾動氣球中的文字。</span><span class="sxs-lookup"><span data-stu-id="a78be-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="a78be-112">當使用 Microsoft 代理程式字元編輯器來編譯字元時，預設設定會以設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="a78be-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="a78be-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a78be-113">See Also</span></span>

[<span data-ttu-id="a78be-114">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="a78be-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




