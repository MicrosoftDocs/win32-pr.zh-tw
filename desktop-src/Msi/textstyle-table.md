---
description: 文字文字表格會列出具有文字的控制項中所使用的不同字型樣式。
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: 樣式表單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943568"
---
# <a name="textstyle-table"></a><span data-ttu-id="8e86e-103">樣式表單</span><span class="sxs-lookup"><span data-stu-id="8e86e-103">TextStyle Table</span></span>

<span data-ttu-id="8e86e-104">文字文字表格會列出具有文字的控制項中所使用的不同字型樣式。</span><span class="sxs-lookup"><span data-stu-id="8e86e-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="8e86e-105">TextStyle 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="8e86e-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="8e86e-106">Column</span><span class="sxs-lookup"><span data-stu-id="8e86e-106">Column</span></span>    | <span data-ttu-id="8e86e-107">類型</span><span class="sxs-lookup"><span data-stu-id="8e86e-107">Type</span></span>                               | <span data-ttu-id="8e86e-108">答案</span><span class="sxs-lookup"><span data-stu-id="8e86e-108">Key</span></span> | <span data-ttu-id="8e86e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e86e-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="8e86e-110">文本</span><span class="sxs-lookup"><span data-stu-id="8e86e-110">TextStyle</span></span> | [<span data-ttu-id="8e86e-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="8e86e-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="8e86e-112">Y</span><span class="sxs-lookup"><span data-stu-id="8e86e-112">Y</span></span>   | <span data-ttu-id="8e86e-113">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-113">N</span></span>        |
| <span data-ttu-id="8e86e-114">FaceName</span><span class="sxs-lookup"><span data-stu-id="8e86e-114">FaceName</span></span>  | [<span data-ttu-id="8e86e-115">Text</span><span class="sxs-lookup"><span data-stu-id="8e86e-115">Text</span></span>](text.md)                   | <span data-ttu-id="8e86e-116">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-116">N</span></span>   | <span data-ttu-id="8e86e-117">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-117">N</span></span>        |
| <span data-ttu-id="8e86e-118">大小</span><span class="sxs-lookup"><span data-stu-id="8e86e-118">Size</span></span>      | [<span data-ttu-id="8e86e-119">整數</span><span class="sxs-lookup"><span data-stu-id="8e86e-119">Integer</span></span>](integer.md)             | <span data-ttu-id="8e86e-120">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-120">N</span></span>   | <span data-ttu-id="8e86e-121">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-121">N</span></span>        |
| <span data-ttu-id="8e86e-122">Color</span><span class="sxs-lookup"><span data-stu-id="8e86e-122">Color</span></span>     | [<span data-ttu-id="8e86e-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="8e86e-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="8e86e-124">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-124">N</span></span>   | <span data-ttu-id="8e86e-125">Y</span><span class="sxs-lookup"><span data-stu-id="8e86e-125">Y</span></span>        |
| <span data-ttu-id="8e86e-126">StyleBits</span><span class="sxs-lookup"><span data-stu-id="8e86e-126">StyleBits</span></span> | [<span data-ttu-id="8e86e-127">整數</span><span class="sxs-lookup"><span data-stu-id="8e86e-127">Integer</span></span>](integer.md)             | <span data-ttu-id="8e86e-128">N</span><span class="sxs-lookup"><span data-stu-id="8e86e-128">N</span></span>   | <span data-ttu-id="8e86e-129">Y</span><span class="sxs-lookup"><span data-stu-id="8e86e-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8e86e-130">資料行</span><span class="sxs-lookup"><span data-stu-id="8e86e-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8e86e-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>文本</span><span class="sxs-lookup"><span data-stu-id="8e86e-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="8e86e-132">此資料行是字型樣式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e86e-132">This column is the name of the font style.</span></span> <span data-ttu-id="8e86e-133">這個名稱可以內嵌在文字字串中，以表示樣式變更。</span><span class="sxs-lookup"><span data-stu-id="8e86e-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="8e86e-134">請注意，此欄位中使用的字型樣式名稱不能以字元： \_ UL 結尾。</span><span class="sxs-lookup"><span data-stu-id="8e86e-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="8e86e-135">請參閱 [加入控制項和文字](adding-controls-and-text.md)。</span><span class="sxs-lookup"><span data-stu-id="8e86e-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e86e-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span><span class="sxs-lookup"><span data-stu-id="8e86e-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="8e86e-137">指出字型名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="8e86e-137">A string indicating the name of the font.</span></span> <span data-ttu-id="8e86e-138">字串的長度不能超過31個字元。</span><span class="sxs-lookup"><span data-stu-id="8e86e-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="8e86e-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>大小</span><span class="sxs-lookup"><span data-stu-id="8e86e-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="8e86e-140">以點為單位的字型大小。</span><span class="sxs-lookup"><span data-stu-id="8e86e-140">The font size measured in points.</span></span> <span data-ttu-id="8e86e-141">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="8e86e-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="8e86e-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>顏色</span><span class="sxs-lookup"><span data-stu-id="8e86e-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="8e86e-143">這個資料行會指定 [文字控制項](text-control.md)所顯示的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="8e86e-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="8e86e-144">所有其他類型的控制項一律會使用預設的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="8e86e-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="8e86e-145">此資料行中的值應該使用下列公式來計算： 65536 \* blue + 256 \* 綠 + red，其中的紅色、綠色和藍色都在0-255 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="8e86e-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="8e86e-146">值不得超過16777215，這是白色的值。</span><span class="sxs-lookup"><span data-stu-id="8e86e-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="8e86e-147">黑色的值為0、紅色為255、紅色為65280、綠色為、紅色為16711680、藍色和8421504。</span><span class="sxs-lookup"><span data-stu-id="8e86e-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="8e86e-148">將欄位保持空白會指定預設色彩。</span><span class="sxs-lookup"><span data-stu-id="8e86e-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="8e86e-149">請勿將透明 [文字控制項](text-control.md) 放在彩色點陣圖上方。</span><span class="sxs-lookup"><span data-stu-id="8e86e-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="8e86e-150">如果使用者變更顯示色彩配置，可能看不到文字。</span><span class="sxs-lookup"><span data-stu-id="8e86e-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="8e86e-151">例如，如果使用者設定協助工具的高對比參數，文字可能會變成隱藏。</span><span class="sxs-lookup"><span data-stu-id="8e86e-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="8e86e-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span><span class="sxs-lookup"><span data-stu-id="8e86e-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="8e86e-153">位的組合，表示文字的格式。</span><span class="sxs-lookup"><span data-stu-id="8e86e-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="8e86e-154">個別的樣式位具有下列值。</span><span class="sxs-lookup"><span data-stu-id="8e86e-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="8e86e-155">常數</span><span class="sxs-lookup"><span data-stu-id="8e86e-155">Constant</span></span>                             | <span data-ttu-id="8e86e-156">十六進位</span><span class="sxs-lookup"><span data-stu-id="8e86e-156">Hexadecimal</span></span> | <span data-ttu-id="8e86e-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="8e86e-157">Decimal</span></span> | <span data-ttu-id="8e86e-158">樣式</span><span class="sxs-lookup"><span data-stu-id="8e86e-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="8e86e-159">**msidbTextStyleStyleBitsBold**</span><span class="sxs-lookup"><span data-stu-id="8e86e-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="8e86e-160">0x001</span><span class="sxs-lookup"><span data-stu-id="8e86e-160">0x001</span></span>       | <span data-ttu-id="8e86e-161">1</span><span class="sxs-lookup"><span data-stu-id="8e86e-161">1</span></span>       | <span data-ttu-id="8e86e-162">粗體</span><span class="sxs-lookup"><span data-stu-id="8e86e-162">Bold</span></span>       |
| <span data-ttu-id="8e86e-163">**msidbTextStyleStyleBitsItalic**</span><span class="sxs-lookup"><span data-stu-id="8e86e-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="8e86e-164">0x002</span><span class="sxs-lookup"><span data-stu-id="8e86e-164">0x002</span></span>       | <span data-ttu-id="8e86e-165">2</span><span class="sxs-lookup"><span data-stu-id="8e86e-165">2</span></span>       | <span data-ttu-id="8e86e-166">斜體</span><span class="sxs-lookup"><span data-stu-id="8e86e-166">Italic</span></span>     |
| <span data-ttu-id="8e86e-167">**msidbTextStyleStyleBitsUnderline**</span><span class="sxs-lookup"><span data-stu-id="8e86e-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="8e86e-168">0x004</span><span class="sxs-lookup"><span data-stu-id="8e86e-168">0x004</span></span>       | <span data-ttu-id="8e86e-169">4</span><span class="sxs-lookup"><span data-stu-id="8e86e-169">4</span></span>       | <span data-ttu-id="8e86e-170">Underline</span><span class="sxs-lookup"><span data-stu-id="8e86e-170">Underline</span></span>  |
| <span data-ttu-id="8e86e-171">**msidbTextStyleStyleBitsStrike**</span><span class="sxs-lookup"><span data-stu-id="8e86e-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="8e86e-172">0x008</span><span class="sxs-lookup"><span data-stu-id="8e86e-172">0x008</span></span>       | <span data-ttu-id="8e86e-173">8</span><span class="sxs-lookup"><span data-stu-id="8e86e-173">8</span></span>       | <span data-ttu-id="8e86e-174">刪除</span><span class="sxs-lookup"><span data-stu-id="8e86e-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8e86e-175">驗證</span><span class="sxs-lookup"><span data-stu-id="8e86e-175">Validation</span></span>

<dl>

[<span data-ttu-id="8e86e-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="8e86e-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8e86e-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="8e86e-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8e86e-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="8e86e-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="8e86e-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="8e86e-179">ICE45</span></span>](ice45.md)  
</dl>

 

 



