---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: GDI+ Flat API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991347"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="dfeca-103">GDI+ Flat API</span><span class="sxs-lookup"><span data-stu-id="dfeca-103">GDI+ Flat API</span></span>

<span data-ttu-id="dfeca-104">Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。</span><span class="sxs-lookup"><span data-stu-id="dfeca-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="dfeca-105">GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。</span><span class="sxs-lookup"><span data-stu-id="dfeca-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="dfeca-106">建議您不要直接呼叫一般 API 中的函式。</span><span class="sxs-lookup"><span data-stu-id="dfeca-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="dfeca-107">每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。</span><span class="sxs-lookup"><span data-stu-id="dfeca-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="dfeca-108">Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。</span><span class="sxs-lookup"><span data-stu-id="dfeca-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="dfeca-109">Microsoft .NET Framework 是 c + + 包裝函式的替代方案，提供一組適用于 GDI + 的 managed 程式碼包裝函式類別。</span><span class="sxs-lookup"><span data-stu-id="dfeca-109">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="dfeca-110">GDI + 的 managed 程式碼包裝函式屬於下列命名空間。</span><span class="sxs-lookup"><span data-stu-id="dfeca-110">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="dfeca-111">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="dfeca-111">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="dfeca-112">Drawing2D</span><span class="sxs-lookup"><span data-stu-id="dfeca-112">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="dfeca-113">System. Drawing. 影像處理</span><span class="sxs-lookup"><span data-stu-id="dfeca-113">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="dfeca-114">System.object。文字</span><span class="sxs-lookup"><span data-stu-id="dfeca-114">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="dfeca-115">這兩組包裝函式 (c + + 和 managed 程式碼) 使用物件導向的方法，因此參數傳遞至包裝函式方法的方式以及參數傳遞至一般 API 中之函式的方式之間有一些差異。</span><span class="sxs-lookup"><span data-stu-id="dfeca-115">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="dfeca-116">例如，其中一個 c + + 包裝函式是 [**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別。</span><span class="sxs-lookup"><span data-stu-id="dfeca-116">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="dfeca-117">每個 **矩陣** 物件都有一個 **nativeMatrix** 的欄位，指向 **GpMatrix** 類型的內部變數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-117">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="dfeca-118">當您將參數傳遞給 **矩陣** 物件的方法時，該方法會將這些參數傳遞 (或一組相關的參數) ，以及 gdi + 一般 API 中的其中一個函式。</span><span class="sxs-lookup"><span data-stu-id="dfeca-118">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="dfeca-119">但是，該方法也會將 **nativeMatrix** 欄位 (為輸入參數) 至一般 API 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-119">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="dfeca-120">下列程式碼顯示 [**Matrix：：切變**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) 方法如何呼叫 **GdipShearMatrix (GPMATRIX \* 矩陣、Real shearX、real shearY、GpMatrixOrder order)** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-120">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="dfeca-121">[**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)的函式會將 **GpMatrix** 指標變數的位址傳遞 (為 **GdipCreateMatrix (GpMatrix \* \* 矩陣)** 函式的輸出) 參數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-121">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="dfeca-122">**GdipCreateMatrix** 會建立並初始化內部 **GpMatrix** 變數，然後將 **GpMatrix** 的位址指派給指標變數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-122">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="dfeca-123">然後，此函式會將指標的值複製到 **nativeMatrix** 欄位。</span><span class="sxs-lookup"><span data-stu-id="dfeca-123">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="dfeca-124">包裝函式類別中的複製方法不會收到任何參數，但通常會將兩個參數傳遞給 GDI + 一般 API 中的基礎函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-124">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="dfeca-125">例如， [**Matrix：： Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) 方法會傳遞 **nativeMatrix** (做為輸入參數) ，而 **GpMatrix** 指標變數的位址 (為 **GdipCloneMatrix** 函式) 的輸出參數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-125">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="dfeca-126">下列程式碼顯示 **Matrix：： Clone** 方法如何呼叫 **GdipCloneMatrix (GpMatrix \* Matrix，GpMatrix \* \* cloneMatrix)** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-126">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="dfeca-127">一般 API 中的函式會傳回 GpStatus 類型的值。</span><span class="sxs-lookup"><span data-stu-id="dfeca-127">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="dfeca-128">GpStatus 列舉等同于包裝函式方法所使用的 [**狀態**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) 列舉。</span><span class="sxs-lookup"><span data-stu-id="dfeca-128">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="dfeca-129">在 GdiplusGpStubs 中，GpStatus 定義如下：</span><span class="sxs-lookup"><span data-stu-id="dfeca-129">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="dfeca-130">包裝函式類別中的大部分方法都會傳回狀態值，指出方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="dfeca-130">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="dfeca-131">不過，某些包裝函式方法會傳回狀態值。</span><span class="sxs-lookup"><span data-stu-id="dfeca-131">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="dfeca-132">當您呼叫會傳回狀態值的包裝函式方法時，包裝函式方法會將適當的參數傳遞至 GDI + 一般 API 中的基礎函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-132">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="dfeca-133">例如， [**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別具有 [**Matrix：： IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) 方法，它會將 **nativeMatrix** 欄位和 **布林** 值變數的位址 (為輸出參數) 至 **GdipIsMatrixInvertible** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-133">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="dfeca-134">下列程式碼顯示 **Matrix：： IsInvertible** 方法如何呼叫 **GdipIsMatrixInvertible (GDIPCONST GPMATRIX \* 矩陣，BOOL \* 結果)** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-134">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="dfeca-135">另一個包裝函式是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 類別。</span><span class="sxs-lookup"><span data-stu-id="dfeca-135">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="dfeca-136">**Color** 物件具有類型 **ARGB** 的單一欄位，定義為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="dfeca-136">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="dfeca-137">當您將 **色彩** 物件傳遞給其中一個包裝函式方法時，該方法會將 **ARGB** 欄位傳遞給 gdi + 一般 API 中的基礎函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-137">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="dfeca-138">下列程式碼顯示 [**Pen：： SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) 方法如何呼叫 **GdipSetPenColor (GPPEN \* 畫筆，argb argb)** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfeca-138">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="dfeca-139">[**Color：： GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue)方法會傳回 **ARGB** 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="dfeca-139">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="dfeca-140">下列主題顯示 GDI + 一般 API 與 c + + 包裝函式方法之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="dfeca-140">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="dfeca-141">AdjustableArrowCap 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-141">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="dfeca-142">點陣圖函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-142">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="dfeca-143">筆刷函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-143">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="dfeca-144">CachedBitmap 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-144">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="dfeca-145">CustomLineCap 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-145">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="dfeca-146">字型函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-146">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="dfeca-147">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="dfeca-147">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="dfeca-148">圖形函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-148">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="dfeca-149">GraphicsPath 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-149">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="dfeca-150">HatchBrush 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-150">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="dfeca-151">影像函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-151">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="dfeca-152">ImageAttributes 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-152">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="dfeca-153">LinearGradientBrush 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-153">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="dfeca-154">矩陣函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-154">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="dfeca-155">記憶體函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-155">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="dfeca-156">通知函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-156">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="dfeca-157">PathGradientBrush 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-157">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="dfeca-158">PathIterator 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-158">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="dfeca-159">畫筆函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-159">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="dfeca-160">區域函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-160">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="dfeca-161">SolidBrush 函式</span><span class="sxs-lookup"><span data-stu-id="dfeca-161">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="dfeca-162">字串格式函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-162">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="dfeca-163">文字函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-163">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="dfeca-164">材質筆刷函數</span><span class="sxs-lookup"><span data-stu-id="dfeca-164">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
