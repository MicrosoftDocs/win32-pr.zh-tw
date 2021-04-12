---
title: 如何建立 Geometry 群組
description: 本主題說明如何建立 geometry 群組。
ms.assetid: be364440-75ab-4d8f-a359-39da275272fd
keywords:
- Direct2D、fill 模式範例
- geometry 群組
- Direct2D，geometry 群組
- 路徑幾何
- Direct2D，路徑幾何
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb4a0e63a3274473153e1871a8a085bb04d5146
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375521"
---
# <a name="how-to-create-geometry-groups"></a><span data-ttu-id="27904-108">如何建立 Geometry 群組</span><span class="sxs-lookup"><span data-stu-id="27904-108">How to Create Geometry Groups</span></span>

<span data-ttu-id="27904-109">本主題說明如何建立 geometry 群組。</span><span class="sxs-lookup"><span data-stu-id="27904-109">This topic describes how to create geometry groups.</span></span>

<span data-ttu-id="27904-110">若要建立 geometry 群組，請呼叫 [**ID2D1Factory：： CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) 方法，並指定幾何的陣列和填滿模式。</span><span class="sxs-lookup"><span data-stu-id="27904-110">To create a geometry group, call the [**ID2D1Factory::CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method and specify an array of geometries and a fill mode.</span></span>

<span data-ttu-id="27904-111">當您將幾何合併至 geometry 群組時，請確定幾何的方向類似。</span><span class="sxs-lookup"><span data-stu-id="27904-111">When you combine geometries into a geometry group, ensure that the geometries are similarly oriented.</span></span> <span data-ttu-id="27904-112">如果您不確定幾何的方向，請在每個專案上個別呼叫 [**ID2D1Geometry：：大綱**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) ，然後將產生的幾何插入 geometry 群組中。</span><span class="sxs-lookup"><span data-stu-id="27904-112">If you are unsure of the orientation of the geometries, call [**ID2D1Geometry::Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) on each of them individually, and then insert the resulting geometries into the geometry group.</span></span>

<span data-ttu-id="27904-113">下列程式碼範例示範如何建立四個同心圓：第一個圓形的半徑為25、第二個50、第三個75和第四個100。</span><span class="sxs-lookup"><span data-stu-id="27904-113">The following code example shows the creation of four concentric circles: the first circle has a radius of 25, the second 50, the third 75, and the fourth 100.</span></span> <span data-ttu-id="27904-114">程式碼也會顯示幾何陣列的具現化，以及兩個 [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup)呼叫。</span><span class="sxs-lookup"><span data-stu-id="27904-114">The code also shows the instantiation of an array of geometries, as well as the two calls to [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup).</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}
```



## <a name="drawing-and-filling-of-geometry-groups"></a><span data-ttu-id="27904-115">繪製和填滿幾何群組</span><span class="sxs-lookup"><span data-stu-id="27904-115">Drawing and Filling of Geometry Groups</span></span>

<span data-ttu-id="27904-116">若要繪製和填滿幾何群組，請使用 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 和 [**ID2D1RenderTarget：:D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="27904-116">To draw and fill a geometry group, use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) and [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) methods.</span></span> <span data-ttu-id="27904-117">下列程式碼範例顯示如何繪製和填滿幾何群組。</span><span class="sxs-lookup"><span data-stu-id="27904-117">The following code example shows how to draw and fill a geometry group.</span></span>


```C++
HRESULT DemoApp::OnRender()
{
    HRESULT hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_fillModeAlternateText[] = L"D2D1_FILL_MODE_ALTERNATE";
        static const WCHAR sc_fillModeWindingText[] = L"D2D1_FILL_MODE_WINDING";

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, rtSize.width, rtSize.height),
            m_pGridPatternBitmapBrush
            );

        // Centers the text in a layout rectangle.
        hr = m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        if (SUCCEEDED(hr))
        {
            // Fill the geometry group with D2D1_FILL_MODE_ALTERNATE and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_AlternateFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_AlternateFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeAlternateText,
                ARRAYSIZE(sc_fillModeAlternateText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

            // Fill the geometry group with D2D1_FILL_MODE_WINDING and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_WindingFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_WindingFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeWindingText,
                ARRAYSIZE(sc_fillModeWindingText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            hr = m_pRenderTarget->EndDraw();

            if (hr == D2DERR_RECREATE_TARGET)
            {
                hr = S_OK;
                DiscardDeviceResources();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="27904-118">程式碼會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="27904-118">The code produces the output shown in the following illustration.</span></span>

![四個同心圓的圖，其中一組已填滿第二個和第四個環形，另一個則填滿所有環形](images/create-geometry-group.png)

 

 