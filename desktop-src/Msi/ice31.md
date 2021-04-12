---
description: ICE31 會驗證顯示文字之控制項中所使用的任何預先定義字型樣式。 它也會驗證 DefaultUIFont 屬性是否參考有效的字型樣式。
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193486"
---
# <a name="ice31"></a><span data-ttu-id="845f8-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="845f8-104">ICE31</span></span>

<span data-ttu-id="845f8-105">ICE31 會驗證顯示文字之 [控制項](controls.md) 中所使用的任何預先定義字型樣式。</span><span class="sxs-lookup"><span data-stu-id="845f8-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="845f8-106">它也會驗證 [**DefaultUIFont**](defaultuifont.md) 屬性是否參考有效的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="845f8-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="845f8-107">控制項可以有預先定義的字型樣式，如 [新增控制項和文字](adding-controls-and-text.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="845f8-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="845f8-108">若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。</span><span class="sxs-lookup"><span data-stu-id="845f8-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="845f8-109">其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="845f8-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="845f8-110">如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。</span><span class="sxs-lookup"><span data-stu-id="845f8-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="845f8-111">ICE31 會檢查 [控制項資料表](control-table.md) 中每個控制項的文字資料行，以確認文字文字 [資料表](textstyle-table.md)中有有效的專案。</span><span class="sxs-lookup"><span data-stu-id="845f8-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="845f8-112">ICE31 會忽略 [ScrollableText 控制項](scrollabletext-control.md)。</span><span class="sxs-lookup"><span data-stu-id="845f8-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="845f8-113">結果</span><span class="sxs-lookup"><span data-stu-id="845f8-113">Results</span></span>

<span data-ttu-id="845f8-114">ICE31 會針對未定義的樣式、太長的樣式名稱、遺漏的樣式表單，以及沒有右大括弧的樣式標記張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="845f8-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="845f8-115">如果 style 標記不在行首，或控制項有多個樣式標記時，ICE31 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="845f8-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="845f8-116">範例</span><span class="sxs-lookup"><span data-stu-id="845f8-116">Example</span></span>

<span data-ttu-id="845f8-117">ICE31 會針對所顯示的範例張貼下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="845f8-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="845f8-118">控制項 DialogB. Control1 使用未定義的文本樣式 BadStyle。</span><span class="sxs-lookup"><span data-stu-id="845f8-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="845f8-119">控制項 DialogB. Control2 使用未定義的文本樣式 BadStyle。</span><span class="sxs-lookup"><span data-stu-id="845f8-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="845f8-120">控制項 DialogB. Control6 缺少文字樣式的右大括弧。</span><span class="sxs-lookup"><span data-stu-id="845f8-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="845f8-121">控制項 DialogB。 Control3 指定的文字樣式太長，無法有效。</span><span class="sxs-lookup"><span data-stu-id="845f8-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="845f8-122">ICE31 會針對所顯示的範例張貼下列警告：</span><span class="sxs-lookup"><span data-stu-id="845f8-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="845f8-123">DialogB. Control4 中的文字樣式標記沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="845f8-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="845f8-124">您真的想要讓它顯示為文字嗎？</span><span class="sxs-lookup"><span data-stu-id="845f8-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="845f8-125">[控制資料表](control-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="845f8-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="845f8-126">對話</span><span class="sxs-lookup"><span data-stu-id="845f8-126">Dialog</span></span>  | <span data-ttu-id="845f8-127">控制</span><span class="sxs-lookup"><span data-stu-id="845f8-127">Control</span></span>  | <span data-ttu-id="845f8-128">Text</span><span class="sxs-lookup"><span data-stu-id="845f8-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845f8-129">DialogA</span><span class="sxs-lookup"><span data-stu-id="845f8-129">DialogA</span></span> | <span data-ttu-id="845f8-130">Control0</span><span class="sxs-lookup"><span data-stu-id="845f8-130">Control0</span></span> | <span data-ttu-id="845f8-131">{ \\ OKStyle} 這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="845f8-132">DialogA</span><span class="sxs-lookup"><span data-stu-id="845f8-132">DialogA</span></span> | <span data-ttu-id="845f8-133">Control1</span><span class="sxs-lookup"><span data-stu-id="845f8-133">Control1</span></span> | <span data-ttu-id="845f8-134">{&OKStyle}這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="845f8-135">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-135">DialogB</span></span> | <span data-ttu-id="845f8-136">Control1</span><span class="sxs-lookup"><span data-stu-id="845f8-136">Control1</span></span> | <span data-ttu-id="845f8-137">{&BadStyle}這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="845f8-138">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-138">DialogB</span></span> | <span data-ttu-id="845f8-139">Control2</span><span class="sxs-lookup"><span data-stu-id="845f8-139">Control2</span></span> | <span data-ttu-id="845f8-140">{ \\ BadStyle} 這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="845f8-141">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-141">DialogB</span></span> | <span data-ttu-id="845f8-142">Control3</span><span class="sxs-lookup"><span data-stu-id="845f8-142">Control3</span></span> | <span data-ttu-id="845f8-143">{&樣式的長度超過72個字元，因此也不能是樣式，即使您在樣式表單中進行管理，也不能是一樣的樣式}這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="845f8-144">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-144">DialogB</span></span> | <span data-ttu-id="845f8-145">Control4</span><span class="sxs-lookup"><span data-stu-id="845f8-145">Control4</span></span> | <span data-ttu-id="845f8-146">警告 { \\ OKStyle} 這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="845f8-147">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-147">DialogB</span></span> | <span data-ttu-id="845f8-148">Control5</span><span class="sxs-lookup"><span data-stu-id="845f8-148">Control5</span></span> | <span data-ttu-id="845f8-149">{ \\ OKStyle} {&OKStyle} 這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="845f8-150">DialogB</span><span class="sxs-lookup"><span data-stu-id="845f8-150">DialogB</span></span> | <span data-ttu-id="845f8-151">Control6</span><span class="sxs-lookup"><span data-stu-id="845f8-151">Control6</span></span> | <span data-ttu-id="845f8-152">{ \\ OKStyle 這是要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="845f8-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="845f8-153"> (部分) 的[樣式表單](textstyle-table.md)</span><span class="sxs-lookup"><span data-stu-id="845f8-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="845f8-154">文本</span><span class="sxs-lookup"><span data-stu-id="845f8-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="845f8-155">OkStyle</span><span class="sxs-lookup"><span data-stu-id="845f8-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="845f8-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="845f8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="845f8-157">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="845f8-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



