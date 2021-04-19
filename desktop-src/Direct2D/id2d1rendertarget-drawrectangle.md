---
title: 'ID2D1RenderTarget Graphicswindow.drawrectangle 方法 (D2d1 \_ 1 .h) '
description: 繪製具有指定維度和筆觸樣式之矩形的外框。
ms.assetid: 3f8c0754-fa68-4b5b-812f-24d8b544ba6e
keywords:
- Graphicswindow.drawrectangle 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4c1f846ca0bc1ddcb52696667edcb87291ae05df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990514"
---
# <a name="id2d1rendertargetdrawrectangle-methods"></a><span data-ttu-id="f8d51-104">ID2D1RenderTarget：:D rawRectangle 方法</span><span class="sxs-lookup"><span data-stu-id="f8d51-104">ID2D1RenderTarget::DrawRectangle methods</span></span>

<span data-ttu-id="f8d51-105">繪製具有指定維度和筆觸樣式之矩形的外框。</span><span class="sxs-lookup"><span data-stu-id="f8d51-105">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f8d51-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="f8d51-106">Overload list</span></span>



| <span data-ttu-id="f8d51-107">方法</span><span class="sxs-lookup"><span data-stu-id="f8d51-107">Method</span></span>                                                                                                                                                                   | <span data-ttu-id="f8d51-108">描述</span><span class="sxs-lookup"><span data-stu-id="f8d51-108">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d51-109">[**Graphicswindow.drawrectangle (D2D1 \_ RECT \_ F&、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="f8d51-109">[**DrawRectangle(D2D1\_RECT\_F&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="f8d51-110">繪製具有指定維度和筆觸樣式之矩形的外框。</span><span class="sxs-lookup"><span data-stu-id="f8d51-110">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span> <br/> |
| <span data-ttu-id="f8d51-111">[**Graphicswindow.drawrectangle (D2D1 \_ RECT \_ F \* 、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="f8d51-111">[**DrawRectangle(D2D1\_RECT\_F\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="f8d51-112">繪製具有指定維度和筆觸樣式之矩形的外框。</span><span class="sxs-lookup"><span data-stu-id="f8d51-112">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="f8d51-113">備註</span><span class="sxs-lookup"><span data-stu-id="f8d51-113">Remarks</span></span>

<span data-ttu-id="f8d51-114">當此方法失敗時，它不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f8d51-114">When this method fails, it does not return an error code.</span></span> <span data-ttu-id="f8d51-115">若要判斷繪圖方法 (如 **graphicswindow.drawrectangle**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="f8d51-115">To determine whether a drawing method (such as **DrawRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f8d51-116">範例</span><span class="sxs-lookup"><span data-stu-id="f8d51-116">Examples</span></span>

<span data-ttu-id="f8d51-117">下列範例會使用 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) 來繪製和填滿數個矩形。</span><span class="sxs-lookup"><span data-stu-id="f8d51-117">The following example uses an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) to draw and fill several rectangles.</span></span> <span data-ttu-id="f8d51-118">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="f8d51-118">This example produces the output shown in the following illustration.</span></span>

![格線背景上兩個矩形的圖例](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="f8d51-120">如需相關的教學課程，請參閱 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="f8d51-120">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d51-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8d51-121">Requirements</span></span>



| <span data-ttu-id="f8d51-122">需求</span><span class="sxs-lookup"><span data-stu-id="f8d51-122">Requirement</span></span> | <span data-ttu-id="f8d51-123">值</span><span class="sxs-lookup"><span data-stu-id="f8d51-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d51-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f8d51-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f8d51-125"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="f8d51-125"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8d51-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8d51-126">Library</span></span><br/> | <dl> <span data-ttu-id="f8d51-127"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8d51-127"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f8d51-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f8d51-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8d51-129"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8d51-129"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="f8d51-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8d51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d51-131">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="f8d51-131">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="f8d51-132">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="f8d51-132">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="f8d51-133">如何繪製和填滿基本圖形</span><span class="sxs-lookup"><span data-stu-id="f8d51-133">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="f8d51-134">�</span><span class="sxs-lookup"><span data-stu-id="f8d51-134">�</span></span>

<span data-ttu-id="f8d51-135">�</span><span class="sxs-lookup"><span data-stu-id="f8d51-135">�</span></span>
