---
title: '字型和文字函數 (OpenGL) '
description: 您可以使用下列函數來管理字型和文字。
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL 函式，文字
- WGL 函式，字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383666"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="94b8f-105">字型和文字函數 (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="94b8f-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="94b8f-106">您可以使用下列函數來管理字型和文字。</span><span class="sxs-lookup"><span data-stu-id="94b8f-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="94b8f-107">Windows 函數</span><span class="sxs-lookup"><span data-stu-id="94b8f-107">Windows Function</span></span>                                 | <span data-ttu-id="94b8f-108">Description</span><span class="sxs-lookup"><span data-stu-id="94b8f-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94b8f-109">**wglUseFontBitmaps**</span><span class="sxs-lookup"><span data-stu-id="94b8f-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="94b8f-110">建立一組字元點陣圖顯示清單。</span><span class="sxs-lookup"><span data-stu-id="94b8f-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="94b8f-111">字元來自指定之裝置內容的目前字型。</span><span class="sxs-lookup"><span data-stu-id="94b8f-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="94b8f-112">字元會指定為字型字元集內的連續執行。</span><span class="sxs-lookup"><span data-stu-id="94b8f-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="94b8f-113">**wglUseFontOutlines**</span><span class="sxs-lookup"><span data-stu-id="94b8f-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="94b8f-114">根據目前選取的裝置內容大綱字型字型，建立一組顯示清單，以與目前的轉譯內容搭配使用。</span><span class="sxs-lookup"><span data-stu-id="94b8f-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="94b8f-115">顯示清單是用來繪製立體字元的 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="94b8f-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="94b8f-116">**WglUseFontBitmaps** 和 **wglUseFontOutlines** 函式會取得裝置內容的控制碼，並使用該裝置內容的目前字型作為點陣圖的來源。</span><span class="sxs-lookup"><span data-stu-id="94b8f-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="94b8f-117">因此，在呼叫 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 之前，必須先設定裝置內容的字型和字型屬性。</span><span class="sxs-lookup"><span data-stu-id="94b8f-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="94b8f-118">[**WglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)和 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)函式也會取得參數，以將字型中的第一個字元轉換成點陣圖顯示清單，以及指定要轉換成顯示清單的字元數的參數。</span><span class="sxs-lookup"><span data-stu-id="94b8f-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="94b8f-119">然後，函數會為指定的連續字元執行建立顯示清單。</span><span class="sxs-lookup"><span data-stu-id="94b8f-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="94b8f-120">例如：</span><span class="sxs-lookup"><span data-stu-id="94b8f-120">For example:</span></span>

-   <span data-ttu-id="94b8f-121">若要為所有 Windows 字元集字元建立一組224點陣圖顯示清單，請將這兩個參數分別設定為32和224。</span><span class="sxs-lookup"><span data-stu-id="94b8f-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="94b8f-122">若要為所有 OEM 字元集字元建立一組256點陣圖顯示清單，請將這兩個參數分別設定為0和256。</span><span class="sxs-lookup"><span data-stu-id="94b8f-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="94b8f-123">若要為任何單一字元集圖像建立單一點陣圖顯示清單，請將這些參數的第二個設為1。</span><span class="sxs-lookup"><span data-stu-id="94b8f-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="94b8f-124">**WglUseFontBitmaps** 和 **wglUseFontOutlines** 函式代表字型中具有空白顯示清單的 null 圖像。</span><span class="sxs-lookup"><span data-stu-id="94b8f-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="94b8f-125">對 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 的呼叫所建立的顯示清單，會連續自動編號。</span><span class="sxs-lookup"><span data-stu-id="94b8f-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="94b8f-126">呼叫 [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) 或 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) 函數之後，請呼叫 [**glCallLists**](glcalllists.md) 來繪製字元字串。</span><span class="sxs-lookup"><span data-stu-id="94b8f-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="94b8f-127">如需範例程式碼，請參閱 [在 Double-Buffered OpenGL 視窗中繪製文字](drawing-text-in-a-double-buffered-opengl-window.md) 。</span><span class="sxs-lookup"><span data-stu-id="94b8f-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="94b8f-128">在此內容中， **glCallLists** 會使用字串中的每個字元做為 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 所建立連續編號顯示清單陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="94b8f-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="94b8f-129">當您完成繪製文字時，請呼叫 [**glDeleteLists**](gldeletelists.md) 函式來釋放 **wglUseFontBitmaps** 和 **wglUseFontOutlines** 所建立的連續一組顯示清單。</span><span class="sxs-lookup"><span data-stu-id="94b8f-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




