---
title: 如何裁剪成幾何遮罩
description: 顯示如何使用圖層來裁剪區域。
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463449"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="8f05c-103">如何裁剪成幾何遮罩</span><span class="sxs-lookup"><span data-stu-id="8f05c-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="8f05c-104">本主題說明如何使用幾何遮罩來裁剪圖層的區域。</span><span class="sxs-lookup"><span data-stu-id="8f05c-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="8f05c-105">**使用幾何遮罩來裁剪區域**</span><span class="sxs-lookup"><span data-stu-id="8f05c-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="8f05c-106">建立將用來裁剪區域的 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 。</span><span class="sxs-lookup"><span data-stu-id="8f05c-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="8f05c-107">呼叫 [**ID2D1RenderTarget：： CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 來建立圖層。</span><span class="sxs-lookup"><span data-stu-id="8f05c-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="8f05c-108">呼叫 [**ID2D1RenderTarget：:P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 並傳遞您在步驟1中定義的幾何遮罩。</span><span class="sxs-lookup"><span data-stu-id="8f05c-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="8f05c-109">將內容繪製至剪輯。</span><span class="sxs-lookup"><span data-stu-id="8f05c-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="8f05c-110">呼叫 [**ID2D1RenderTarget：:P oplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) ，將圖層從呈現目標中移除。</span><span class="sxs-lookup"><span data-stu-id="8f05c-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="8f05c-111">接下來的範例會使用幾何遮罩來裁剪影像和數個矩形。</span><span class="sxs-lookup"><span data-stu-id="8f05c-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="8f05c-112">下圖顯示左邊的原始點陣圖，以及裁剪至右側幾何遮罩的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8f05c-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![點陣圖裁剪成星形遮罩之前和之後的金魚點陣圖圖例](images/cliparegion-layers.png)

<span data-ttu-id="8f05c-114">若要裁剪繪圖（如上圖所示），您可以建立一個 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) ，並用它來定義星形。</span><span class="sxs-lookup"><span data-stu-id="8f05c-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="8f05c-115">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="8f05c-115">The following code shows how to do this.</span></span>


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



<span data-ttu-id="8f05c-116">呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 來建立圖層。</span><span class="sxs-lookup"><span data-stu-id="8f05c-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="8f05c-117">從 Windows 8 開始，您不需要呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))。</span><span class="sxs-lookup"><span data-stu-id="8f05c-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="8f05c-118">在大部分情況下，如果您未呼叫此方法，而 Direct2D 管理層資源，則效能會比較好。</span><span class="sxs-lookup"><span data-stu-id="8f05c-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="8f05c-119">使用幾何遮罩呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 來推送圖層。</span><span class="sxs-lookup"><span data-stu-id="8f05c-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="8f05c-120">將內容繪製到剪輯，然後呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 以彈出圖層。</span><span class="sxs-lookup"><span data-stu-id="8f05c-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="8f05c-121">這會產生星形繪圖。</span><span class="sxs-lookup"><span data-stu-id="8f05c-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="8f05c-122">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="8f05c-122">The following code shows how to do this.</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8f05c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f05c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f05c-124">圖層總覽</span><span class="sxs-lookup"><span data-stu-id="8f05c-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="8f05c-125">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="8f05c-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 