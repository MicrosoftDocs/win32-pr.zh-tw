---
title: IAgentCharacterEx 考慮
description: IAgentCharacterEx 考慮
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023380"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="f31ed-103">IAgentCharacterEx：：試想</span><span class="sxs-lookup"><span data-stu-id="f31ed-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="f31ed-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f31ed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="f31ed-105">以指定的文字顯示字元的考慮字組氣球。</span><span class="sxs-lookup"><span data-stu-id="f31ed-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="f31ed-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f31ed-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f31ed-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="f31ed-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="f31ed-108">要在字元的考慮氣球中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="f31ed-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="f31ed-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="f31ed-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f31ed-110">接收 **考慮** 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="f31ed-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="f31ed-111">如同 [**IAgentCharacter：：說話**](iagentcharacter--speak.md) 方法， **考慮** 方法是佇列的要求，它會在文字氣球中顯示文字，但想法會顯示在特殊的思考球中。</span><span class="sxs-lookup"><span data-stu-id="f31ed-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="f31ed-112">想像的氣球只支援書簽語音控制項標記 (**\\ Mrk**) 並忽略其他任何語音控制項標記。</span><span class="sxs-lookup"><span data-stu-id="f31ed-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="f31ed-113">不同于 **IAgentCharacter：：說話**， **考慮** 方法不會變更字元的動畫狀態。</span><span class="sxs-lookup"><span data-stu-id="f31ed-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="f31ed-114">[**IAgentBalloon**](/windows/desktop/lwef/iagentballoon)設定也適用于考慮氣球的外觀樣式。</span><span class="sxs-lookup"><span data-stu-id="f31ed-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="f31ed-115">例如，氣球的 [**Enabled**](enabled-property.md) 屬性也必須為 **True** ，才能顯示要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="f31ed-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="f31ed-116">Microsoft Agent 自動斷詞字組會使用空白字元來中斷文字 (例如，空格鍵和 tab) 。</span><span class="sxs-lookup"><span data-stu-id="f31ed-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="f31ed-117">不過，它也可能會中斷文字以容納球。</span><span class="sxs-lookup"><span data-stu-id="f31ed-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="f31ed-118">在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。</span><span class="sxs-lookup"><span data-stu-id="f31ed-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="f31ed-119">使用 [**IAgentCharacterEx：： SetLanguageID**](iagentcharacterex--setlanguageid.md) ，將字元的語言識別項設定為 (，然後再使用 [**IAgentCharacter：：**](iagentcharacter--speak.md) using 方法，以確保文字氣球內適當的文字顯示。</span><span class="sxs-lookup"><span data-stu-id="f31ed-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f31ed-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f31ed-120">See Also</span></span>

<span data-ttu-id="f31ed-121">[**IAgentBalloon：： GetEnabled**](iagentballoon--getenabled.md)、 [**IAgentBalloonEx：： >setstyle**](iagentballoonex--setstyle.md)、 [**IAgentCharacter：：說話**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="f31ed-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 