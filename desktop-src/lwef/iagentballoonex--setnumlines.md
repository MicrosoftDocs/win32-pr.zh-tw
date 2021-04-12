---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462376"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="157bd-103">IAgentBalloonEx::SetNumLines</span><span class="sxs-lookup"><span data-stu-id="157bd-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="157bd-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="157bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="157bd-105">設定可在字元的文字氣球中顯示的文字輸出行數。</span><span class="sxs-lookup"><span data-stu-id="157bd-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="157bd-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="157bd-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="157bd-107">\_如果參數為零，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="157bd-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="157bd-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span><span class="sxs-lookup"><span data-stu-id="157bd-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="157bd-109">要在文字提示中顯示的行數。</span><span class="sxs-lookup"><span data-stu-id="157bd-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="157bd-110">最小設定為1，最大值為128。</span><span class="sxs-lookup"><span data-stu-id="157bd-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="157bd-111">如果 [**說話**](speak-method.md) 或 [**考慮**](think-method.md) 方法中指定的文字超過目前的球標大小，則代理程式會自動滾動氣球中的文字。</span><span class="sxs-lookup"><span data-stu-id="157bd-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="157bd-112">如果設定了 **SizeToText** 氣球樣式位，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="157bd-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="157bd-113">當使用 Microsoft 代理程式字元編輯器來編譯字元時，預設設定會以設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="157bd-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="157bd-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="157bd-114">See Also</span></span>

<span data-ttu-id="157bd-115">[**IAgentBalloon：： GetNumLines**](iagentballoon--getnumlines.md)、 [**IAgentBalloonEx：： GetStyle**](iagentballoonex--getstyle.md)、 [**IAgentBalloonEx：： >setstyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="157bd-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




