---
title: 'D2D1_RECT_F (D2DBaseTypes) '
description: '代表由左上角座標所定義的矩形， (左、上) 和右下角的座標 (右邊、下) 。 |D2D1_RECT_F (D2DBaseTypes) '
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035254"
---
# <a name="d2d1_rect_f"></a><span data-ttu-id="bb53f-105">D2D1 \_ RECT \_ F</span><span class="sxs-lookup"><span data-stu-id="bb53f-105">D2D1\_RECT\_F</span></span>

<span data-ttu-id="bb53f-106">代表由左上角座標所定義的矩形， (左、上) 和右下角的座標 (右邊、下) 。</span><span class="sxs-lookup"><span data-stu-id="bb53f-106">Represents a rectangle defined by the coordinates of the upper-left corner (left, top) and the coordinates of the lower-right corner (right, bottom).</span></span>


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a><span data-ttu-id="bb53f-107">備註</span><span class="sxs-lookup"><span data-stu-id="bb53f-107">Remarks</span></span>

<span data-ttu-id="bb53f-108">**D2D1 \_RECT \_ f** 是已定義之 [**D2D \_ RECT \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) 結構的新名稱。</span><span class="sxs-lookup"><span data-stu-id="bb53f-108">**D2D1\_RECT\_F** is a new name for the already defined [**D2D\_RECT\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) struct.</span></span>

## <a name="examples"></a><span data-ttu-id="bb53f-109">範例</span><span class="sxs-lookup"><span data-stu-id="bb53f-109">Examples</span></span>

<span data-ttu-id="bb53f-110">下列範例會使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 來繪製和填滿數個矩形。</span><span class="sxs-lookup"><span data-stu-id="bb53f-110">The following example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw and fill several rectangles.</span></span> <span data-ttu-id="bb53f-111">此範例會產生如下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="bb53f-111">This example produces output as shown in the following illustration.</span></span>

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
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

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



<span data-ttu-id="bb53f-113">如需相關的教學課程，請參閱 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="bb53f-113">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb53f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb53f-114">Requirements</span></span>



| <span data-ttu-id="bb53f-115">需求</span><span class="sxs-lookup"><span data-stu-id="bb53f-115">Requirement</span></span> | <span data-ttu-id="bb53f-116">值</span><span class="sxs-lookup"><span data-stu-id="bb53f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb53f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb53f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb53f-118">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="bb53f-118">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bb53f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb53f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb53f-120">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb53f-120">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bb53f-121">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="bb53f-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bb53f-122">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb53f-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="bb53f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="bb53f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb53f-124"><dt>D2DBaseTypes (包含 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="bb53f-124"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bb53f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb53f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb53f-126">**D2D \_ RECT \_ F**</span><span class="sxs-lookup"><span data-stu-id="bb53f-126">**D2D\_RECT\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[<span data-ttu-id="bb53f-127">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="bb53f-127">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

