---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: CachedBitmap 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebb19648e38425561d1a1609c5f71368718ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692559"
---
# <a name="cachedbitmap-functions"></a>CachedBitmap 函式

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) c + + 類別包裝。

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>CachedBitmap 函式和對應的包裝函式方法



| 一般函數                                                                                                             | 包裝函式方法                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap ( GpBitmap \* bitmap、GpGraphics \* Graphics、GpCachedBitmap \* \* cachedBitmap )    | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | 根據 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)物件和 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件建立 [**CachedBitmap：： CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_))物件。 快取的點陣圖會接受 **點陣圖** 物件的圖元資料，並將其儲存為針對與 **圖形** 物件相關聯的顯示裝置所優化的格式。 |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap (GpCachedBitmap \* cachedBitmap) <br/>                                      | ~ CachedBitmap ()                                                                                  | 清除 [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) 物件所使用的資源。                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap ( GpGraphics \* graphics、GpCachedBitmap \* CACHEDBITMAP、int x、int y )             | [**圖形：:D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | [**Graphics：:D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)方法會繪製儲存在 [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)物件中的影像。                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits ( HENHMETAFILE hemf、UINT cbData16、LPBYTE pData16、INT iMapMode、INT eFlags ) <br/> | [**中繼檔：： EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | 將增強格式的中繼檔轉換成 Windows 中繼檔格式 (WMF) 中繼檔，並將轉換的記錄儲存在指定的緩衝區中。                                                                                                                                                                                                                                                                                       |



 

 

