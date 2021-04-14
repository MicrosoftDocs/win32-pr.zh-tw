---
title: 如何套用2D 轉換
description: 本主題示範如何使用 Microsoft DirectComposition 將2D 轉換套用至視覺效果。
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- 如何套用 DirectComposition 2D 轉換
- DirectComposition 2D 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382453"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="3cb04-105">如何套用2D 轉換</span><span class="sxs-lookup"><span data-stu-id="3cb04-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="3cb04-106">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="3cb04-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3cb04-107">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="3cb04-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="3cb04-108">本主題示範如何使用 Microsoft DirectComposition 將2D 轉換套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3cb04-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="3cb04-109">本主題中的範例會套用一組轉換，這些轉換會：</span><span class="sxs-lookup"><span data-stu-id="3cb04-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="3cb04-110">依180度旋轉視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3cb04-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="3cb04-111">將視覺效果擴大至其原始大小的三倍。</span><span class="sxs-lookup"><span data-stu-id="3cb04-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="3cb04-112">轉譯 (將) 視覺效果150圖元移至其原始位置右邊。</span><span class="sxs-lookup"><span data-stu-id="3cb04-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="3cb04-113">下列螢幕擷取畫面顯示套用2D 轉換之前和之後的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3cb04-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![將2d 轉換群組套用至視覺效果的結果](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="3cb04-115">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="3cb04-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3cb04-116">技術</span><span class="sxs-lookup"><span data-stu-id="3cb04-116">Technologies</span></span>

-   [<span data-ttu-id="3cb04-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3cb04-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="3cb04-118">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="3cb04-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="3cb04-119">DirectX Graphic Infrastructure (DXGI) </span><span class="sxs-lookup"><span data-stu-id="3cb04-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="3cb04-120">必要條件</span><span class="sxs-lookup"><span data-stu-id="3cb04-120">Prerequisites</span></span>

-   <span data-ttu-id="3cb04-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="3cb04-121">C/C++</span></span>
-   <span data-ttu-id="3cb04-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="3cb04-122">Microsoft Win32</span></span>
-   <span data-ttu-id="3cb04-123">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="3cb04-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="3cb04-124">指示</span><span class="sxs-lookup"><span data-stu-id="3cb04-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="3cb04-125">步驟1：初始化 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="3cb04-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="3cb04-126">建立裝置物件和組合目標物件。</span><span class="sxs-lookup"><span data-stu-id="3cb04-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="3cb04-127">建立視覺效果、設定其內容，並將它新增至視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="3cb04-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="3cb04-128">如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。</span><span class="sxs-lookup"><span data-stu-id="3cb04-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="3cb04-129">步驟2：建立轉換群組陣列</span><span class="sxs-lookup"><span data-stu-id="3cb04-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="3cb04-130">步驟3：建立轉換物件、設定其屬性，並將其新增至轉換群組陣列</span><span class="sxs-lookup"><span data-stu-id="3cb04-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="3cb04-131">您可以使用 [**IDCompositionDevice：： CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform)、 [**：： CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)和 [**：： CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) 方法來建立轉換物件。</span><span class="sxs-lookup"><span data-stu-id="3cb04-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="3cb04-132">使用 [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)、 [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)和 [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) 介面的成員函式來設定轉換的屬性。</span><span class="sxs-lookup"><span data-stu-id="3cb04-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="3cb04-133">將轉換介面指標複製到轉換群組陣列。</span><span class="sxs-lookup"><span data-stu-id="3cb04-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="3cb04-134">步驟4：建立轉換群組物件</span><span class="sxs-lookup"><span data-stu-id="3cb04-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="3cb04-135">呼叫 [**IDCompositionDevice：： CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) 方法，以建立轉換群組物件。</span><span class="sxs-lookup"><span data-stu-id="3cb04-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="3cb04-136">步驟5：將轉換群組物件套用至視覺效果</span><span class="sxs-lookup"><span data-stu-id="3cb04-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="3cb04-137">您可以使用 [**IDCompositionVisual：： SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) 方法，將視覺效果的轉換屬性與轉換群組物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3cb04-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="3cb04-138">步驟6：認可組合</span><span class="sxs-lookup"><span data-stu-id="3cb04-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="3cb04-139">呼叫 [**IDCompositionDevice：： commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法，將視覺效果的更新認可至 DirectComposition 以進行處理。</span><span class="sxs-lookup"><span data-stu-id="3cb04-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="3cb04-140">套用2D 轉換群組的結果會出現在目標視窗中。</span><span class="sxs-lookup"><span data-stu-id="3cb04-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="3cb04-141">步驟7：釋放 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="3cb04-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="3cb04-142">當您不再需要2D 轉換物件時，請務必釋放2D 轉換物件的群組。</span><span class="sxs-lookup"><span data-stu-id="3cb04-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="3cb04-143">下列範例會呼叫應用程式定義的 [**SafeRelease**](/windows/desktop/medfound/saferelease) 宏來釋放轉換物件。</span><span class="sxs-lookup"><span data-stu-id="3cb04-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="3cb04-144">也請記得在應用程式結束之前釋出裝置物件、組合目標物件和視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3cb04-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="3cb04-145">完整範例</span><span class="sxs-lookup"><span data-stu-id="3cb04-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3cb04-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cb04-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb04-147">轉換</span><span class="sxs-lookup"><span data-stu-id="3cb04-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 