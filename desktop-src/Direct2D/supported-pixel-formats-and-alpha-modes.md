---
title: 支援的像素格式和 Alpha 模式
description: 描述每個呈現目標型別所支援的像素格式和 Alpha 模式。
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D，像素格式
- Direct2D，Alpha 模式
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917158"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>支援的像素格式和 Alpha 模式

本主題說明 Direct2D 各個部分所支援的像素格式和 Alpha 模式，包括每個轉譯目標型別、 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)和 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)。 包含以下幾節。

-   [針對 DXGI 映射來源支援的 YUV 格式](#supported-yuv-formats-for-dxgi-image-source)
-   [指定呈現目標的像素格式](#specifying-a-pixel-format-for-a-render-target)
-   [支援的 ID2D1HwndRenderTarget 格式](#supported-formats-for-id2d1hwndrendertarget)
-   [支援的 ID2D1DeviceCoNtext 格式](#supported-formats-for-id2d1devicecontext)
-   [相容轉譯目標支援的格式](#supported-formats-for-compatible-render-target)
-   [適用于 DXGI 介面轉譯目標的支援格式](#supported-formats-for-dxgi-surface-render-target)
-   [WIC 點陣圖轉譯目標支援的格式](#supported-formats-for-wic-bitmap-render-target)
-   [支援的 ID2D1DCRenderTarget 格式](#supported-formats-for-id2d1dcrendertarget)
-   [為 ID2D1Bitmap 指定像素格式](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [支援的 WIC 格式](#supported-wic-formats)
-   [使用不支援的格式](#using-an-unsupported-format)
-   [關於 Alpha 模式](#about-alpha-modes)
    -   [關於預乘和直接 Alpha 模式](#about-premultiplied-and-straight-alpha-modes)
    -   [直線和預乘 Alpha 之間的差異](#the-differences-between-straight-and-premultiplied-alpha)
    -   [呈現目標的 Alpha 模式](#alpha-mode-for-render-targets)
    -   [ClearType 和 Alpha 模式](#cleartype-and-alpha-modes)
-   [相關主題](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>針對 DXGI 映射來源支援的 YUV 格式

[**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)是一種抽象的圖元提供者。 它可以從 WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) 或 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)) 來具現化。

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) 支援與 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)相同的一組像素格式和 Alpha 模式。

除了上述以外，從 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)具現化的 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)也支援一些 YUV 像素格式，包括將平面資料分割成多個表面。 如需每個像素格式需求的詳細資訊，請參閱 [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) 。



| 格式                    |
|---------------------------|
| DXGI \_ 格式 \_ AYUV        |
| DXGI \_ 格式 \_ NV12        |
| DXGI \_ 格式 \_ YUY2        |
| DXGI \_ 格式 \_ P208        |
| DXGI \_ 格式 \_ V208        |
| DXGI \_ 格式 \_ V408        |
| DXGI \_ 格式 \_ R8 \_ UNORM   |
| DXGI \_ 格式 \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>指定呈現目標的像素格式

當您建立轉譯目標時，您必須指定它的像素格式。 若要指定像素格式，您可以使用 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)結構來設定 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 **pixelFormat** 成員。 然後，將該結構傳遞至適當的 Create 方法，例如 [**ID2D1Factory：： CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))。

[**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)結構有兩個欄位：

-   **format**（ [DXGI \_ 格式](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值），描述每個圖元中通道的大小和相片順序，以及
-   **Alpha**， [**D2D1 \_ Alpha \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 值，描述如何解讀 Alpha 資訊。

下列範例會建立 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) 結構，並用它來指定 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)的像素格式和 Alpha 模式。


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



不同的呈現目標支援不同的格式和 Alpha 模式組合。 下列各節列出每個呈現目標所支援的格式和 Alpha 組合。

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>支援的 ID2D1HwndRenderTarget 格式

[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)支援的格式取決於它是使用硬體或軟體所呈現，還是 Direct2D 預設會自動處理轉譯模式。

> [!Note]  
> 建議您使用 [**DXGI \_ format \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 做為像素格式，以獲得更好的效能。 這對軟體呈現目標特別有用。 BGRA 格式目標的執行效果優於 RGBA 格式。

 

當您建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)時，您可以使用 [**D2D1 \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構來指定轉譯選項。 選項包括像素格式，如上一節所述。 此結構的 [類型] 欄位可讓您指定轉譯目標是要呈現給硬體或軟體，還是 Direct2D 應該自動判斷轉譯模式。

若要啟用 Direct2D 以判斷轉譯目標是使用硬體或軟體轉譯，請使用 [**D2D1 \_ 轉譯 \_ 目標 \_ 類型 \_ 預設**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。

下表列出使用 [ [**D2D1 轉譯 \_ \_ 目標 \_ 類型] \_ 預設**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)設定所建立之 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)物件的支援格式。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ 未知         | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知         | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ 未知         | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

若要強制轉譯目標使用硬體呈現，請使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 硬體**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。 下表列出明確使用硬體轉譯的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件所支援的格式。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ 未知         | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知         | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ 未知         | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

若要強制轉譯目標使用軟體呈現，請使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 軟體**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。 下表列出明確使用軟體轉譯的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件所支援的格式。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ 未知         | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知         | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ 未知         | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

無論 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 是否為硬體加速，預設的 [dxgi \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式都會使用 [dxgi \_ 格式 \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ，而 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式預設會使用 **D2D1 \_ Alpha \_ 模式 \_ 忽略** 。

## <a name="supported-formats-for-id2d1devicecontext"></a>支援的 ID2D1DeviceCoNtext 格式

從 Windows 8 開始，[**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)會利用更多的 [**Direct3D 高色彩格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)，例如：

-   DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM
-   DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT

使用 [**ID2D1DeviceCoNtext：： IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) 方法來查看格式是否適用于特定的裝置內容。 這些格式也可以在 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)上運作。

這些格式除了 Windows 7 中的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)介面所支援的格式之外。 如需詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。

## <a name="supported-formats-for-compatible-render-target"></a>相容轉譯目標支援的格式

相容的轉譯目標 (由其中一個 [**ID2D1RenderTarget：： CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))方法所建立的 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) ，) 會繼承其所建立之轉譯目標的支援格式和 Alpha 模式。 相容的轉譯目標也支援下列格式和 Alpha 模式組合，無論其父系支援何種組合。



| 格式                  | Alpha 模式                       |
|-------------------------|----------------------------------|
| DXGI \_ 格式 \_ A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ A8 \_ UNORM | \_直接 D2D1 ALPHA \_ 模式 \_      |
| DXGI \_ 格式 \_ 未知   | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

[ [DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式] 預設會使用父轉譯目標格式，而 [ [**D2D1 \_ Alpha \_ ] 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 [Alpha] 模式則使用預設預 **乘的 D2D1 \_ Alpha \_ 模式 \_** 。

## <a name="supported-formats-for-dxgi-surface-render-target"></a>適用于 DXGI 介面轉譯目標的支援格式

DXGI 轉譯目標是由其中一個 [**ID2D1Factory：： CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))方法所建立的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。 它支援下列格式和 Alpha 模式組合。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ A8 \_ UNORM       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ A8 \_ UNORM       | \_直接 D2D1 ALPHA \_ 模式 \_      |
| DXGI \_ 格式 \_ 未知         | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知         | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |



 

> [!Note]  
> 格式必須符合 dxgi 介面呈現目標所繪製之 DXGI 介面的格式。

 

[ [Dxgi \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ] 格式預設會使用 dxgi 介面格式。 請勿使用 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式搭配 DXGI 介面轉譯目標。 它沒有預設值，而且會導致 DXGI 表面呈現目標建立失敗。

## <a name="supported-formats-for-wic-bitmap-render-target"></a>WIC 點陣圖轉譯目標支援的格式

WIC 點陣圖轉譯目標是由其中一個 [**ID2D1Factory：： CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))方法所建立的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。 它支援下列格式和 Alpha 模式組合。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ A8 \_ UNORM       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ A8 \_ UNORM       | \_直接 D2D1 ALPHA \_ 模式 \_      |
| DXGI \_ 格式 \_ A8 \_ UNORM       | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ 未知         | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知         | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ 未知         | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

WIC 點陣圖目標的像素格式必須符合 WIC 點陣圖的像素格式。

在預設情況下，[DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式使用 wic 點陣圖格式，而 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式預設會使用 wic 點陣圖 Alpha 模式。

## <a name="supported-formats-for-id2d1dcrendertarget"></a>支援的 ID2D1DCRenderTarget 格式

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)支援下列格式和 Alpha 模式組合。



| 格式                        | Alpha 模式                       |
|-------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |



 

請勿使用 [DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 的格式或 [**D2D1 \_ Alpha 模式的 \_ \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha 模式與 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)。 它沒有預設值，而且會造成 **ID2D1DCRenderTarget** 建立失敗。

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>為 ID2D1Bitmap 指定像素格式

一般而言， [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 物件支援下列格式和 Alpha 模式 (有一些限制，如接下來的段落所述。 ) 



| 格式                                                      | Alpha 模式                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM                               | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM                               | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ A8 \_ UNORM                                     | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ A8 \_ UNORM                                     | \_直接 D2D1 ALPHA \_ 模式 \_      |
| DXGI \_ 格式 \_ A8 \_ UNORM                                     | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ 未知                                       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ 未知                                       | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ 未知                                       | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM (Windows 8.1 和更新版本，只能)  | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能)       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能)       | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能)       | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能)       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能)       | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能)       | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |
| DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能)       | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_ |
| DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能)       | D2D1 \_ ALPHA \_ 模式 \_ 忽略        |
| DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能)       | 未知的 D2D1 \_ ALPHA \_ 模式 \_       |



 

當您使用 [**ID2D1RenderTarget：： CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)方法時，您可以使用 [**D2D1 \_ BITMAP \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties)結構的 **pixelFormat** 欄位來指定新轉譯目標的像素格式。 它必須符合 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 來源的像素格式。

當您使用 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap))方法時，您可以使用 [**D2D1 \_ 點陣圖 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties)結構的 **pixelFormat** 欄位 (而不是 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 **pixelFormat** 成員) 指定新轉譯目標的像素格式。 它必須符合 WIC 點陣圖來源的像素格式。

> [!Note]  
> 如需 (BCn) 像素格式之區塊壓縮的詳細資訊，請參閱 [區塊壓縮](block-compression.md)。

 

### <a name="supported-wic-formats"></a>支援的 WIC 格式

當您使用 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap))方法從 WIC 點陣圖建立點陣圖，或搭配 [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)方法時，WIC 來源的格式必須是 Direct2D 所支援的格式。



| WIC 格式                     | 對應的 DXGI 格式     | 對應的 Alpha 模式                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | DXGI \_ 格式 \_ A8 \_ UNORM       | 預 \_ \_ 乘的 D2D1 Alpha 模式 \_ 直接或 D2D1 \_ Alpha \_ 模式 \_ |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM | D2D1 \_ Alpha \_ 模式 \_ 的預乘或 D2D1 \_ Alpha \_ 模式 \_ 略過   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ 模式 \_ 忽略                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM | 預 \_ 乘的 D2D1 ALPHA \_ 模式 \_                                |



 

如需示範如何將 WIC 點陣圖轉換成支援格式的範例，請參閱 [如何從檔案載入點陣圖](how-to-load-a-direct2d-bitmap-from-a-file.md)。

## <a name="using-an-unsupported-format"></a>使用不支援的格式

使用上述表格中所列的像素格式和 Alpha 模式以外的任何組合，會導致 [**D2DERR \_ 不支援的 \_ 圖元 \_ 格式**](direct2d-error-codes.md) 或 **電子 \_ INVALIDARG** 錯誤。

## <a name="about-alpha-modes"></a>關於 Alpha 模式

### <a name="about-premultiplied-and-straight-alpha-modes"></a>關於預乘和直接 Alpha 模式

[**D2D1 \_ Alpha \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)列舉指出 Alpha 色板是使用預乘 Alpha、直立的 Alpha，還是應該忽略並視為不透明。 若使用直接 Alpha，Alpha 色板會指出一個值，對應至色彩的透明程度。

無論目的地格式為何，色彩一律會藉由 Direct2D 繪製命令和筆刷來視為直接 Alpha。

使用預乘 Alpha 時，每個色頻都會依 Alpha 值調整。 一般而言，沒有色頻值大於 Alpha 色板值。 如果以乘前格式的色頻值大於 Alpha 色板，則標準來源過度混色數學會建立加法 blend。

Alpha 色板本身的值在直線和乘乘的 Alpha 中都相同。

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>直線和預乘 Alpha 之間的差異

使用直接 Alpha 描述 RGBA 色彩時，色彩的 Alpha 值會儲存在 Alpha 色板中。 例如，若要描述60% 不透明的紅色色彩，請使用下列值： (255、0、0、255 \* 0.6) = (255、0、0、153) 。 255值表示全紅色，153 (是 255) 的60% 表示色彩應該有60% 的不透明度。

使用預乘 Alpha 描述 RGBA 色彩時，每個色彩會乘以 Alpha 值： (255 \* 0.6、0 \* 0.6、0 \* 0.6、255 \* 0.6) = (153、0、0、153) 。

無論轉譯目標的 Alpha 模式為何， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 值一律會轉譯為純 Alpha。 例如，當指定要搭配使用預乘 Alpha 模式之轉譯目標使用的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 色彩時，請指定色彩，就像轉譯目標使用的是直接 Alpha 一樣。 當您使用筆刷繪製時，Direct2D 會為您將色彩轉譯成目的地格式。

### <a name="alpha-mode-for-render-targets"></a>呈現目標的 Alpha 模式

無論 Alpha 模式設定為何，轉譯目標的內容都支援透明度。 例如，如果您繪製部分透明的紅色矩形，且其轉譯目標具有 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)的 Alpha 模式，則矩形會顯示為粉紅色 (如果背景是白色) 。

如果您在 Alpha 模式 [**D2D1 預 \_ 乘的 Alpha \_ \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)時繪製部分透明的紅色矩形，矩形會顯示為粉紅色 (假設背景是白色) ，而您可以透過它來查看呈現目標背後的任何內容。 當您使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 轉譯成透明視窗，或當您使用相容的轉譯目標 ([**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 方法所建立的呈現目標，) 建立支援透明度的點陣圖時，這會很有用。

### <a name="cleartype-and-alpha-modes"></a>ClearType 和 Alpha 模式

如果您針對轉譯目標指定 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 以外的 Alpha 模式，則文字消除鋸齒模式會自動從 [**D2D1 \_ 文字 \_ 消除鋸齒模式 \_ CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) 變更為 **D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式灰階**。  (當您指定 **D2D1 \_ Alpha \_ 模式 \_** 的 Alpha 模式時，Direct2D 會根據轉譯目標的種類為您設定 Alpha。 ) 

您可以使用 [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) 方法，將文字消除鋸齒模式變更回 [**D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式 CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)，但是將 CLEARTYPE 文字轉譯成透明介面可能會產生無法預期的結果。 如果您想要將 ClearType 文字轉譯成透明轉譯目標，建議您使用下列其中一種方法。

-   您可以使用 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) 方法，將轉譯目標裁剪至將呈現文字的區域，然後呼叫 [**Clear**](id2d1rendertarget-clear.md) 方法並指定不透明的色彩，然後轉譯您的文字。
-   您可以使用 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) ，在要呈現文字的區域後方繪製不透明的矩形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**D2D1 \_ ALPHA \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[DXGI \_ 格式](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 