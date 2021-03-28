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
# <a name="gdi-flat-api"></a>GDI+ Flat API

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。

Microsoft .NET Framework 是 c + + 包裝函式的替代方案，提供一組適用于 GDI + 的 managed 程式碼包裝函式類別。 GDI + 的 managed 程式碼包裝函式屬於下列命名空間。

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. 影像處理](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.object。文字](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

這兩組包裝函式 (c + + 和 managed 程式碼) 使用物件導向的方法，因此參數傳遞至包裝函式方法的方式以及參數傳遞至一般 API 中之函式的方式之間有一些差異。 例如，其中一個 c + + 包裝函式是 [**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別。 每個 **矩陣** 物件都有一個 **nativeMatrix** 的欄位，指向 **GpMatrix** 類型的內部變數。 當您將參數傳遞給 **矩陣** 物件的方法時，該方法會將這些參數傳遞 (或一組相關的參數) ，以及 gdi + 一般 API 中的其中一個函式。 但是，該方法也會將 **nativeMatrix** 欄位 (為輸入參數) 至一般 API 函數。 下列程式碼顯示 [**Matrix：：切變**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) 方法如何呼叫 **GdipShearMatrix (GPMATRIX \* 矩陣、Real shearX、real shearY、GpMatrixOrder order)** 函數。


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



[**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)的函式會將 **GpMatrix** 指標變數的位址傳遞 (為 **GdipCreateMatrix (GpMatrix \* \* 矩陣)** 函式的輸出) 參數。 **GdipCreateMatrix** 會建立並初始化內部 **GpMatrix** 變數，然後將 **GpMatrix** 的位址指派給指標變數。 然後，此函式會將指標的值複製到 **nativeMatrix** 欄位。


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



包裝函式類別中的複製方法不會收到任何參數，但通常會將兩個參數傳遞給 GDI + 一般 API 中的基礎函數。 例如， [**Matrix：： Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) 方法會傳遞 **nativeMatrix** (做為輸入參數) ，而 **GpMatrix** 指標變數的位址 (為 **GdipCloneMatrix** 函式) 的輸出參數。 下列程式碼顯示 **Matrix：： Clone** 方法如何呼叫 **GdipCloneMatrix (GpMatrix \* Matrix，GpMatrix \* \* cloneMatrix)** 函數。


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



一般 API 中的函式會傳回 GpStatus 類型的值。 GpStatus 列舉等同于包裝函式方法所使用的 [**狀態**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) 列舉。 在 GdiplusGpStubs 中，GpStatus 定義如下：

`typedef Status GpStatus;`

包裝函式類別中的大部分方法都會傳回狀態值，指出方法是否成功。 不過，某些包裝函式方法會傳回狀態值。 當您呼叫會傳回狀態值的包裝函式方法時，包裝函式方法會將適當的參數傳遞至 GDI + 一般 API 中的基礎函數。 例如， [**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別具有 [**Matrix：： IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) 方法，它會將 **nativeMatrix** 欄位和 **布林** 值變數的位址 (為輸出參數) 至 **GdipIsMatrixInvertible** 函數。 下列程式碼顯示 **Matrix：： IsInvertible** 方法如何呼叫 **GdipIsMatrixInvertible (GDIPCONST GPMATRIX \* 矩陣，BOOL \* 結果)** 函數。


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



另一個包裝函式是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 類別。 **Color** 物件具有類型 **ARGB** 的單一欄位，定義為 **DWORD**。 當您將 **色彩** 物件傳遞給其中一個包裝函式方法時，該方法會將 **ARGB** 欄位傳遞給 gdi + 一般 API 中的基礎函數。 下列程式碼顯示 [**Pen：： SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) 方法如何呼叫 **GdipSetPenColor (GPPEN \* 畫筆，argb argb)** 函數。 [**Color：： GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue)方法會傳回 **ARGB** 欄位的值。


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



下列主題顯示 GDI + 一般 API 與 c + + 包裝函式方法之間的關聯性。

-   [AdjustableArrowCap 函式](-gdiplus-adjustablearrowcap-flat.md)
-   [點陣圖函數](-gdiplus-bitmap-flat.md)
-   [筆刷函數](-gdiplus-brush-flat.md)
-   [CachedBitmap 函式](-gdiplus-cachedbitmap-flat.md)
-   [CustomLineCap 函式](-gdiplus-customlinecap-flat.md)
-   [字型函數](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [圖形函式](-gdiplus-graphics-flat.md)
-   [GraphicsPath 函式](-gdiplus-graphicspath-flat.md)
-   [HatchBrush 函式](-gdiplus-hatchbrush-flat.md)
-   [影像函式](-gdiplus-image-flat.md)
-   [ImageAttributes 函式](-gdiplus-imageattributes-flat.md)
-   [LinearGradientBrush 函式](-gdiplus-lineargradientbrush-flat.md)
-   [矩陣函數](-gdiplus-matrix-flat.md)
-   [記憶體函數](-gdiplus-memory-flat.md)
-   [通知函數](-gdiplus-notification-flat.md)
-   [PathGradientBrush 函式](-gdiplus-pathgradientbrush-flat.md)
-   [PathIterator 函式](-gdiplus-pathiterator-flat.md)
-   [畫筆函數](-gdiplus-pen-flat.md)
-   [區域函數](-gdiplus-region-flat.md)
-   [SolidBrush 函式](-gdiplus-solidbrush-flat.md)
-   [字串格式函數](-gdiplus-stringformat-flat.md)
-   [文字函數](-gdiplus-text-flat.md)
-   [材質筆刷函數](-gdiplus-texturebrush-flat.md)

 

 
