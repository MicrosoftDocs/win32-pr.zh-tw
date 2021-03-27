---
description: 雖然上述工作中討論的函式適用于許多語言，但是它們可能無法處理複雜字集的需求。
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: 複雜字集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848573"
---
# <a name="complex-scripts"></a><span data-ttu-id="38d50-103">複雜字集</span><span class="sxs-lookup"><span data-stu-id="38d50-103">Complex Scripts</span></span>

<span data-ttu-id="38d50-104">雖然上述工作中討論的函式適用于許多語言，但是它們可能無法處理複雜字集的需求。</span><span class="sxs-lookup"><span data-stu-id="38d50-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="38d50-105">*複雜的腳本* 是指不會以簡單的方式轉譯印刷表單的語言。</span><span class="sxs-lookup"><span data-stu-id="38d50-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="38d50-106">例如，複雜的腳本可能會允許雙向轉譯、字型的內容成形，或合併字元。</span><span class="sxs-lookup"><span data-stu-id="38d50-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="38d50-107">由於這些特殊需求的緣故，文字輸出的控制必須非常有彈性。</span><span class="sxs-lookup"><span data-stu-id="38d50-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="38d50-108">顯示文字 [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)、 [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)、 [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)、 [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)和 [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) 的函式已經過擴充，可支援複雜的腳本。</span><span class="sxs-lookup"><span data-stu-id="38d50-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="38d50-109">一般而言，這項支援對應用程式而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="38d50-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="38d50-110">但是，應用程式應該將字元儲存在緩衝區中，並一次顯示整行文字，讓複雜的腳本成形模組可以使用內容來正確地重新排列和產生字元。</span><span class="sxs-lookup"><span data-stu-id="38d50-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="38d50-111">此外，由於圖像的寬度可能會因內容而異，因此應用程式應該使用 [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) 來判斷行長度，而不是使用快取的字元寬度。</span><span class="sxs-lookup"><span data-stu-id="38d50-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="38d50-112">此外，複雜的腳本感知應用程式應該考慮將由右至左的讀取順序以及適當對齊其應用程式的支援。</span><span class="sxs-lookup"><span data-stu-id="38d50-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="38d50-113">您可以使用下列程式碼，將讀取順序或左右對齊切換至左方和右邊：</span><span class="sxs-lookup"><span data-stu-id="38d50-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



<span data-ttu-id="38d50-114">若要一次切換這兩個屬性，請執行下列語句，然後呼叫 [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 和 [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)，如先前所示：</span><span class="sxs-lookup"><span data-stu-id="38d50-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="38d50-115">您也可以使用 Uniscribe 處理複雜的腳本。</span><span class="sxs-lookup"><span data-stu-id="38d50-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="38d50-116">Uniscribe 是一組功能，可讓您對複雜的腳本進行精細的控制。</span><span class="sxs-lookup"><span data-stu-id="38d50-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="38d50-117">如需詳細資訊，請參閱 [Uniscribe](../intl/uniscribe.md) 和 [處理複雜的腳本](../intl/processing-complex-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="38d50-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
