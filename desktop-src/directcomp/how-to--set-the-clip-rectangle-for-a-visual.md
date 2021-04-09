---
title: 如何使用矩形剪輯物件裁剪
description: 本主題將示範如何使用矩形剪輯物件來裁剪視覺效果或視覺化樹狀結構。
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024306"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="d2208-103">如何使用矩形剪輯物件裁剪</span><span class="sxs-lookup"><span data-stu-id="d2208-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="d2208-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="d2208-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="d2208-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="d2208-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="d2208-106">本主題將示範如何使用矩形剪輯物件來裁剪視覺效果或視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="d2208-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="d2208-107">本主題中的範例會定義以滑鼠位置為中心的矩形剪輯，並將剪輯套用至在組合目標視窗的工作區中央的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="d2208-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="d2208-108">這個螢幕擷取畫面顯示將矩形剪輯物件套用至視覺效果的結果。</span><span class="sxs-lookup"><span data-stu-id="d2208-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![將矩形剪輯物件套用至視覺效果的結果](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2208-110">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d2208-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2208-111">技術</span><span class="sxs-lookup"><span data-stu-id="d2208-111">Technologies</span></span>

-   [<span data-ttu-id="d2208-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d2208-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="d2208-113">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="d2208-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="d2208-114">DirectX Graphic Infrastructure (DXGI) </span><span class="sxs-lookup"><span data-stu-id="d2208-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="d2208-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="d2208-115">Prerequisites</span></span>

-   <span data-ttu-id="d2208-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2208-116">C/C++</span></span>
-   <span data-ttu-id="d2208-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="d2208-117">Microsoft Win32</span></span>
-   <span data-ttu-id="d2208-118">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="d2208-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="d2208-119">指示</span><span class="sxs-lookup"><span data-stu-id="d2208-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="d2208-120">步驟1：初始化 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="d2208-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="d2208-121">建立裝置物件和組合目標物件。</span><span class="sxs-lookup"><span data-stu-id="d2208-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="d2208-122">建立視覺效果、設定其內容，並將它新增至視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="d2208-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="d2208-123">如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。</span><span class="sxs-lookup"><span data-stu-id="d2208-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="d2208-124">步驟2：建立矩形剪輯物件</span><span class="sxs-lookup"><span data-stu-id="d2208-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="d2208-125">您可以使用 [**IDCompositionDevice：： CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) 方法來建立矩形剪輯物件的實例。</span><span class="sxs-lookup"><span data-stu-id="d2208-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="d2208-126">步驟3：設定矩形剪輯物件的屬性</span><span class="sxs-lookup"><span data-stu-id="d2208-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="d2208-127">呼叫矩形剪輯物件之 [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面的方法，以設定剪切矩形的屬性。</span><span class="sxs-lookup"><span data-stu-id="d2208-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="d2208-128">下列範例會定義以目前滑鼠位置為中心的剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d2208-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="d2208-129">`m_offsetX`和 `m_offsetY` 成員變數包含視覺效果的 OffsetX 和 OffsetY 屬性值。</span><span class="sxs-lookup"><span data-stu-id="d2208-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



<span data-ttu-id="d2208-130">請注意， [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面包含下列方法，以定義具有圓角的剪輯矩形：</span><span class="sxs-lookup"><span data-stu-id="d2208-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="d2208-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="d2208-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="d2208-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="d2208-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="d2208-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="d2208-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="d2208-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="d2208-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="d2208-135">步驟4：設定視覺效果的剪輯屬性</span><span class="sxs-lookup"><span data-stu-id="d2208-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="d2208-136">使用 [**IDCompositionVisual：： SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) 方法，將視覺效果的剪輯屬性與矩形剪輯物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d2208-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="d2208-137">步驟5：認可組合</span><span class="sxs-lookup"><span data-stu-id="d2208-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="d2208-138">呼叫 [**IDCompositionDevice：： commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法，將命令批次認可至 Microsoft DirectComposition 進行處理。</span><span class="sxs-lookup"><span data-stu-id="d2208-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="d2208-139">套用剪輯矩形的結果會出現在目標視窗中。</span><span class="sxs-lookup"><span data-stu-id="d2208-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="d2208-140">步驟6：釋放 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="d2208-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="d2208-141">當您不再需要時，請務必釋放矩形剪輯物件，以及裝置物件、組合目標物件和任何視覺物件。</span><span class="sxs-lookup"><span data-stu-id="d2208-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="d2208-142">下列範例會呼叫應用程式定義的 [**SafeRelease**](/windows/desktop/medfound/saferelease) 宏來釋放 DirectComposition 物件。</span><span class="sxs-lookup"><span data-stu-id="d2208-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="d2208-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2208-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2208-144">裁剪</span><span class="sxs-lookup"><span data-stu-id="d2208-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 