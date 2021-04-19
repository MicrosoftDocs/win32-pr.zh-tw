---
title: IAgentBalloonEx >setstyle
description: IAgentBalloonEx >setstyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967855"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="0aab3-103">IAgentBalloonEx：： >setstyle</span><span class="sxs-lookup"><span data-stu-id="0aab3-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="0aab3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0aab3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="0aab3-105">抓取字元的文字球標樣式設定。</span><span class="sxs-lookup"><span data-stu-id="0aab3-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="0aab3-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0aab3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0aab3-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span><span class="sxs-lookup"><span data-stu-id="0aab3-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="0aab3-108">文字氣球的樣式設定，可以是下列任何值的組合：</span><span class="sxs-lookup"><span data-stu-id="0aab3-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="0aab3-109">值</span><span class="sxs-lookup"><span data-stu-id="0aab3-109">Value</span></span>                                                                            | <span data-ttu-id="0aab3-110">描述</span><span class="sxs-lookup"><span data-stu-id="0aab3-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0aab3-111">**const 不帶正負號的簡短\*\*\*\*氣球 \_ 樣式 \_ BALLOONON = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="0aab3-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="0aab3-112">提示支援輸出。</span><span class="sxs-lookup"><span data-stu-id="0aab3-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="0aab3-113">**const 不帶正負號的簡短\*\*\*\*氣球 \_ 樣式 \_ SIZETOTEXT = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="0aab3-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="0aab3-114">氣球的高度會調整大小以容納文字輸出。</span><span class="sxs-lookup"><span data-stu-id="0aab3-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="0aab3-115">**const 不帶正負號的簡短\*\*\*\*氣球 \_ 樣式自動 \_ 隱藏 = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="0aab3-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="0aab3-116">提示會自動隱藏。</span><span class="sxs-lookup"><span data-stu-id="0aab3-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="0aab3-117">**const 不帶正負號的簡短\*\*\*\*氣球 \_ 樣式 \_ AUTOPACE = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="0aab3-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="0aab3-118">文字輸出的進度是根據輸出速率。</span><span class="sxs-lookup"><span data-stu-id="0aab3-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="0aab3-119">當設定 **BalloonOn** 樣式位時，除非使用者覆寫 Microsoft Agent 屬性工作表中的顯示，否則會在使用「 [**說話**](speak-method.md) 」或「 [**想法**](think-method.md) 」方法時出現文字提示。</span><span class="sxs-lookup"><span data-stu-id="0aab3-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0aab3-120">未設定時，不會出現任何氣球。</span><span class="sxs-lookup"><span data-stu-id="0aab3-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="0aab3-121">當設定 **SizeToText** 樣式位時，文字批註會自動將球的高度調整為 [**說**](speak-method.md) 出或 [**考慮**](think-method.md) 方法中所指定文字的目前大小。</span><span class="sxs-lookup"><span data-stu-id="0aab3-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="0aab3-122">若未設定，則氣球的高度會以球的 [行數] 屬性設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="0aab3-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="0aab3-123">此樣式位設定為1，而且嘗試使用 [**IAgentBalloonEx：： SetNumLines**](iagentballoonex--setnumlines.md) 將會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="0aab3-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="0aab3-124">設定自動 **隱藏** 樣式位時，會在短時間之後自動隱藏文字提示。</span><span class="sxs-lookup"><span data-stu-id="0aab3-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="0aab3-125">若未設定，則會顯示氣球，直到新的 [**說話**](speak-method.md) 或 [**思考**](think-method.md) 通話、隱藏字元或使用者按一下或拖曳字元為止。</span><span class="sxs-lookup"><span data-stu-id="0aab3-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="0aab3-126">當設定 **AutoPace** 樣式位時，文字氣球會根據目前的輸出速率來步調輸出，例如一次一個單字。</span><span class="sxs-lookup"><span data-stu-id="0aab3-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="0aab3-127">當輸出超過球的大小時，就會自動滾動先前的文字。</span><span class="sxs-lookup"><span data-stu-id="0aab3-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="0aab3-128">若未設定，則會同時顯示 [**說**](speak-method.md) 出或 [**考慮**](think-method.md) 語句中包含的所有文字。</span><span class="sxs-lookup"><span data-stu-id="0aab3-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="0aab3-129">您可以設定球標的樣式屬性，即使使用者已使用 Microsoft Agent 屬性工作表來停用氣球的顯示。</span><span class="sxs-lookup"><span data-stu-id="0aab3-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="0aab3-130">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="0aab3-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="0aab3-131">當使用 Microsoft Agent 字元編輯器來編譯字元時，這些樣式位的預設值會以其設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="0aab3-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="0aab3-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aab3-132">See Also</span></span>

[<span data-ttu-id="0aab3-133">**IAgentBalloonEx::GetStyle**</span><span class="sxs-lookup"><span data-stu-id="0aab3-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





