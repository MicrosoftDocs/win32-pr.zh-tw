---
description: 下列函式可用於點陣圖。
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: " (Windows GDI) 的點陣圖函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991290"
---
# <a name="bitmap-functions-windows-gdi"></a> (Windows GDI) 的點陣圖函數

下列函式可用於點陣圖。



| 函式                                                 | 描述                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | 顯示具有透明或半透明圖元的點陣圖。  |
| [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | 執行位區區塊轉送。                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | 建立點陣圖。                                              |
| [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | 建立點陣圖。                                              |
| [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | 建立與裝置相容的點陣圖。                     |
| [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | 從 DIB 建立裝置相依點陣圖 (DDB) 。            |
| [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | 建立應用程式可直接寫入的 DIB。         |
| [**ExtFloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | 使用目前的筆刷來填滿顯示介面的區域。   |
| [**GetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | 取得點陣圖的維度。                               |
| [**GetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | 從 DIB 區段點陣圖取出 RGB 色彩值。          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | 將點陣圖複製到緩衝區。                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | 取得指定座標之圖元的 RGB 色彩值。   |
| [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | 取得目前的延展模式。                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | 填滿矩形和三角形結構。                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | 從模組的可執行檔載入點陣圖。                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | 結合來源和目的點陣圖中的色彩資料。 |
| [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | 執行位區區塊轉送。                                 |
| [**SetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | 將慣用的維度設定為點陣圖。                     |
| [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | 在 DIB 中設定 RGB 值。                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | 使用 DIB 中的色彩資料，設定點陣圖中的圖元。       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | 使用 DIB 中的色彩資料，設定矩形中的圖元。    |
| [**Bitmap.setpixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | 設定圖元的色彩。                                    |
| [**SetPixelV**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | 將圖元設定為色彩的最佳近似。             |
| [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | 設定點陣圖延展模式。                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | 複製並伸展或壓縮點陣圖。                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | 複製 DIB 中的色彩資料。                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | 執行色彩資料的位區塊傳輸。                   |



 

## <a name="obsolete-functions"></a>過時的函式

下列函式僅提供給與16位版本的 Microsoft Windows 相容：

-   [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**GetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**SetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



