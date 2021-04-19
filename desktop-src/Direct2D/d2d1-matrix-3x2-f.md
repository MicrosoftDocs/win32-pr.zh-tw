---
title: 'D2D1_MATRIX_3X2_F (D2d1) '
description: 表示 3 x 2 矩陣。
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969151"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="5ea54-104">D2D1 \_ 矩陣 \_ 3X2 \_ F</span><span class="sxs-lookup"><span data-stu-id="5ea54-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="5ea54-105">表示 3 x 2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="5ea54-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="5ea54-106">備註</span><span class="sxs-lookup"><span data-stu-id="5ea54-106">Remarks</span></span>

<span data-ttu-id="5ea54-107">**D2D1 \_矩陣 \_ 3X2** 是 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構的新名稱。</span><span class="sxs-lookup"><span data-stu-id="5ea54-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="5ea54-108">如需矩陣所提供的欄位清單，請參閱 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)。</span><span class="sxs-lookup"><span data-stu-id="5ea54-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="5ea54-109">為了簡化常見的矩陣作業，Direct2D 會提供 [**D2D1：： Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別，這是衍生自 [**D2D1 \_ 矩陣 \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構的類別。</span><span class="sxs-lookup"><span data-stu-id="5ea54-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="5ea54-110">**Matrix3x2F** 類別提供一組 helper 方法來執行一般工作，例如建立平移或扭曲矩陣。</span><span class="sxs-lookup"><span data-stu-id="5ea54-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="5ea54-111">範例</span><span class="sxs-lookup"><span data-stu-id="5ea54-111">Examples</span></span>

<span data-ttu-id="5ea54-112">下列範例會使用 [**D2D1：： Matrix3x2F：：輪替**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)方法來建立旋轉矩陣，以旋轉正方形中央的正方形45度，然後將矩陣傳遞給轉譯目標 (*m \_ pRenderTarget*) 的 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))方法。</span><span class="sxs-lookup"><span data-stu-id="5ea54-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="5ea54-113">下圖顯示將上述旋轉轉換套用至正方形的效果。</span><span class="sxs-lookup"><span data-stu-id="5ea54-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="5ea54-114">原始正方形是虛線外框，而旋轉的正方形是實心的外框。</span><span class="sxs-lookup"><span data-stu-id="5ea54-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![正方形的圖，與原始正方形的中心旋轉45度](images/rotate-ovw.png)


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



<span data-ttu-id="5ea54-116">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="5ea54-116">Code has been omitted from this example.</span></span> <span data-ttu-id="5ea54-117">如需轉換的詳細資訊，請參閱 [轉換總覽](direct2d-transforms-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5ea54-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea54-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ea54-118">Requirements</span></span>



| <span data-ttu-id="5ea54-119">需求</span><span class="sxs-lookup"><span data-stu-id="5ea54-119">Requirement</span></span> | <span data-ttu-id="5ea54-120">值</span><span class="sxs-lookup"><span data-stu-id="5ea54-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea54-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ea54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea54-122">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="5ea54-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5ea54-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ea54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea54-124">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ea54-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5ea54-125">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="5ea54-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5ea54-126">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ea54-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="5ea54-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5ea54-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea54-128"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea54-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="5ea54-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ea54-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea54-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="5ea54-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="5ea54-131">轉換總覽</span><span class="sxs-lookup"><span data-stu-id="5ea54-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="5ea54-132">如何旋轉物件</span><span class="sxs-lookup"><span data-stu-id="5ea54-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="5ea54-133">如何調整物件</span><span class="sxs-lookup"><span data-stu-id="5ea54-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="5ea54-134">如何扭曲物件</span><span class="sxs-lookup"><span data-stu-id="5ea54-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="5ea54-135">如何轉譯物件</span><span class="sxs-lookup"><span data-stu-id="5ea54-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="5ea54-136">**D2D \_ 矩陣 \_ 3X2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="5ea54-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

