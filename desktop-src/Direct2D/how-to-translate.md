---
title: 如何轉譯物件
description: 顯示如何轉譯物件。
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316087"
---
# <a name="how-to-translate-an-object"></a><span data-ttu-id="37a59-103">如何轉譯物件</span><span class="sxs-lookup"><span data-stu-id="37a59-103">How to Translate an Object</span></span>

<span data-ttu-id="37a59-104">若要轉譯2D 物件，請沿著 X 軸、y 軸或兩者移動物件。</span><span class="sxs-lookup"><span data-stu-id="37a59-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="37a59-105">您可以呼叫下列其中一種方法來建立轉譯轉換。</span><span class="sxs-lookup"><span data-stu-id="37a59-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="37a59-106">[**轉譯 (D2D1 \_大小： \_ F 大小)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))：採用已排序的配對，定義沿著 X 軸和 y 軸平移的距離。</span><span class="sxs-lookup"><span data-stu-id="37a59-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="37a59-107">[**轉譯 (float x，float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float))：採用沿著 X 軸平移的距離，以及沿著 y 軸平移的距離。</span><span class="sxs-lookup"><span data-stu-id="37a59-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="37a59-108">下列程式碼會建立轉譯轉換矩陣，沿著 X 軸將正方形20單位向右移動，沿著 y 軸向下移動10個單位。</span><span class="sxs-lookup"><span data-stu-id="37a59-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="37a59-109">下圖顯示將轉譯轉換套用至正方形的效果，其中原始正方形是虛線外框，而轉譯的正方形是實心外框。</span><span class="sxs-lookup"><span data-stu-id="37a59-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![正方形的圖例將沿著 X 軸向右移動20個單位，並沿著 y 軸向下移動10個單位](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="37a59-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="37a59-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a59-112">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="37a59-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="37a59-113">Direct2D 轉換總覽</span><span class="sxs-lookup"><span data-stu-id="37a59-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 