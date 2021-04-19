---
title: 如何建立點陣圖筆刷
description: 顯示如何使用 Direct2D 建立點陣圖筆刷。
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969917"
---
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="e6871-103">如何建立點陣圖筆刷</span><span class="sxs-lookup"><span data-stu-id="e6871-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="e6871-104">若要建立點陣圖筆刷，請使用 [**ID2D1RenderTarget：： CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法，並指定點陣圖筆刷屬性。</span><span class="sxs-lookup"><span data-stu-id="e6871-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="e6871-105">某些多載可讓您指定筆刷屬性。</span><span class="sxs-lookup"><span data-stu-id="e6871-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="e6871-106">下列程式碼示範如何建立點陣圖筆刷來填滿正方形，以及建立實心黑色筆刷來繪製正方形的外框。</span><span class="sxs-lookup"><span data-stu-id="e6871-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="e6871-107">程式碼會產生下列螢幕擷取畫面中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="e6871-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="e6871-108">從 Windows 8 開始，您可以使用 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面上的 [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1))方法來建立 [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) ，而不是 **ID2D1BitmapBrush**。</span><span class="sxs-lookup"><span data-stu-id="e6871-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="e6871-109">**ID2D1BitmapBrush1** 會將高品質的縮放模式新增至點陣圖筆刷。</span><span class="sxs-lookup"><span data-stu-id="e6871-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![填滿植物點陣圖之方塊的螢幕擷取畫面](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="e6871-111">宣告 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)型別的變數。</span><span class="sxs-lookup"><span data-stu-id="e6871-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="e6871-112">從資源載入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="e6871-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="e6871-113">如需詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="e6871-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
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

    

3.  <span data-ttu-id="e6871-114">選擇擴充模式 ([**D2D1 \_ 延伸 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) 和插補模式 (點陣圖筆刷的 [**D2D1 \_ 點陣圖 \_ 插補 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) ，然後呼叫 [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法來建立筆刷，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="e6871-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e6871-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6871-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6871-116">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="e6871-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 