---
title: 如何建立點陣圖筆刷
description: 顯示如何使用 Direct2D 建立點陣圖筆刷。
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274d359b8ad8298a4e45d01014a6e9b19aa58c4b81725c5d8c41ac931e24eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569291"
---
# <a name="how-to-create-a-bitmap-brush"></a>如何建立點陣圖筆刷

若要建立點陣圖筆刷，請使用 [**ID2D1RenderTarget：： CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法，並指定點陣圖筆刷屬性。 某些多載可讓您指定筆刷屬性。 下列程式碼示範如何建立點陣圖筆刷來填滿正方形，以及建立實心黑色筆刷來繪製正方形的外框。 程式碼會產生下列螢幕擷取畫面中顯示的輸出。

> [!Note]  
> 從 Windows 8 開始，您可以使用 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面上的 [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1))方法來建立 [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) ，而不是 **ID2D1BitmapBrush**。 **ID2D1BitmapBrush1** 會將高品質的縮放模式新增至點陣圖筆刷。

 

![填滿植物點陣圖之方塊的螢幕擷取畫面](images/brushes-ovw-bitmap.png)

1.  宣告 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)型別的變數。
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  從資源載入點陣圖。 如需詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  選擇擴充模式 ([**D2D1 \_ 延伸 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) 和插補模式 (點陣圖筆刷的 [**D2D1 \_ 點陣圖 \_ 插補 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) ，然後呼叫 [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法來建立筆刷，如下列程式碼所示。
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 