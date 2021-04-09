---
title: 如何結合幾何
description: 說明如何使用 Direct2D 結合兩個幾何。
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8332421c62f49b60bb2186118ac7f741922fdc7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023802"
---
# <a name="how-to-combine-geometries"></a><span data-ttu-id="f092e-103">如何結合幾何</span><span class="sxs-lookup"><span data-stu-id="f092e-103">How to Combine Geometries</span></span>

<span data-ttu-id="f092e-104">本主題說明如何結合兩個幾何。</span><span class="sxs-lookup"><span data-stu-id="f092e-104">This topic describes how to combine two geometries.</span></span> <span data-ttu-id="f092e-105">Direct2D 支援四種結合幾何的模式： Union、Intersect、XOR 和 Exclude。</span><span class="sxs-lookup"><span data-stu-id="f092e-105">Direct2D supports four modes for combining geometries: Union, Intersect, XOR, and Exclude.</span></span> <span data-ttu-id="f092e-106">這些模式是以 [**D2D1 \_ 合併 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) 列舉類型來指定。</span><span class="sxs-lookup"><span data-stu-id="f092e-106">These modes are specified in the [**D2D1\_COMBINE\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) enum type.</span></span>

<span data-ttu-id="f092e-107">**使用四種模式的任一個來結合兩個幾何**</span><span class="sxs-lookup"><span data-stu-id="f092e-107">**To combine two geometries by using any of the four modes**</span></span>

1.  <span data-ttu-id="f092e-108">宣告路徑幾何： [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 類型的變數，其會儲存幾何組合的結果。</span><span class="sxs-lookup"><span data-stu-id="f092e-108">Declare a path geometry: a variable of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) that will store the result of geometry combination.</span></span>
2.  <span data-ttu-id="f092e-109">宣告幾何接收： [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) 類型的變數，其會儲存路徑幾何。</span><span class="sxs-lookup"><span data-stu-id="f092e-109">Declare a geometry sink: a variable of type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) that will store the path geometry.</span></span>
3.  <span data-ttu-id="f092e-110">藉由呼叫 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法來建立路徑幾何物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-110">Create the path geometry object by calling the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span>
4.  <span data-ttu-id="f092e-111">藉由呼叫 [**ID2D1PathGeometry：： open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法來開啟 geometry 接收器物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-111">Open the geometry sink object by calling the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>
5.  <span data-ttu-id="f092e-112">使用四種模式的其中一種，藉由呼叫 [**ID2D1EllipseGeometry：： CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) 方法來合併這兩個幾何。</span><span class="sxs-lookup"><span data-stu-id="f092e-112">Use one of the four modes to combine the two geometries by calling the [**ID2D1EllipseGeometry::CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) method.</span></span>
6.  <span data-ttu-id="f092e-113">關閉 geometry 接收器物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-113">Close the geometry sink object.</span></span>

<span data-ttu-id="f092e-114">下列程式碼會宣告 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 和 **ID2D1GeometrySink** 類型的變數。</span><span class="sxs-lookup"><span data-stu-id="f092e-114">The following code declares the variables of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and **ID2D1GeometrySink**.</span></span>


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



<span data-ttu-id="f092e-115">下列程式碼會使用四種模式的每一個來結合兩個 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) 物件，並執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="f092e-115">The following code uses each of the four modes to combine the two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and performs the following actions:</span></span>

-   <span data-ttu-id="f092e-116">建立兩個省略號： m \_ spEllipseGeometryOne 和 m \_ spEllipseGeometryTwo。</span><span class="sxs-lookup"><span data-stu-id="f092e-116">Creates two ellipses, m\_spEllipseGeometryOne and m\_spEllipseGeometryTwo.</span></span>
-   <span data-ttu-id="f092e-117">建立路徑幾何物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-117">Creates a path geometry object.</span></span>
-   <span data-ttu-id="f092e-118">開啟幾何接收物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-118">Opens a geometry sink object.</span></span>
-   <span data-ttu-id="f092e-119">結合兩個省略號。</span><span class="sxs-lookup"><span data-stu-id="f092e-119">Combines the two ellipses.</span></span>
-   <span data-ttu-id="f092e-120">關閉 geometry 接收器物件。</span><span class="sxs-lookup"><span data-stu-id="f092e-120">Closes the geometry sink object.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="f092e-121">此程式碼會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="f092e-121">This code produces the output shown in the following illustration.</span></span>

![兩個幾何的圖例，以及用來合併幾何 (聯集、交集、xor 和排除的四種模式) ](images/combine-modes.png)

## <a name="related-topics"></a><span data-ttu-id="f092e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="f092e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f092e-124">**D2D1 \_ 合併 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="f092e-124">**D2D1\_COMBINE\_MODE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[<span data-ttu-id="f092e-125">**ID2D1EllipseGeometry**</span><span class="sxs-lookup"><span data-stu-id="f092e-125">**ID2D1EllipseGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[<span data-ttu-id="f092e-126">**ID2D1PathGeometry**</span><span class="sxs-lookup"><span data-stu-id="f092e-126">**ID2D1PathGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

<span data-ttu-id="f092e-127">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="f092e-127">**ID2D1GeometrySink**</span></span>
</dt> </dl>

 

 