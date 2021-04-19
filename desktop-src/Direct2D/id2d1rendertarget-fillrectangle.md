---
title: 'ID2D1RenderTarget Graphicswindow.fillrectangle 方法 (D2d1 \_ 1 .h) '
description: 繪製指定矩形的內部。
ms.assetid: 08e498f9-b564-4da6-ba9b-bff08964ce08
keywords:
- Graphicswindow.fillrectangle 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 21339e535aec294b3737f8a81ce313d524004bcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995194"
---
# <a name="id2d1rendertargetfillrectangle-methods"></a><span data-ttu-id="9bf1d-104">ID2D1RenderTarget：： Graphicswindow.fillrectangle 方法</span><span class="sxs-lookup"><span data-stu-id="9bf1d-104">ID2D1RenderTarget::FillRectangle methods</span></span>

<span data-ttu-id="9bf1d-105">繪製指定矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-105">Paints the interior of the specified rectangle.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9bf1d-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="9bf1d-106">Overload list</span></span>



| <span data-ttu-id="9bf1d-107">方法</span><span class="sxs-lookup"><span data-stu-id="9bf1d-107">Method</span></span>                                                                                                               | <span data-ttu-id="9bf1d-108">描述</span><span class="sxs-lookup"><span data-stu-id="9bf1d-108">Description</span></span>                                                 |
|:---------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="9bf1d-109">[**Graphicswindow.fillrectangle (D2D1 \_ RECT \_ F&、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="9bf1d-109">[**FillRectangle(D2D1\_RECT\_F&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span></span>  | <span data-ttu-id="9bf1d-110">繪製指定矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-110">Paints the interior of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="9bf1d-111">[**Graphicswindow.fillrectangle (D2D1 \_ RECT \_ F \* 、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="9bf1d-111">[**FillRectangle(D2D1\_RECT\_F\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span></span> | <span data-ttu-id="9bf1d-112">繪製指定矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-112">Paints the interior of the specified rectangle.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9bf1d-113">備註</span><span class="sxs-lookup"><span data-stu-id="9bf1d-113">Remarks</span></span>

<span data-ttu-id="9bf1d-114">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="9bf1d-115">若要判斷繪圖作業 (如 **graphicswindow.fillrectangle**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-115">To determine whether a drawing operation (such as **FillRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="9bf1d-116">範例</span><span class="sxs-lookup"><span data-stu-id="9bf1d-116">Examples</span></span>

<span data-ttu-id="9bf1d-117">下列範例會使用 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) 來繪製和填滿數個矩形。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-117">The following example uses an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) to draw and fill several rectangles.</span></span> <span data-ttu-id="9bf1d-118">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-118">This example produces the output shown in the following illustration.</span></span>

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



<span data-ttu-id="9bf1d-120">如需相關的教學課程，請參閱 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="9bf1d-120">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf1d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bf1d-121">Requirements</span></span>



| <span data-ttu-id="9bf1d-122">需求</span><span class="sxs-lookup"><span data-stu-id="9bf1d-122">Requirement</span></span> | <span data-ttu-id="9bf1d-123">值</span><span class="sxs-lookup"><span data-stu-id="9bf1d-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf1d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9bf1d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9bf1d-125"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="9bf1d-125"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="9bf1d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9bf1d-126">Library</span></span><br/> | <dl> <span data-ttu-id="9bf1d-127"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bf1d-127"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9bf1d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf1d-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bf1d-129"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf1d-129"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="9bf1d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bf1d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf1d-131">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="9bf1d-131">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="9bf1d-132">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="9bf1d-132">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

<span data-ttu-id="9bf1d-133">�</span><span class="sxs-lookup"><span data-stu-id="9bf1d-133">�</span></span>

<span data-ttu-id="9bf1d-134">�</span><span class="sxs-lookup"><span data-stu-id="9bf1d-134">�</span></span>
