---
title: 如何使用點陣圖作為不透明度遮罩
description: 顯示如何使用點陣圖遮罩來裁剪區域。
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42829ab9a873be9adbeca7795dd87aed62a258ce5737db6e3f86612b4ffef43c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259611"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>如何使用點陣圖作為不透明度遮罩

本主題描述如何藉由呼叫 [**ID2D1Factory：： FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) 方法，使用點陣圖作為 opacty mask。 不透明度遮罩是一種點陣圖，可提供由 Alpha 色板表示的涵蓋範圍資訊，以控制所呈現內容的透明度。 這種方法比使用具有不透明度遮罩的圖層更有效率。 如需詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。

**若要裁剪區域**

1.  從資源載入原始點陣圖。 如需有關如何載入點陣圖的詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。
2.  從資源載入點陣圖遮罩。
3.  使用原始點陣圖建立點陣圖筆刷。 如需有關如何建立點陣圖筆刷的詳細資訊，請參閱 [如何建立點陣圖筆刷](how-to-create-a-bitmap-brush.md)。
4.  呼叫 [**ID2D1Factory：： SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 可在轉譯目標上設定消除鋸齒模式，以 D2D1 \_ \_ \_ 別名為 [**ID2D1Factory：： FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 的鋸齒消除鋸齒模式運作。
5.  使用點陣圖遮罩和轉譯目標上的點陣圖筆刷來呼叫 [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) ，以填滿剪輯。

下圖顯示左邊的原始點陣圖、中間的點陣圖遮罩，以及裁剪到右邊遮罩的點陣圖。

![金魚點陣圖、從點陣圖建立的魚狀遮罩，以及遮罩後產生的魚形點陣圖的圖例](images/cliparegion-opacitymask.png)

下列程式碼示範如何使用上圖所示的遮罩來裁剪區域。 它會先載入原始點陣圖和點陣圖遮罩。 然後使用原始點陣圖建立點陣圖筆刷。


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



然後，它會呼叫 [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 來設定消除鋸齒模式。 呼叫 [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) ，以使用點陣圖遮罩來裁剪原始點陣圖。


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



如需不透明度遮罩的詳細資訊，請參閱 [不透明度遮罩總覽](opacity-masks-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 