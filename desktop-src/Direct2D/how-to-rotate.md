---
title: 如何旋轉物件
description: 顯示如何旋轉物件。
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933436"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="027bb-103">如何旋轉物件</span><span class="sxs-lookup"><span data-stu-id="027bb-103">How to Rotate an Object</span></span>

<span data-ttu-id="027bb-104">本主題說明如何旋轉物件的相關指定點。</span><span class="sxs-lookup"><span data-stu-id="027bb-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="027bb-105">若要旋轉物件，請呼叫 [**Matrix3x2F：：輪替**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) 方法。</span><span class="sxs-lookup"><span data-stu-id="027bb-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="027bb-106">這個方法會採用兩個參數：指定的角度和中心點。</span><span class="sxs-lookup"><span data-stu-id="027bb-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="027bb-107">角度是順時針旋轉角度（以度為單位），而中心點是物件旋轉的點。</span><span class="sxs-lookup"><span data-stu-id="027bb-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="027bb-108">中心點會以轉換之物件的座標系統表示。</span><span class="sxs-lookup"><span data-stu-id="027bb-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="027bb-109">例如，下列程式碼會在正方形的中央旋轉大約45度的正方形。</span><span class="sxs-lookup"><span data-stu-id="027bb-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="027bb-110">下圖顯示將上述旋轉轉換套用至正方形的效果。</span><span class="sxs-lookup"><span data-stu-id="027bb-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="027bb-111">原始正方形是虛線外框，而旋轉的正方形是實心的外框。</span><span class="sxs-lookup"><span data-stu-id="027bb-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![正方形的圖，與原始正方形的中心旋轉45度](images/rotate-ovw.png)

<span data-ttu-id="027bb-113">下圖顯示與不同中心點的相同角度旋轉的效果。</span><span class="sxs-lookup"><span data-stu-id="027bb-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="027bb-114">請注意，旋轉的物件位於相對於原始位置的不同位置。</span><span class="sxs-lookup"><span data-stu-id="027bb-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="027bb-115">左邊的正方形是圍繞原始正方形的中心旋轉的結果，右邊的方塊則是圍繞原始方形左上角旋轉的結果。</span><span class="sxs-lookup"><span data-stu-id="027bb-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![有關不同中心點的正方形順時針旋轉45度的圖例](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="027bb-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="027bb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027bb-118">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="027bb-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="027bb-119">Direct2D 轉換總覽</span><span class="sxs-lookup"><span data-stu-id="027bb-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 