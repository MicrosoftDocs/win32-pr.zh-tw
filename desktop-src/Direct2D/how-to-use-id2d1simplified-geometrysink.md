---
title: 如何藉由擴充 ID2D1SimplifiedGeometrySink 來取出幾何資料
description: 顯示如何藉由擴充 ID2D1SimplifiedGeometrySink 介面來取出幾何資料。
ms.assetid: c6777b11-6d4e-409e-9c30-da1e060c9aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba3670eb8d0152cc1dae8fbcc164bd8a6167630
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023897"
---
# <a name="how-to-retrieve-geometry-data-by-extending-id2d1simplifiedgeometrysink"></a><span data-ttu-id="9006d-103">如何藉由擴充 ID2D1SimplifiedGeometrySink 來取出幾何資料</span><span class="sxs-lookup"><span data-stu-id="9006d-103">How to Retrieve Geometry Data by Extending ID2D1SimplifiedGeometrySink</span></span>

<span data-ttu-id="9006d-104">雖然 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件是不可變的，但在某些情況下，您需要在 path geometry 物件中操作幾何資料。</span><span class="sxs-lookup"><span data-stu-id="9006d-104">While an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object is immutable, there are cases where you need to manipulate the geometry data in a path geometry object.</span></span> <span data-ttu-id="9006d-105">Direct2D 可讓您藉由提供一個可延伸的介面（名為 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)）來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="9006d-105">Direct2D enables you to do so by providing an extendable interface named [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="9006d-106">在概念圖例中，本主題說明如何擴充這個介面，以從路徑幾何物件中取出幾何資料。</span><span class="sxs-lookup"><span data-stu-id="9006d-106">For concept illustration, this topic describes how to extend this interface to retrieve the geometry data from a path geometry object.</span></span>

<span data-ttu-id="9006d-107">**擴充 ID2D1SimplifiedGeometrySink 介面**</span><span class="sxs-lookup"><span data-stu-id="9006d-107">**To Extend the ID2D1SimplifiedGeometrySink interface**</span></span>

1.  <span data-ttu-id="9006d-108">執行繼承自 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)的類別。</span><span class="sxs-lookup"><span data-stu-id="9006d-108">Implement a class that inherits from [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span>
2.  <span data-ttu-id="9006d-109">建立該類別的實例，並將它傳遞給 [**ID2D1Geometry：：簡化**](id2d1geometry-simplify.md)。</span><span class="sxs-lookup"><span data-stu-id="9006d-109">Create an instance of that class and pass it to [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md).</span></span>

<span data-ttu-id="9006d-110">下列程式碼範例示範如何執行繼承自 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) 介面之名為 SpecializedSink 的類別。</span><span class="sxs-lookup"><span data-stu-id="9006d-110">The following code example shows how to implement a class named SpecializedSink that inherits from the [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) interface.</span></span> <span data-ttu-id="9006d-111">為了簡單起見概念圖例，擴充 **AddLines** 方法會抓取幾何資料，然後在主控台視窗中顯示該資料。您可以自訂此方法，以符合您的特定資料需求。</span><span class="sxs-lookup"><span data-stu-id="9006d-111">For the simplicity of concept illustration, the extended **AddLines** method retrieves the geometry data and then displays it on the console window; you can customize this method to meet your specific data needs.</span></span>


```C++
class SpecializedSink : public ID2D1SimplifiedGeometrySink
{
    public:
        SpecializedSink()
            : m_cRef(1)
        {
        }

        STDMETHOD_(ULONG, AddRef)(THIS)
        {
            return InterlockedIncrement(reinterpret_cast<LONG volatile *>(&m_cRef));
        }

        STDMETHOD_(ULONG, Release)(THIS)
        {
            ULONG cRef = static_cast<ULONG>(
            InterlockedDecrement(reinterpret_cast<LONG volatile *>(&m_cRef)));

            if(0 == cRef)
            {
                delete this;
            }

            return cRef;
        }

        STDMETHOD(QueryInterface)(THIS_ REFIID iid, void** ppvObject)
        {
            HRESULT hr = S_OK;

            if (__uuidof(IUnknown) == iid)
            {
                *ppvObject = static_cast<IUnknown*>(this);
                AddRef();
            }
            else if (__uuidof(ID2D1SimplifiedGeometrySink) == iid)
            {
                *ppvObject = static_cast<ID2D1SimplifiedGeometrySink*>(this);
                AddRef();
            }
            else
            {
                *ppvObject = NULL;
                hr = E_NOINTERFACE;
            }

            return hr;
        }

        STDMETHOD_(void, AddBeziers)(const D2D1_BEZIER_SEGMENT * /*beziers*/,
                                     UINT /*beziersCount*/)
        {
            // Customize this method to meet your specific data needs.
        }

        STDMETHOD_(void, AddLines)(const D2D1_POINT_2F *points, UINT pointsCount)
        {
            // Customize this method to meet your specific data needs.
            printf("\n\nRetrieving geometry data from a derived ID2D1SimplifiedGeometrySink object:\n");
            for (UINT i = 0; i < pointsCount; ++i)
            {
                printf("%.0f, %.0f\n", points[i].x, points[i].y);
            }
        }

        STDMETHOD_(void, BeginFigure)(D2D1_POINT_2F startPoint,
                                      D2D1_FIGURE_BEGIN figureBegin)
        {
        }

        STDMETHOD_(void, EndFigure)(D2D1_FIGURE_END figureEnd)
        {
        }

        STDMETHOD_(void, SetFillMode)(D2D1_FILL_MODE fillMode)
        {
        }

        STDMETHOD_(void, SetSegmentFlags)(D2D1_PATH_SEGMENT vertexFlags)
        {
        }

        STDMETHOD(Close)()
        {
            return S_OK;
        }

    private:
        UINT m_cRef;
};
```



<span data-ttu-id="9006d-112">然後，此範例會使用一組資料 (182、209) 、 (211、251) 、 (251、226) 、 (392、360) 和 (101、360) 和 (、) 建立已填入的路徑幾何 **m \_ pGeometry** 可從中抓取資料。</span><span class="sxs-lookup"><span data-stu-id="9006d-112">The example then uses a set of data (182, 209), (211, 251), (251, 226), (392, 360), and (101, 360) to create a populated path geometry (**m\_pGeometry**) where data can be retrieved.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pGeometry);
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;

    hr = m_pGeometry->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

        pSink->BeginFigure(
            D2D1::Point2F(101,360),
            D2D1_FIGURE_BEGIN_FILLED
            );
        D2D1_POINT_2F points[5] = {
           D2D1::Point2F(182,209),
           D2D1::Point2F(211,251),
           D2D1::Point2F(251,226),
           D2D1::Point2F(392,360),
           D2D1::Point2F(101,360),
           };

        printf("Adding the following geometry data to an ID2D1GeometrySink object:\n");
        printf("182, 209\n");
        printf("211, 251\n");
        printf("251, 226\n");
        printf("392, 360\n");
        printf("101, 360\n");

        pSink->AddLines(points, ARRAYSIZE(points));
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
        pSink->Release();
```



<span data-ttu-id="9006d-113">最後，此範例會建立 SpecializedSink 物件，然後呼叫 [**ID2D1Geometry：：簡化**](id2d1geometry-simplify.md) 方法，傳入 SpecializedSink 物件和 [**D2D1 \_ 幾何 \_ 簡化 \_ 選項 \_ 行**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) 參數，以將任何曲線壓平合併成線段。</span><span class="sxs-lookup"><span data-stu-id="9006d-113">Finally, the example creates a SpecializedSink object, and then calls the [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md) method, passing in the SpecializedSink object and the [**D2D1\_GEOMETRY\_SIMPLIFICATION\_OPTION\_LINES**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) parameter, which causes any curves to be flattened into line segments.</span></span>


```C++
        SpecializedSink *pSpecializedSink = NULL;

        if (SUCCEEDED(hr))
        {
            pSpecializedSink = new SpecializedSink();
            if (!pSpecializedSink)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        if (SUCCEEDED(hr))
        {
            hr = m_pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, // This causes any curves to be flattened into line segments.
                    NULL, // world transform
                    pSpecializedSink
                    );


            if (SUCCEEDED(hr))
            {
                hr = pSpecializedSink->Close();
            }

            pSpecializedSink->Release();
        }
```



<span data-ttu-id="9006d-114">程式會建立輸出，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="9006d-114">The program creates outputs as shown in the following screen shot.</span></span>

![主控台視窗的螢幕擷取畫面，其中包含有關新增和取出幾何資料的輸出](images/specializedgeometrysink.png)

## <a name="related-topics"></a><span data-ttu-id="9006d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9006d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9006d-117">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="9006d-117">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 