---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681925"
---
# <a name="iagentballoon"></a><span data-ttu-id="b679e-103">IAgentBalloon</span><span class="sxs-lookup"><span data-stu-id="b679e-103">IAgentBalloon</span></span>

<span data-ttu-id="b679e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b679e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b679e-105">**IAgentBalloon** 定義了一個介面，可讓應用程式查詢 Microsoft Agent 文字提示的屬性。</span><span class="sxs-lookup"><span data-stu-id="b679e-105">**IAgentBalloon** defines an interface that allows applications to query properties for the Microsoft Agent word balloon.</span></span> <span data-ttu-id="b679e-106">這些函數也可從 [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**)取得。</span><span class="sxs-lookup"><span data-stu-id="b679e-106">These functions are also available from [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**).</span></span>

<span data-ttu-id="b679e-107">字元的文字氣球的初始預設值是在 Microsoft Agent 字元編輯器中設定，但是在應用程式執行之後，使用者可能會覆寫 [ [**Enabled**](enabled-property.md) ] 和 [ [Font](fontname-property.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="b679e-107">Initial defaults for a character's word balloon are set in the Microsoft Agent Character Editor, but once the application is running, the user may override the [**Enabled**](enabled-property.md) and [Font](fontname-property.md) properties.</span></span> <span data-ttu-id="b679e-108">如果使用者變更氣球的屬性，變更就會影響所有的字元。</span><span class="sxs-lookup"><span data-stu-id="b679e-108">If a user changes the balloon's properties, the change affects all characters.</span></span> <span data-ttu-id="b679e-109">[**IAgentBalloon**](/windows/desktop/lwef/iagentballoon)物件的屬性也適用于透過 [[**思考**](think-method.md)] 方法的文字輸出。</span><span class="sxs-lookup"><span data-stu-id="b679e-109">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) object's properties also apply to text output through the [**Think**](think-method.md) method.</span></span>

<span data-ttu-id="b679e-110">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="b679e-110">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="b679e-111">IAgentBalloon 方法</span><span class="sxs-lookup"><span data-stu-id="b679e-111">IAgentBalloon Methods</span></span>                                       | <span data-ttu-id="b679e-112">Description</span><span class="sxs-lookup"><span data-stu-id="b679e-112">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="b679e-113">GetEnabled</span><span class="sxs-lookup"><span data-stu-id="b679e-113">GetEnabled</span></span>](iagentballoon--getenabled.md)                 | <span data-ttu-id="b679e-114">傳回是否啟用文字提示。</span><span class="sxs-lookup"><span data-stu-id="b679e-114">Returns whether the word balloon is enabled.</span></span>                                          |
| [<span data-ttu-id="b679e-115">GetNumLines</span><span class="sxs-lookup"><span data-stu-id="b679e-115">GetNumLines</span></span>](iagentballoon--getnumlines.md)               | <span data-ttu-id="b679e-116">傳回文字氣球中顯示的行數。</span><span class="sxs-lookup"><span data-stu-id="b679e-116">Returns the number of lines displayed in the word balloon.</span></span>                            |
| [<span data-ttu-id="b679e-117">GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="b679e-117">GetNumCharsPerLine</span></span>](iagentballoon--getnumcharsperline.md) | <span data-ttu-id="b679e-118">傳回文字球中顯示的每一行字元平均字元數。</span><span class="sxs-lookup"><span data-stu-id="b679e-118">Returns the average number of characters per line displayed in the word balloon.</span></span>      |
| [<span data-ttu-id="b679e-119">GetFontName</span><span class="sxs-lookup"><span data-stu-id="b679e-119">GetFontName</span></span>](iagentballoon--getfontname.md)               | <span data-ttu-id="b679e-120">傳回文字氣球中所顯示字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="b679e-120">Returns the name of the font displayed in the word balloon.</span></span>                           |
| [<span data-ttu-id="b679e-121">GetFontSize</span><span class="sxs-lookup"><span data-stu-id="b679e-121">GetFontSize</span></span>](iagentballoon--getfontsize.md)               | <span data-ttu-id="b679e-122">傳回文字氣球中所顯示字型的大小。</span><span class="sxs-lookup"><span data-stu-id="b679e-122">Returns the size of the font displayed in the word balloon.</span></span>                           |
| [<span data-ttu-id="b679e-123">GetFontBold</span><span class="sxs-lookup"><span data-stu-id="b679e-123">GetFontBold</span></span>](iagentballoon--getfontbold.md)               | <span data-ttu-id="b679e-124">傳回文字批註框中顯示的字型是否為粗體。</span><span class="sxs-lookup"><span data-stu-id="b679e-124">Returns whether the font displayed in the word balloon is bold.</span></span>                       |
| [<span data-ttu-id="b679e-125">GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="b679e-125">GetFontItalic</span></span>](iagentballoon--getfontitalic.md)           | <span data-ttu-id="b679e-126">傳回文字批註框中顯示的字型是否為斜體。</span><span class="sxs-lookup"><span data-stu-id="b679e-126">Returns whether the font displayed in the word balloon is italic.</span></span>                     |
| [<span data-ttu-id="b679e-127">GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="b679e-127">GetFontStrikethru</span></span>](iagentballoon--getfontstrikethru.md)   | <span data-ttu-id="b679e-128">傳回文字氣球中顯示的字型是否顯示為刪除線。</span><span class="sxs-lookup"><span data-stu-id="b679e-128">Returns whether the font displayed in the word balloon is displayed as strikethrough.</span></span> |
| [<span data-ttu-id="b679e-129">GetFontUnderline</span><span class="sxs-lookup"><span data-stu-id="b679e-129">GetFontUnderline</span></span>](iagentballoon--getfontunderline.md)     | <span data-ttu-id="b679e-130">傳回文字氣球中顯示的字型是否加上底線。</span><span class="sxs-lookup"><span data-stu-id="b679e-130">Returns whether the font displayed in the word balloon is underlined.</span></span>                 |
| [<span data-ttu-id="b679e-131">GetForeColor</span><span class="sxs-lookup"><span data-stu-id="b679e-131">GetForeColor</span></span>](iagentballoon--getforecolor.md)             | <span data-ttu-id="b679e-132">傳回文字氣球中所顯示的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="b679e-132">Returns the foreground color displayed in the word balloon.</span></span>                           |
| [<span data-ttu-id="b679e-133">GetBackColor</span><span class="sxs-lookup"><span data-stu-id="b679e-133">GetBackColor</span></span>](iagentballoon--getbackcolor.md)             | <span data-ttu-id="b679e-134">傳回文字氣球中所顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="b679e-134">Returns the background color displayed in the word balloon.</span></span>                           |
| [<span data-ttu-id="b679e-135">GetBorderColor</span><span class="sxs-lookup"><span data-stu-id="b679e-135">GetBorderColor</span></span>](iagentballoon--getbordercolor.md)         | <span data-ttu-id="b679e-136">傳回文字氣球中顯示的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="b679e-136">Returns the border color displayed in the word balloon.</span></span>                               |
| [<span data-ttu-id="b679e-137">SetVisible</span><span class="sxs-lookup"><span data-stu-id="b679e-137">SetVisible</span></span>](iagentballoon--setvisible.md)                 | <span data-ttu-id="b679e-138">將文字批註設定為可見。</span><span class="sxs-lookup"><span data-stu-id="b679e-138">Sets the word balloon to be visible.</span></span>                                                  |
| [<span data-ttu-id="b679e-139">GetVisible</span><span class="sxs-lookup"><span data-stu-id="b679e-139">GetVisible</span></span>](iagentballoon--getvisible.md)                 | <span data-ttu-id="b679e-140">傳回文字氣球的可見度設定。</span><span class="sxs-lookup"><span data-stu-id="b679e-140">Returns the visibility setting for the word balloon.</span></span>                                  |
| [<span data-ttu-id="b679e-141">SetFontName</span><span class="sxs-lookup"><span data-stu-id="b679e-141">SetFontName</span></span>](iagentballoon--setfontname.md)               | <span data-ttu-id="b679e-142">設定文字氣球中使用的字型。</span><span class="sxs-lookup"><span data-stu-id="b679e-142">Sets the font used in the word balloon.</span></span>                                               |
| [<span data-ttu-id="b679e-143">SetFontSize</span><span class="sxs-lookup"><span data-stu-id="b679e-143">SetFontSize</span></span>](iagentballoon--setfontsize.md)               | <span data-ttu-id="b679e-144">設定文字氣球中使用的字型大小。</span><span class="sxs-lookup"><span data-stu-id="b679e-144">Sets the font size used in the word balloon.</span></span>                                          |
| [<span data-ttu-id="b679e-145">SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="b679e-145">SetFontCharSet</span></span>](iagentballoon--setfontcharset.md)         | <span data-ttu-id="b679e-146">設定字組氣球中使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="b679e-146">Sets the character set used in the word balloon.</span></span>                                      |
| [<span data-ttu-id="b679e-147">GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="b679e-147">GetFontCharSet</span></span>](iagentballoon--getfontcharset.md)         | <span data-ttu-id="b679e-148">傳回字組氣球中使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="b679e-148">Returns the character set used in the word balloon.</span></span>                                   |



 

 

 