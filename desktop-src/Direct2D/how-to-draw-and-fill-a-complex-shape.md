---
title: 如何繪製和填滿複雜的圖形
description: Direct2D 提供 ID2D1PathGeometry 介面，可用來描述可包含曲線、弧形和線條的複雜圖形。 本主題說明如何定義和轉譯路徑幾何。
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a163e85d76a65f6b807ad1e4a9c9f740a32bf1
ms.sourcegitcommit: 4859402a45b9928c3e1354ded06b1d6a682a0be9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/30/2021
ms.locfileid: "106991069"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a><span data-ttu-id="65d8d-104">如何繪製和填滿複雜的圖形</span><span class="sxs-lookup"><span data-stu-id="65d8d-104">How to Draw and Fill a Complex Shape</span></span>

<span data-ttu-id="65d8d-105">Direct2D 提供 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 介面，可用來描述可包含曲線、弧形和線條的複雜圖形。</span><span class="sxs-lookup"><span data-stu-id="65d8d-105">Direct2D provides the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface for describing complex shapes that can contain curves, arcs, and lines.</span></span> <span data-ttu-id="65d8d-106">本主題說明如何定義和轉譯路徑幾何。</span><span class="sxs-lookup"><span data-stu-id="65d8d-106">This topic describes how to define and render a path geometry.</span></span>

<span data-ttu-id="65d8d-107">若要定義路徑幾何，請先使用 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法來建立路徑幾何，然後使用路徑幾何的 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法來取得 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)。</span><span class="sxs-lookup"><span data-stu-id="65d8d-107">To define a path geometry, first use the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create the path geometry, then use the path geometry's [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="65d8d-108">然後，您可以藉由呼叫接收器的各種新增方法來新增線條、曲線和弧形。</span><span class="sxs-lookup"><span data-stu-id="65d8d-108">You can then add lines, curves, and arcs by calling the sink's various Add methods.</span></span>

<span data-ttu-id="65d8d-109">下列範例會建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)、抓取接收器，並用它來定義沙漏圖形。</span><span class="sxs-lookup"><span data-stu-id="65d8d-109">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;

// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```

<span data-ttu-id="65d8d-110">請注意， [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 是與裝置無關的資源，因此可以建立一次，並保留在應用程式的存留期內。</span><span class="sxs-lookup"><span data-stu-id="65d8d-110">Note that an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) is a device-independent resource and can, therefore, be created once and retained for the life of the application.</span></span> <span data-ttu-id="65d8d-111"> (如需有關不同資源類型的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="65d8d-111">(For more information about different types of resources, see the [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="65d8d-112">下一個範例會建立兩筆筆刷，用來繪製路徑幾何的輪廓和填滿。</span><span class="sxs-lookup"><span data-stu-id="65d8d-112">The next example creates two brushes that will be used to paint the path geometry's outline and fill.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



<span data-ttu-id="65d8d-113">最後一個範例會使用 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法來繪製幾何的輪廓和內部。</span><span class="sxs-lookup"><span data-stu-id="65d8d-113">The final example uses the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods to paint the geometry's outline and interior.</span></span> <span data-ttu-id="65d8d-114">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="65d8d-114">This example produces the output shown in the following illustration.</span></span>

![沙漏狀幾何的圖例](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

<span data-ttu-id="65d8d-116">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="65d8d-116">Code has been omitted from this example.</span></span> <span data-ttu-id="65d8d-117">如需幾何的詳細資訊，請參閱 [幾何總覽](direct2d-geometries-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="65d8d-117">For more information about geometries, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>
