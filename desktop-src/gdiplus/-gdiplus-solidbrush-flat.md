---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972145"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="e1239-103">SolidBrush 函式</span><span class="sxs-lookup"><span data-stu-id="e1239-103">SolidBrush Functions</span></span>

<span data-ttu-id="e1239-104">Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。</span><span class="sxs-lookup"><span data-stu-id="e1239-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="e1239-105">GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。</span><span class="sxs-lookup"><span data-stu-id="e1239-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="e1239-106">建議不要直接呼叫一般 API 中的函式。</span><span class="sxs-lookup"><span data-stu-id="e1239-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="e1239-107">每當您對 GDI + 進行呼叫時，我們建議您呼叫 c + + 包裝函式所提供的方法和函式來執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="e1239-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="e1239-108">Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。</span><span class="sxs-lookup"><span data-stu-id="e1239-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="e1239-109">如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。</span><span class="sxs-lookup"><span data-stu-id="e1239-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="e1239-110">下列一般 API 函式是由 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) c + + 類別包裝。</span><span class="sxs-lookup"><span data-stu-id="e1239-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="e1239-111">筆刷函數和對應的包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="e1239-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="e1239-112">一般函數</span><span class="sxs-lookup"><span data-stu-id="e1239-112">Flat function</span></span>                                                                               | <span data-ttu-id="e1239-113">包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="e1239-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="e1239-114">備註</span><span class="sxs-lookup"><span data-stu-id="e1239-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1239-115">**GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB 色彩、GpSolidFill \* \* 筆刷)**</span><span class="sxs-lookup"><span data-stu-id="e1239-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="e1239-116">[**SolidBrush：： SolidBrush (const 色彩& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="e1239-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="e1239-117">根據色彩建立 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件</span><span class="sxs-lookup"><span data-stu-id="e1239-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="e1239-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* 筆刷，ARGB 色彩)**</span><span class="sxs-lookup"><span data-stu-id="e1239-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="e1239-119">**SolidBrush：： SetColor (const 色彩& Color)**</span><span class="sxs-lookup"><span data-stu-id="e1239-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="e1239-120">設定此實心筆刷的色彩</span><span class="sxs-lookup"><span data-stu-id="e1239-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="e1239-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* 筆刷，ARGB \* 色彩)**</span><span class="sxs-lookup"><span data-stu-id="e1239-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="e1239-122">**SolidBrush：： GetColor (OUT Color \* color) const**</span><span class="sxs-lookup"><span data-stu-id="e1239-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="e1239-123">取得這個實心筆刷的色彩</span><span class="sxs-lookup"><span data-stu-id="e1239-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
