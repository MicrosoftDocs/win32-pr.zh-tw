---
description: Windows GDI + 會公開由大約600函式組成的一般 API。 這些一般 API 函式是由 GdiplusBase c + + 類別包裝。
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: 記憶體函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395823"
---
# <a name="memory-functions"></a><span data-ttu-id="1073e-104">記憶體函數</span><span class="sxs-lookup"><span data-stu-id="1073e-104">Memory Functions</span></span>

<span data-ttu-id="1073e-105">Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。</span><span class="sxs-lookup"><span data-stu-id="1073e-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="1073e-106">GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。</span><span class="sxs-lookup"><span data-stu-id="1073e-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="1073e-107">建議您不要直接呼叫一般 API 中的函式。</span><span class="sxs-lookup"><span data-stu-id="1073e-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="1073e-108">每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。</span><span class="sxs-lookup"><span data-stu-id="1073e-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="1073e-109">Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。</span><span class="sxs-lookup"><span data-stu-id="1073e-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="1073e-110">如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。</span><span class="sxs-lookup"><span data-stu-id="1073e-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="1073e-111">下列一般 API 函式是由 [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) c + + 類別包裝。</span><span class="sxs-lookup"><span data-stu-id="1073e-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="1073e-112">記憶體函數和對應的包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="1073e-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="1073e-113">一般函數</span><span class="sxs-lookup"><span data-stu-id="1073e-113">Flat function</span></span>                                          | <span data-ttu-id="1073e-114">包裝函式方法</span><span class="sxs-lookup"><span data-stu-id="1073e-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="1073e-115">備註</span><span class="sxs-lookup"><span data-stu-id="1073e-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1073e-116">GpStatus WINGDIPAPI GdipAlloc (size \_ t size) </span><span class="sxs-lookup"><span data-stu-id="1073e-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="1073e-117">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)  (size \_ t \_ 大小)**</span><span class="sxs-lookup"><span data-stu-id="1073e-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="1073e-118">配置一個 Windows GDI + 物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1073e-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="1073e-119">GdipAlloc 宣告于 GdiplusMem 中。</span><span class="sxs-lookup"><span data-stu-id="1073e-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="1073e-120">GpStatus WINGDIPAPI GdipFree (void \* ptr) ;</span><span class="sxs-lookup"><span data-stu-id="1073e-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="1073e-121">**GpStatus WINGDIPAPI GdiplusBase void (運算子 delete)  (void \* in \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="1073e-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="1073e-122">解除配置一個 Windows GDI + 物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1073e-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="1073e-123">GdipFree 宣告于 GdiplusMem 中。</span><span class="sxs-lookup"><span data-stu-id="1073e-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
