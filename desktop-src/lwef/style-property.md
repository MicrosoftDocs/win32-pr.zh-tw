---
title: Style 屬性
description: Style 屬性
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300915"
---
# <a name="style-property"></a><span data-ttu-id="1944e-103">Style 屬性</span><span class="sxs-lookup"><span data-stu-id="1944e-103">Style Property</span></span>

<span data-ttu-id="1944e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1944e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1944e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="1944e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1944e-106">傳回或設定字元的文字球標輸出樣式。</span><span class="sxs-lookup"><span data-stu-id="1944e-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="1944e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="1944e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1944e-108">*代理程式。\*\*\*字元 (*\*\* 」CharacterID \* \* \* ) 。球形\* 樣式 \*  \[  =  *樣式*\]</span><span class="sxs-lookup"><span data-stu-id="1944e-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="1944e-109">部分</span><span class="sxs-lookup"><span data-stu-id="1944e-109">Part</span></span>    | <span data-ttu-id="1944e-110">描述</span><span class="sxs-lookup"><span data-stu-id="1944e-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1944e-111">*Style*</span><span class="sxs-lookup"><span data-stu-id="1944e-111">*Style*</span></span> | <span data-ttu-id="1944e-112">表示球的輸出樣式的整數。</span><span class="sxs-lookup"><span data-stu-id="1944e-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="1944e-113">樣式設定是位在的位位，其中的位會對應至：球形 (位 0) 、大小為文字 (位 1) 、自動隱藏 (位 2) 、自動步調 (位 3) 、每行字元數 (位 16-23) ，以及 (位 24-31) 的行數。</span><span class="sxs-lookup"><span data-stu-id="1944e-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1944e-114">備註</span><span class="sxs-lookup"><span data-stu-id="1944e-114">Remarks</span></span>

<span data-ttu-id="1944e-115">當氣球 on 樣式位設定為1時，除非使用者在 Microsoft Agent 屬性工作表中覆寫此設定，否則會在使用 [**說話**](https://www.bing.com/search?q=**Speak**) 或 [**考慮**](think-method.md) 方法時出現文字批註。</span><span class="sxs-lookup"><span data-stu-id="1944e-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="1944e-116">當設定為0時，不會出現球形。</span><span class="sxs-lookup"><span data-stu-id="1944e-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="1944e-117">當 [大小到文字] 樣式位設定為1時，[文字] 氣球會自動將球的高度大小調整為 [ [**朗讀**](https://www.bing.com/search?q=**Speak**) ] 或 [ [**想像**](think-method.md) ] 語句的文字目前大小。</span><span class="sxs-lookup"><span data-stu-id="1944e-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="1944e-118">當設定為0時，氣球的高度會以 [**NumberOfLines**](numberoflines-property.md) 屬性設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="1944e-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="1944e-119">如果此樣式位設定為1，而您嘗試設定 **NumberOfLines** 屬性，則代理程式會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="1944e-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="1944e-120">當自動隱藏樣式位設定為1時，當語音輸出完成時，會自動隱藏文字球。</span><span class="sxs-lookup"><span data-stu-id="1944e-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="1944e-121">當設定為0時，氣球會保持顯示，直到下一個 [**說話**](https://www.bing.com/search?q=**Speak**) 或 [**思考**](think-method.md) 呼叫、隱藏字元或使用者按一下或拖曳字元為止。</span><span class="sxs-lookup"><span data-stu-id="1944e-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="1944e-122">當自動步調樣式位設定為1時，文字氣球會根據目前的輸出速率步調輸出，例如一次一個單字。</span><span class="sxs-lookup"><span data-stu-id="1944e-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="1944e-123">當輸出超過球的大小時，就會自動滾動先前的文字。</span><span class="sxs-lookup"><span data-stu-id="1944e-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="1944e-124">當設定為0時，會一次顯示 [**說**](https://www.bing.com/search?q=**Speak**) 出或 [**考慮**](think-method.md) 語句中包含的所有文字。</span><span class="sxs-lookup"><span data-stu-id="1944e-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="1944e-125">表示只抓取底部四個位的值，**以及\*\*\*\*樣式** 與255所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="1944e-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="1944e-126">設定位值， **或** 以您要設定之位的值傳回的值。</span><span class="sxs-lookup"><span data-stu-id="1944e-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="1944e-127">若要關閉一點， **以及** 以一補數的值傳回的值：</span><span class="sxs-lookup"><span data-stu-id="1944e-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="1944e-128">**Style** 屬性也會傳回上方單字的下個位元組中的字元數，以及上方單字之高位位元組中的行數。</span><span class="sxs-lookup"><span data-stu-id="1944e-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="1944e-129">雖然使用 [**CharsPerLine**](charsperline-property.md) 和 [**NumberOfLines**](numberoflines-property.md)屬性可以更輕鬆地閱讀，但是 **Style** 屬性也可讓您設定這些值。</span><span class="sxs-lookup"><span data-stu-id="1944e-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="1944e-130">例如，若要變更行數，請在將新值設定為新值時間 2 ^ 24 的乘積之前，先清除位24到 31 **，然後再** 將新值設定為新值 **（property）的現有** 值。</span><span class="sxs-lookup"><span data-stu-id="1944e-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="1944e-131">若要設定每行的字元數，請在將新值設定為新值時間 2 ^ 16 的產品，然後將新值新增至 Style 屬性的現有值之前，先清除位16到23（具有邏輯 **AND** 運算）。</span><span class="sxs-lookup"><span data-stu-id="1944e-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="1944e-132">即使使用者已使用 Microsoft Agent 屬性工作表停用氣球顯示，也可以設定 **樣式** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1944e-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="1944e-133">不過，行數的值必須介於1到128之間，且每行的數位字元必須介於8到255之間。</span><span class="sxs-lookup"><span data-stu-id="1944e-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="1944e-134">如果您為 **Style** 屬性提供不正確值，Agent 將會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="1944e-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="1944e-135">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1944e-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="1944e-136">當使用 Microsoft Agent 字元編輯器來編譯字元時，這些樣式位的預設值會以其設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="1944e-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




