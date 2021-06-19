---
description: Windows GDI + 會公開由大約600函式組成的一般 API。 這些一般 API 函式是由筆刷 c + + 類別包裝。
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: " (GDI +) 的筆刷函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395083"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="34754-104"> (GDI +) 的筆刷函數</span><span class="sxs-lookup"><span data-stu-id="34754-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="34754-105">Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。</span><span class="sxs-lookup"><span data-stu-id="34754-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="34754-106">GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。</span><span class="sxs-lookup"><span data-stu-id="34754-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="34754-107">建議您不要直接呼叫一般 API 中的函式。</span><span class="sxs-lookup"><span data-stu-id="34754-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="34754-108">每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。</span><span class="sxs-lookup"><span data-stu-id="34754-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="34754-109">Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。</span><span class="sxs-lookup"><span data-stu-id="34754-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="34754-110">如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。</span><span class="sxs-lookup"><span data-stu-id="34754-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="34754-111">下列一般 API 函式是由 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) c + + 類別包裝。</span><span class="sxs-lookup"><span data-stu-id="34754-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="34754-112">筆刷函數和對應的包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="34754-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="34754-113">一般函數</span><span class="sxs-lookup"><span data-stu-id="34754-113">Flat function</span></span>                                                                        | <span data-ttu-id="34754-114">包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="34754-114">Wrapper method</span></span>                                          | <span data-ttu-id="34754-115">描述</span><span class="sxs-lookup"><span data-stu-id="34754-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34754-116">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* 筆刷，GpBrush \* \* cloneBrush) </span><span class="sxs-lookup"><span data-stu-id="34754-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="34754-117">**筆刷：： Clone**</span><span class="sxs-lookup"><span data-stu-id="34754-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="34754-118">[**Brush：： Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)方法會根據此筆刷建立新的 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)物件。</span><span class="sxs-lookup"><span data-stu-id="34754-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="34754-119">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* 筆刷) </span><span class="sxs-lookup"><span data-stu-id="34754-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="34754-120">虛擬 ~ 筆刷 () </span><span class="sxs-lookup"><span data-stu-id="34754-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="34754-121">清除 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="34754-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="34754-122">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* 筆刷，GpBrushType \* 類型) </span><span class="sxs-lookup"><span data-stu-id="34754-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="34754-123">**筆刷：： GetType**</span><span class="sxs-lookup"><span data-stu-id="34754-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="34754-124">[**Brush：： GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype)方法會取得此筆刷的型別。</span><span class="sxs-lookup"><span data-stu-id="34754-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




