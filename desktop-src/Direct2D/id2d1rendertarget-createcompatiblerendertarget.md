---
title: 'ID2D1RenderTarget CreateCompatibleRenderTarget 方法 (D2d1 .h) '
description: 建立新的點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用。
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- CreateCompatibleRenderTarget 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9015586109ff5015743874d18b604de919a9464a655383cf4d47aabb7b7acf35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432778"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>ID2D1RenderTarget：： CreateCompatibleRenderTarget 方法

建立新的點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget (D2D1 \_ size \_ F、D2D1 \_ SIZE \_ U、D2D1 \_ 圖元 \_ FORMAT、D2D1 \_ 相容 \_ 轉譯 \_ 目標 \_ 選項、ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | 建立點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用。<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget (D2D1 \_ size \_ F \* 、D2D1 \_ SIZE \_ U \* 、D2D1 \_ 圖元 \_ FORMAT \* 、D2D1 \_ 相容 \_ 轉譯 \_ 目標 \_ 選項、ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | 建立點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用。 <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget (ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | 建立新的點陣圖呈現目標，以在與目前轉譯目標相容的中繼螢幕外繪圖期間使用，而且具有相同的大小、DPI 和像素格式 (但非 Alpha 模式) 為目前的轉譯目標。 <br/>         |
| [**CreateCompatibleRenderTarget (D2D1 \_ SIZE \_ F，ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | 建立新的點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用，而且具有相同的像素格式 (但 Alpha 模式) 為目前的轉譯目標。 <br/>                        |
| [**CreateCompatibleRenderTarget (D2D1 \_ 大小 \_ F、D2D1 \_ 大小 \_ U、ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | 建立點陣圖呈現目標，以在與目前轉譯目標相容的中繼離螢幕繪圖期間使用。 新的點陣圖轉譯目標具有相同的像素格式 (但非 Alpha 模式) 為目前的轉譯目標。 <br/> |
| [**CreateCompatibleRenderTarget (D2D1 \_ size \_ F、D2D1 \_ SIZE \_ U、D2D1 \_ 圖元 \_ FORMAT、ID2D1BitmapRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | 建立點陣圖呈現目標，以便在與目前轉譯目標相容的中繼螢幕外繪圖期間使用。 <br/>                                                                                                            |



## <a name="examples"></a>範例

下列範例會使用 **CreateCompatibleRenderTarget** 方法來建立 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) ，並使用它來繪製方格模式。 格線模式會用來做為 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)的來源。


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



下列程式碼範例會使用筆刷來繪製模式。


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



此範例中省略了程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
