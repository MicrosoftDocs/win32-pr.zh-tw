---
description: CDrawImage 類別是管理影片轉譯器篩選器繪圖的 helper 類別。
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: 'CDrawImage 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 001b91338b2956f663d777cbc9597fa2d9a478f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993671"
---
# <a name="cdrawimage-class"></a>CDrawImage 類別

`CDrawImage`類別是管理影片轉譯器篩選器繪圖的 helper 類別。 所有繪製作業都是使用 GDI 來執行。 此類別不提供任何以 DirectDraw 轉譯的支援。 `CDrawImage`類別需要擁有篩選器也會使用 [**CBaseWindow**](cbasewindow.md)類別，此類別會管理影片視窗。 此函式 `CDrawImage` 會採用 **CBaseWindow** 物件的指標。

下圖顯示在自訂影片轉譯器篩選中使用此類別的慣用方式。

![使用 cdrawimage 的自訂影片轉譯器](images/videorenderer.png)

若要使用此類別，請執行下列動作：

-   當 pin 連接時，請呼叫 [**CDrawImage：： NotifyMediaType**](cdrawimage-notifymediatype.md) 和 [**CDrawImage：： NotifyAllocator**](cdrawimage-notifyallocator.md) 方法。
-   當媒體類型變更時，請再次呼叫 **NotifyMediaType** 。
-   在任何轉譯發生之前，呼叫 [**CDrawImage：： SetDrawCoNtext**](cdrawimage-setdrawcontext.md)。
-   如果來源矩形變更，請呼叫 [**CDrawImage：： SetSourceRect**](cdrawimage-setsourcerect.md) ，如果目標矩形變更，則呼叫 [**CDrawImage：： SetTargetRect**](cdrawimage-settargetrect.md) 。
-   管理調色盤影像的選擇區，如接下來的調色板一節所述。

## <a name="allocators"></a>配置器

上圖所示的篩選器會使用自訂配置器類別 [**CImageAllocator**](cimageallocator.md)。 此配置器會使用 GDI **CreateDIBSection** 函數，在共用記憶體中建立 dib。 配置器所建立的範例是 [**CImageSample**](cimagesample.md) 物件。

如果篩選準則擁有連接的配置器，則會保證媒體範例是 [**CImageSample**](cimagesample.md) 物件。 在這種情況下， **CDrawImage** 物件可以使用 **BitBlt** 或 StretchBlt 來優化繪圖。 否則，它必須使用較慢的 **SetDIBitsToDevice** 或 **StretchDIBits** 函數。 更快的選項是由 [**CDrawImage：： FastRender**](cdrawimage-fastrender.md) 方法所執行，這是 [**CDrawImage：： SlowRender**](cdrawimage-slowrender.md) 方法的慢速選項。  (儘管名稱一樣，您可能不會在 **SlowRender** 中看到較大的效能衝擊，尤其是在較新的硬體上。 ) 

## <a name="palettes"></a>調色板

如果 [**FastRender**](cdrawimage-fastrender.md) 方法用於繪圖，且影像是調色盤，則篩選器需要管理該調色板，如下所示：

-   [**CImageSample**](cimagesample.md)類別包含儲存在 [**DIBDATA**](dibdata.md)結構中的調色板版本號碼。 此值會在配置器建立範例時初始化。
-   **CDrawImage** 類別也包含在建立時初始化的調色板版本號碼。
-   當媒體類型變更為新的調色盤格式時，請呼叫 [**CDrawImage：： IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)。 這個方法會遞增 **CDrawImage** 物件的調色板版本號碼。 如果篩選使用 [**CImagePalette**](cimagepalette.md) 類別來管理調色板資訊，只要媒體類型變更，您就可以直接呼叫 [**CImagePalette：:P reparepalette**](cimagepalette-preparepalette.md) 。 只有在必要時， **PreparePalette** 方法才會遞增元件的版本。
-   [**FastRender**](cdrawimage-fastrender.md)方法會比較 **CDrawImage** 調色板版本與範例的調色板版本。 如果範例的版本號碼晚于 **CDrawImage** 版本號碼之後， **FastRender** 方法就會呼叫 [**CDrawImage：： UpdateColourTable**](cdrawimage-updatecolourtable.md)。 **UpdateColourTable** 方法會使用 GDI **SetDIBColorTable** 函式來設定裝置內容中的色彩表。 此外，範例上的調色板版本會更新為目前的版本號碼。
-   如果 pin 重新連接，則篩選準則應該呼叫 [**CDrawImage：： ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) 來重設調色板版本。 在 pin 重新連接時，配置器會重新配置所有範例。



| 受保護的成員變數                                            | Description                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bStretch**](cdrawimage-m-bstretch.md)                          | 指出是否必須延展影片影像以符合目的地視窗。                                              |
| [**m \_ bUsingImageAllocator**](cdrawimage-m-busingimageallocator.md)  | 指出釘選連接的配置器是否為 **CImageAllocator** 物件。                                         |
| [**m \_ EndSample**](cdrawimage-m-endsample.md)                        | 指定最新範例的停止時間。                                                                              |
| [**m \_ hdc**](cdrawimage-m-hdc.md)                                    | 主控視窗的裝置內容控制碼。                                                                              |
| [**m \_ MemoryDC**](cdrawimage-m-memorydc.md)                          | 主控視窗的記憶體裝置內容控制碼。                                                                       |
| [**m \_ PaletteVersion**](cdrawimage-m-paletteversion.md)              | 用來追蹤調色板變更的時間。                                                                                         |
| [**m \_ pBaseWindow**](cdrawimage-m-pbasewindow.md)                    | 擁有 **CBaseWindow** 物件的指標。                                                                                   |
| [**m \_ pMediaType**](cdrawimage-m-pmediatype.md)                      | 目前媒體類型的指標。                                                                                              |
| [**m \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | 指定繪圖的來源矩形。                                                                                     |
| [**m \_ StartSample**](cdrawimage-m-startsample.md)                    | 指定最新範例的開始時間。                                                                             |
| [**m \_ TargetRect**](cdrawimage-m-targetrect.md)                      | 指定繪圖的目標矩形。                                                                                     |
| 保護方法                                                     | Description                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | 在影片影像上方繪製媒體範例的時間戳記。                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | 使用 **BitBlt** 或 **StretchBlt** 函數繪製影片影像。                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | 計算影片影像是否必須伸展。                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | 使用 **SetDIBitsToDevice** 或 **StretchDIBits** 函數繪製影片影像。                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | 以新的調色板更新色彩表。                                                                                     |
| 公用方法                                                        | Description                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | 函式方法。                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | 在影片視窗中繪製影片框架。                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | 從媒體範例將影像繪製到指定的裝置內容。                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | 抓取元件的版本。                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | 抓取目前的來源矩形。                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | 抓取目前的目的地矩形。                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | 遞增元件的版本。                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | 通知物件，連接的配置器 `CDrawImage` 是否為 **CImageAllocator** 物件。                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | 不支援。                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | 通知目前媒體類型的物件。                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | 不支援。                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | 重設調色板版本。                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | 如果原生影片大小和媒體類型格式之間有差異，則調整指定的來源矩形。 虛擬。 |
| [**SetDrawCoNtext**](cdrawimage-setdrawcontext.md)                   | 設定用於繪製的裝置內容。                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | 設定來源矩形。                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | 設定目標矩形。                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | 指出目前的配置器是否為 [**CImageAllocator**](cimageallocator.md) 物件。                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




