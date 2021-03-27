---
description: 當應用程式執行這類工作時，必須抓取字元寬度的資料，以將文字的字串調整為頁面或資料行寬度。
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: 字元寬度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848575"
---
# <a name="character-widths"></a><span data-ttu-id="592da-103">字元寬度</span><span class="sxs-lookup"><span data-stu-id="592da-103">Character Widths</span></span>

<span data-ttu-id="592da-104">當應用程式執行這類工作時，必須抓取字元寬度的資料，以將文字的字串調整為頁面或資料行寬度。</span><span class="sxs-lookup"><span data-stu-id="592da-104">Applications need to retrieve character-width data when they perform such tasks as fitting strings of text to page or column widths.</span></span> <span data-ttu-id="592da-105">應用程式可以使用四個函式來取出字元寬度的資料。</span><span class="sxs-lookup"><span data-stu-id="592da-105">There are four functions that an application can use to retrieve character-width data.</span></span> <span data-ttu-id="592da-106">其中兩個函式會抓取字元前進寬度，而其中兩個函式會取出實際的字元寬度資料。</span><span class="sxs-lookup"><span data-stu-id="592da-106">Two of these functions retrieve the character-advance width and two of these functions retrieve actual character-width data.</span></span>

<span data-ttu-id="592da-107">應用程式可以使用 [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) 和 [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) 函式，在文字字串中取得個別字元或符號的前進寬度。</span><span class="sxs-lookup"><span data-stu-id="592da-107">An application can use the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) and [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) functions to retrieve the advance width for individual characters or symbols in a string of text.</span></span> <span data-ttu-id="592da-108">[前進寬度] 是影片顯示器上的游標或印表機上的列印頭必須先前進，然後才能列印文字字串中的下一個字元。</span><span class="sxs-lookup"><span data-stu-id="592da-108">The advance width is the distance that the cursor on a video display or the print-head on a printer must advance before printing the next character in a string of text.</span></span> <span data-ttu-id="592da-109">[**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a)函式會將前進寬度傳回為整數值。</span><span class="sxs-lookup"><span data-stu-id="592da-109">The [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function returns the advance width as an integer value.</span></span> <span data-ttu-id="592da-110">如果需要更高的精確度，則應用程式可以使用 [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) 函式來取出小數預付寬度值。</span><span class="sxs-lookup"><span data-stu-id="592da-110">If greater precision is required, an application can use the [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) function to retrieve fractional advance-width values.</span></span>

<span data-ttu-id="592da-111">應用程式可以使用 [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) 和 [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) 函數來取得實際的字元寬度資料。</span><span class="sxs-lookup"><span data-stu-id="592da-111">An application can retrieve actual character-width data by using the [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) and [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) functions.</span></span> <span data-ttu-id="592da-112">**GetCharABCWidthsFloat** 函數適用于所有字型。</span><span class="sxs-lookup"><span data-stu-id="592da-112">The **GetCharABCWidthsFloat** function works with all fonts.</span></span> <span data-ttu-id="592da-113">[**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa)函式僅適用于 TrueType 和 OpenType 字型。</span><span class="sxs-lookup"><span data-stu-id="592da-113">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function only works with TrueType and OpenType fonts.</span></span> <span data-ttu-id="592da-114">如需有關 TrueType 和 OpenType 字型的詳細資訊，請參閱 [點陣、向量、TrueType 和 opentype](raster--vector--truetype--and-opentype-fonts.md)字型。</span><span class="sxs-lookup"><span data-stu-id="592da-114">For more information about TrueType and OpenType fonts, see [Raster, Vector, TrueType, and OpenType Fonts](raster--vector--truetype--and-opentype-fonts.md).</span></span>

<span data-ttu-id="592da-115">下圖顯示字元寬度的三個元件：</span><span class="sxs-lookup"><span data-stu-id="592da-115">The following illustration shows the three components of a character width:</span></span>

![顯示兩個相鄰字元的間距、b 間距和 c 間距的圖例](images/csftx-02.png)

<span data-ttu-id="592da-117">間距是在放置字元之前，要加入至目前位置的寬度。</span><span class="sxs-lookup"><span data-stu-id="592da-117">The A spacing is the width to add to the current position before placing the character.</span></span> <span data-ttu-id="592da-118">B 間距是字元本身的寬度。</span><span class="sxs-lookup"><span data-stu-id="592da-118">The B spacing is the width of the character itself.</span></span> <span data-ttu-id="592da-119">C 間距是字元右邊的空白字元。</span><span class="sxs-lookup"><span data-stu-id="592da-119">The C spacing is the white space to the right of the character.</span></span> <span data-ttu-id="592da-120">總進寬度是藉由計算 + B + C 的總和來決定。</span><span class="sxs-lookup"><span data-stu-id="592da-120">The total advance width is determined by calculating the sum of A+B+C.</span></span> <span data-ttu-id="592da-121">字元資料格是以字型括住每個字元或符號的虛數矩形。</span><span class="sxs-lookup"><span data-stu-id="592da-121">The character cell is an imaginary rectangle that surrounds each character or symbol in a font.</span></span> <span data-ttu-id="592da-122">因為字元可能會超出或 underhang 字元資料格，所以 A 和 C 的每個增量都可以是負數。</span><span class="sxs-lookup"><span data-stu-id="592da-122">Because characters can overhang or underhang the character cell, either or both of the A and C increments can be a negative number.</span></span>

 

 
