---
title: 如何調整物件
description: 顯示如何調整物件。
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463501"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="1d357-103">如何調整物件</span><span class="sxs-lookup"><span data-stu-id="1d357-103">How to Scale an Object</span></span>

<span data-ttu-id="1d357-104">本主題說明如何使用 [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別來調整物件。</span><span class="sxs-lookup"><span data-stu-id="1d357-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="1d357-105">若要調整物件，表示要讓物件變大或較小。</span><span class="sxs-lookup"><span data-stu-id="1d357-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="1d357-106">您可以呼叫下列其中一種方法來調整物件。</span><span class="sxs-lookup"><span data-stu-id="1d357-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="1d357-107">**Matrix3x2F：： Scale (D2D1 \_ SIZE \_ F SCALEFACTOR，D2D1 \_ POINT \_ 2f centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="1d357-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="1d357-108">**Matrix3x2F：： Scale (float scalex、float scaley、D2D1 \_ POINT \_ 2f centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="1d357-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="1d357-109">第一個方法會將 *scalex* 和 *Scaley* 儲存為 [**D2D1 \_ 大小 \_ F**](/windows/desktop/Direct2D/d2d1-size-f) 結構中的已排序浮點數配對。</span><span class="sxs-lookup"><span data-stu-id="1d357-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="1d357-110">第二個方法會將 *scalex* 和 *scaley* 定義為個別參數。</span><span class="sxs-lookup"><span data-stu-id="1d357-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="1d357-111">無論您使用哪一種方法，您都必須同時指定 *scalex* 和 *scaley* 因數。</span><span class="sxs-lookup"><span data-stu-id="1d357-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="1d357-112">*Scalex* 值是 x 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="1d357-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="1d357-113">例如， *scalex* 值1.5 會沿著 X 軸將物件延伸至150%。</span><span class="sxs-lookup"><span data-stu-id="1d357-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="1d357-114">同樣地， *scaley* 值是 y 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="1d357-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="1d357-115">例如， *scaley* 值0.5 會將物件的高度縮減為 y 軸的50%。</span><span class="sxs-lookup"><span data-stu-id="1d357-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="1d357-116">若要將某個點指定為縮放作業的中心點，請使用 *centerpoint* 參數。</span><span class="sxs-lookup"><span data-stu-id="1d357-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="1d357-117">根據預設，物件會以其原點為中心 (0、0) 。</span><span class="sxs-lookup"><span data-stu-id="1d357-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="1d357-118">下列程式碼範例會建立縮放轉換，以將正方形的大小增加到其原始大小的130%。</span><span class="sxs-lookup"><span data-stu-id="1d357-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="1d357-119">*Centerpoint* 會設定為原始正方形的左上角。</span><span class="sxs-lookup"><span data-stu-id="1d357-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="1d357-120">下圖顯示將刻度轉換套用至正方形的效果。</span><span class="sxs-lookup"><span data-stu-id="1d357-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="1d357-121">原始正方形是虛線外框，而縮放的正方形是實心外框。</span><span class="sxs-lookup"><span data-stu-id="1d357-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![正方形的圖已調整大小為130% 的原始大小](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="1d357-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d357-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d357-124">Direct2D 轉換總覽</span><span class="sxs-lookup"><span data-stu-id="1d357-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="1d357-125">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="1d357-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 