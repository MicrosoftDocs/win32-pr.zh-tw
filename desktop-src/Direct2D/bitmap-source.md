---
title: 點陣圖來源效果
description: 使用點陣圖來源效果從 IWICBitmapSource 產生 ID2D1Image，以做為效果圖形中的輸入。
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- 點陣圖來源效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844240"
---
# <a name="bitmap-source-effect"></a>點陣圖來源效果

使用點陣圖來源效果從 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)產生 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) ，以做為效果圖形中的輸入。 此效果會執行 CPU 的調整和旋轉。 它也可以選擇性地產生系統記憶體 mipmap，這可以是在各種減少解析度上主動調整非常大型影像的效能優化。

> [!Note]  
> 點陣圖來源效果接受其輸入做為屬性，而不是影像輸入。 您必須使用 [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法，而不是 [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) 方法。 *WicBitmapSource* 屬性可讓您指定影像輸入資料。

 

這項效果的 CLSID 是 CLSID \_ D2D1BitmapSource。

-   [效果屬性](#effect-properties)
-   [插補模式](#interpolation-modes)
-   [Orientation](#orientation)
-   [Alpha 模式](#alpha-modes)
-   [備註](#remarks)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> D2D1 \_ BITMAPSOURCE \_ 的 \_ \_ 版本 WIC 點陣圖 \_ 來源<br/>         | [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) ，其中包含要載入的影像資料。<br/> 此類型為 [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource)。<br/> 預設值是 NULL。<br/>                                                                                                                                                                                                                   |
| 調整<br/> D2D1 \_ BITMAPSOURCE \_ 的 \_ 範圍調整<br/>                                 | 以 X 和 Y 方向的比例量。 效果會將寬度乘以 X 值，並將高度乘以 Y 值。 這個屬性是 \_ \_ 定義為： (X 刻度、Y 尺規) 的 D2D1 向量2f。 尺規數量為 FLOAT、無量，且必須為正數或0。<br/> 此類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {1.0 f、1.0 f}。<br/>                                                                           |
| InterpolationMode.<br/> D2D1 \_ BITMAPSOURCE \_ 的 \_ 內插補點 \_ 模式<br/>      | 用來調整影像的插補模式。 如需詳細資訊，請參閱 [插補模式](#interpolation-modes) 。<br/> 如果模式停用 mipmap，則 BitmapSouce 會以 Scale 和 EnableDPICorrection 屬性所決定的解析度來快取影像。<br/> 此類型為 D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式。<br/> 預設值為 D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 線性。<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ 的 \_ 支援 \_ DPI \_ 修正<br/> | 如果您將此設定為 TRUE，效果將會調整輸入影像，以將 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) 所報告的 DPI 轉換成裝置內容的 DPI。 效果會使用您使用 InterpolationMode 屬性設定的插補模式。 如果您將此設定為 FALSE，則效果會使用96.0 的 DPI 作為輸出影像。<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>   |
| AlphaMode<br/> D2D1 \_ BITMAPSOURCE \_ 的 \_ ALPHA \_ 模式<br/>                       | 輸出的 Alpha 模式。 這可以是預乘或直接。 如需詳細資訊，請參閱 [Alpha 模式](#alpha-modes) 。<br/> 此類型為 D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式。<br/> 預設值是預乘的 D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式 \_ 。<br/>                                                                                                                                                              |
| Orientation<br/> D2D1 \_ BITMAPSOURCE 的 \_ 主張 \_ 方向<br/>                     | 要在影像上執行的翻轉和/或旋轉操作。 如需詳細資訊，請參閱 [方向](#orientation) 。<br/> 此類型為 D2D1 \_ BITMAPSOURCE \_ 方向。<br/> 預設值為 D2D1 \_ BITMAPSOURCE \_ 方向預設值 \_ 。<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>插補模式

效果會在縮放影像或更正 DPI 時，使用此模式來進行插補。 此效果使用的插補模式是由 CPU 計算，而不是 GPU。



| Name                                                       | 描述                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 BITMAPSOURCE 插補模式 | 範例最接近的單一點，並使用該點。 不會產生 mipmap。                                                                                                                                                           |
| D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 線性            | 使用四個點取樣和線性插補。 不會產生 mipmap。                                                                                                                                                        |
| D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 立方             | 使用16個範例三核心來進行插補。 不會產生 mipmap。                                                                                                                                                          |
| D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ FANT              | 使用 WIC fant 插補，與 [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) 介面相同。 不會產生 mipmap。                                                                                       |
| D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ MIPMAP \_ 線性    | 使用雙線性插補，在系統記憶體中產生 mipmap 鏈。 針對每個 mipmap，效果會使用雙線性插補來調整為最接近的0.5 倍數，然後使用線性插補來調整剩餘的數量。 |



 

## <a name="orientation"></a>Orientation

方向屬性可以用來套用內嵌于影像內的 EXIF 方向旗標。



| Name                                                                    | 描述                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 預設值                                | 預設值。 效果不會變更輸入的方向。   |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ \_ 水準翻轉                       | 水準翻轉影像。                                      |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE180                   | 以順時針旋轉180度旋轉影像。                           |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE180 \_ 翻轉 \_ 水準 | 以順時針180度旋轉影像，並水準翻轉。 |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE270 \_ 翻轉 \_ 水準 | 以順時針270度旋轉影像，並水準翻轉。 |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE90                    | 以順時針旋轉90度旋轉影像。                            |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE90 \_ 翻轉 \_ 水準  | 以順時針90度旋轉影像，並水準翻轉。  |
| D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE270                   | 以順時針旋轉270度旋轉影像。                           |



 

此程式碼片段示範如何從) propkey 中定義的 EXIF 方向值轉換 (在 D2D1 \_ BITMAPSOURCE \_ 方向值。


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Alpha 模式



| Name                                           | 描述                                            |
|------------------------------------------------|--------------------------------------------------------|
| 預 \_ 乘的 D2D1 BITMAPSOURCE \_ ALPHA \_ 模式 \_ | 效果輸出使用預乘 Alpha。<br/> |
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式 \_ 直接      | 效果輸出會使用直接 Alpha。<br/>      |



 

## <a name="remarks"></a>備註

若要在同時使用 WIC 和 [Direct2D](./direct2d-portal.md) 時將效能優化，您應該使用 [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) ，根據您的應用程式案例和映射的原生精確度，轉換成適當的像素格式。

在大多數情況下，您的應用程式 [Direct2D](./direct2d-portal.md) 管線只需要每個通道8個位 (bpc) 的精確度，或者影像只提供8個 bpc 的有效位數，因此您應該轉換為 GUID \_ WICPixelFormat32bppPBGRA。 但是，如果您想要利用影像所提供的額外精確度 (例如，以超過 8 bpc 的精確度來儲存 XR 或 TIFF) ，您應該使用以 RGBA 為基礎的像素格式。 下表提供更多詳細資料。



| 需要的精確度   | 影像的原生精確度 | 建議的像素格式                |
|---------------------|-------------------------------|-----------------------------------------|
| 每個通道8個位  | <= 每個通道8位      | GUID \_ WICPixelFormat32bppPBGRA          |
| 越高越好 | <= 每個通道8位      | GUID \_ WICPixelFormat32bppPBGRA          |
| 越高越好 | 每個通道 > 8 個位       | RGBA 頻道順序，預乘 Alpha |



 

由於許多影像格式支援多個精確度層級，因此您應該使用 [**IWICBitmapSource：： GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) 來取得影像的原生像素格式，然後使用 [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) 來判斷該格式的每個有效位數通道位數。 另請注意，並非所有硬體都支援高精確度的像素格式。 在這些情況下，您的應用程式可能需要切換回彎曲裝置，以支援高精確度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

