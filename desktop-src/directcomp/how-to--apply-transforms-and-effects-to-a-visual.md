---
title: 如何套用效果
description: 本主題將示範如何使用 Microsoft DirectComposition 將效果和3D 轉換套用至視覺效果。
ms.assetid: FE5A0BE9-B84C-4DE1-85D8-375897237F96
keywords:
- 如何套用 DirectComposition 效果
- DirectComposition 效果，如何申請
- DirectComposition 3D 轉換
- DirectComposition 3D 轉換
- DirectComposition 不透明度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728496309f62aaa0027ca3751a6681384fb83c95
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383202"
---
# <a name="how-to-apply-effects"></a><span data-ttu-id="6a065-108">如何套用效果</span><span class="sxs-lookup"><span data-stu-id="6a065-108">How to apply effects</span></span>

> [!NOTE]
> <span data-ttu-id="6a065-109">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="6a065-109">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="6a065-110">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="6a065-110">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="6a065-111">本主題將示範如何使用 Microsoft DirectComposition 將效果和3D 轉換套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="6a065-111">This topic demonstrates how to use Microsoft DirectComposition to apply effects and 3D transformations to a visual.</span></span> <span data-ttu-id="6a065-112">本主題中的範例會變更視覺效果的不透明度，並繞著位於視覺效果中央的垂直軸旋轉。</span><span class="sxs-lookup"><span data-stu-id="6a065-112">The example in this topic changes the opacity of a visual and rotates it around a vertical axis located at the center of the visual.</span></span> <span data-ttu-id="6a065-113">若要深入瞭解 DirectComposition 支援的其他效果，請參閱 [效果](effects.md)。</span><span class="sxs-lookup"><span data-stu-id="6a065-113">To learn more about other effects supported by DirectComposition, see [Effects](effects.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6a065-114">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="6a065-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6a065-115">技術</span><span class="sxs-lookup"><span data-stu-id="6a065-115">Technologies</span></span>

-   [<span data-ttu-id="6a065-116">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="6a065-116">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="6a065-117">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="6a065-117">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="6a065-118">DirectX Graphic Infrastructure (DXGI) </span><span class="sxs-lookup"><span data-stu-id="6a065-118">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="6a065-119">必要條件</span><span class="sxs-lookup"><span data-stu-id="6a065-119">Prerequisites</span></span>

-   <span data-ttu-id="6a065-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="6a065-120">C/C++</span></span>
-   <span data-ttu-id="6a065-121">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="6a065-121">Microsoft Win32</span></span>
-   <span data-ttu-id="6a065-122">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="6a065-122">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="6a065-123">指示</span><span class="sxs-lookup"><span data-stu-id="6a065-123">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="6a065-124">步驟1：初始化 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="6a065-124">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="6a065-125">建立裝置物件和組合目標物件。</span><span class="sxs-lookup"><span data-stu-id="6a065-125">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="6a065-126">建立視覺效果、設定其內容，並將它新增至視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="6a065-126">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="6a065-127">如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。</span><span class="sxs-lookup"><span data-stu-id="6a065-127">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-a-3d-rotate-transform-object-an-effect-group-object-and-an-animation-object"></a><span data-ttu-id="6a065-128">步驟2：建立3D 旋轉轉換物件、效果群組物件和動畫物件</span><span class="sxs-lookup"><span data-stu-id="6a065-128">Step 2: Create a 3D rotate transform object, an effect group object, and an animation object</span></span>

<span data-ttu-id="6a065-129">您可以使用 [**IDCompositionDevice：： CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) 方法來建立3d 旋轉轉換物件，並使用 [**CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) 方法來建立效果群組物件。</span><span class="sxs-lookup"><span data-stu-id="6a065-129">Use the [**IDCompositionDevice::CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) method to create a 3D rotate transform object, and the [**CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) method to create an effect group object.</span></span> <span data-ttu-id="6a065-130">此範例也會使用 [**CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) 方法來建立動畫物件，以製作3d 旋轉轉換的動畫。</span><span class="sxs-lookup"><span data-stu-id="6a065-130">This example also uses the [**CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) method to create an animation object for animating the 3D rotate transform.</span></span> <span data-ttu-id="6a065-131">若要深入瞭解如何套用動畫，請參閱 [如何套用動畫](how-to--animate-a-visual.md)。</span><span class="sxs-lookup"><span data-stu-id="6a065-131">To learn more about applying animations, see [How to apply animations](how-to--animate-a-visual.md).</span></span>


```C++
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;


    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }
```





### <a name="step-3-define-the-animation-function"></a><span data-ttu-id="6a065-132">步驟3：定義動畫函數</span><span class="sxs-lookup"><span data-stu-id="6a065-132">Step 3: Define the animation function</span></span>

<span data-ttu-id="6a065-133">使用 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 物件的方法來定義動畫函數。</span><span class="sxs-lookup"><span data-stu-id="6a065-133">Use the methods of the [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) object to define the animation function.</span></span>

<span data-ttu-id="6a065-134">下列範例會定義簡單的動畫函數。</span><span class="sxs-lookup"><span data-stu-id="6a065-134">The following example defines a simple animation function.</span></span> <span data-ttu-id="6a065-135">當套用至物件屬性時，動畫函式會以累加方式將屬性值從0變更為一秒的 *度數* 引數值。</span><span class="sxs-lookup"><span data-stu-id="6a065-135">When applied to an object property, the animation function incrementally changes the property value from 0 to the value of the *degrees* argument over the course of one second.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);
```



### <a name="step-4-set-the-properties-of-the-3d-rotate-transform"></a><span data-ttu-id="6a065-136">步驟4：設定3D 旋轉轉換的屬性</span><span class="sxs-lookup"><span data-stu-id="6a065-136">Step 4: Set the properties of the 3D rotate transform</span></span>

1.  <span data-ttu-id="6a065-137">藉由呼叫 [**IDCompositionRotateTransform3D：： SetAngle**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation)) 方法，將動畫函數套用至3d 旋轉轉換的 Angle 屬性。</span><span class="sxs-lookup"><span data-stu-id="6a065-137">Apply the animation function to the Angle property of the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetAngle**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation)) method.</span></span>
2.  <span data-ttu-id="6a065-138">藉由呼叫 [**IDCompositionRotateTransform3D：： SetAxisX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float))、 [**SetAxisY**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisy)和 [**SetAxisZ**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisz) 方法，設定3d 旋轉轉換的旋轉軸。</span><span class="sxs-lookup"><span data-stu-id="6a065-138">Set the axis of rotation for the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetAxisX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)), [**SetAxisY**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisy), and [**SetAxisZ**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisz) methods.</span></span>
3.  <span data-ttu-id="6a065-139">藉由呼叫 [**IDCompositionRotateTransform3D：： SetCenterX**](/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)) 和 [**SetCenterY**](/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)) 方法，設定3d 旋轉轉換的旋轉中心。</span><span class="sxs-lookup"><span data-stu-id="6a065-139">Set the center of rotation for the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetCenterX**](/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)) and [**SetCenterY**](/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)) methods.</span></span>

<span data-ttu-id="6a065-140">下列範例會設定3D 旋轉轉換，以在視覺效果的中央周圍垂直軸旋轉視覺效果。</span><span class="sxs-lookup"><span data-stu-id="6a065-140">The following example sets up a 3D rotate transform for spinning a visual around a vertical axis located at the center of the visual.</span></span> <span data-ttu-id="6a065-141">*M \_ bitmapWidth* 和 *m \_ bitmapHeight* 參數是點陣圖的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a065-141">The *m\_bitmapWidth* and *m\_bitmapHeight* parameters are the width and height of the bitmap, in pixels.</span></span>


```C++
        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual's bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual's bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }
```



### <a name="step-5-set-the-properties-of-the-effect-group-object"></a><span data-ttu-id="6a065-142">步驟5：設定效果群組物件的屬性</span><span class="sxs-lookup"><span data-stu-id="6a065-142">Step 5: Set the properties of the effect group object</span></span>

1.  <span data-ttu-id="6a065-143">藉由呼叫 [**IDCompositionEffectGroup：： SetTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d) 方法，將3d 旋轉轉換物件套用至效果群組物件的 system.windows.media.media3d.transform3d> 屬性。</span><span class="sxs-lookup"><span data-stu-id="6a065-143">Apply the 3D rotate transform object to the Transform3D property of the effect group object by calling the [**IDCompositionEffectGroup::SetTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d) method.</span></span>
2.  <span data-ttu-id="6a065-144">藉由呼叫 [**IDCompositionEffectGroup：： SetOpacity**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float))，設定效果群組物件的不透明度屬性。</span><span class="sxs-lookup"><span data-stu-id="6a065-144">Set the Opacity property of the effect group object by calling the [**IDCompositionEffectGroup::SetOpacity**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float)).</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }


    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }
```





### <a name="step-6-apply-the-effect-group-object-to-the-effect-property-of-the-visual"></a><span data-ttu-id="6a065-145">步驟6：將效果群組物件套用至視覺效果的效果屬性</span><span class="sxs-lookup"><span data-stu-id="6a065-145">Step 6: Apply the effect group object to the Effect property of the visual</span></span>

<span data-ttu-id="6a065-146">呼叫 [**IDCompositionVisual：： SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) 方法，將效果群組物件套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="6a065-146">Call the [**IDCompositionVisual::SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) method to apply the effect group object to the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }
```



### <a name="step-7-commit-the-composition"></a><span data-ttu-id="6a065-147">步驟7：認可組合</span><span class="sxs-lookup"><span data-stu-id="6a065-147">Step 7: Commit the composition</span></span>

<span data-ttu-id="6a065-148">呼叫 [**IDCompositionDevice：： commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法，將命令批次認可到 DirectComposition 進行處理。</span><span class="sxs-lookup"><span data-stu-id="6a065-148">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to DirectComposition for processing.</span></span> <span data-ttu-id="6a065-149">產生的組合會出現在目標視窗中。</span><span class="sxs-lookup"><span data-stu-id="6a065-149">The resulting composition appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }
```



### <a name="step-8-free-the-directcomposition-objects"></a><span data-ttu-id="6a065-150">步驟8：釋放 DirectComposition 物件</span><span class="sxs-lookup"><span data-stu-id="6a065-150">Step 8: Free the DirectComposition objects</span></span>

<span data-ttu-id="6a065-151">當您不再需要時，請務必釋出動畫物件、3D 旋轉轉換物件和效果群組物件。</span><span class="sxs-lookup"><span data-stu-id="6a065-151">Be sure to free the animation object, the 3D rotate transform object, and the effect group object when you no longer need them.</span></span> <span data-ttu-id="6a065-152">下列範例會呼叫應用程式定義的 [**SafeRelease**](/windows/desktop/medfound/saferelease) 宏來釋放物件。</span><span class="sxs-lookup"><span data-stu-id="6a065-152">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the objects.</span></span>


```C++
    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);
```



<span data-ttu-id="6a065-153">也請記得在您的應用程式結束之前釋放裝置物件、組合目標物件和視覺效果。</span><span class="sxs-lookup"><span data-stu-id="6a065-153">Also remember to free the device object, the composition target object, and the visual before your application exits.</span></span> <span data-ttu-id="6a065-154">如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。</span><span class="sxs-lookup"><span data-stu-id="6a065-154">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="6a065-155">完整範例</span><span class="sxs-lookup"><span data-stu-id="6a065-155">Complete example</span></span>


```C++
//
// ApplyEffects.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition and Direct3D Header Files
#include <dcomp.h>
#include <d3d11.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnPaint();
    HRESULT OnClientClick(int xPos, int yPos);
    HRESULT OnMouseMove(int xPos, int yPos);

    HRESULT LoadResourceGDIBitmap(
        PCWSTR resourceName, 
        HBITMAP &hbmp
        );

    HRESULT MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface);

    HRESULT SetVisualOpacity(IDCompositionVisual *pVisual, float opacity);
    HRESULT RotateVisual(IDCompositionVisual *pVisual,float degrees);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    HBITMAP m_hBitmap;
    int m_bitmapWidth;
    int m_bitmapHeight;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    IDCompositionVisual *m_pVisual;
 };


//
// ApplyEffects.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Hover over the image to see the opacity change. Click
//   the image to apply a 3D rotation.

#include &quot;ApplyEffects.h&quot;

#define OFFSET_X 20
#define OFFSET_Y 20
#define TRANSPARENT 0.5
#define OPAQUE 1.0

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmap(NULL),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr),
    m_pD3D11Device(nullptr),
    m_pVisual(nullptr),
    m_bitmapHeight(0),
    m_bitmapWidth(0)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pVisual);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L&quot;DirectCompDemoApp&quot;,
        L&quot;DirectComposition Demo Application&quot;,
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;

    if (SUCCEEDED(hr))
    {   
        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    if (SUCCEEDED(hr))
    {
       ShowWindow(m_hwnd, SW_SHOWNORMAL);
       UpdateWindow(m_hwnd);
    }    

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object.
    D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT,
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        NULL);

    IDXGIDevice *pDXGIDevice = nullptr;

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pCompTarget);   
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L&quot;Penguins&quot;, m_hBitmap);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    DeleteObject(m_hBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  Called when the application&#39;s main window is painted. This     *
*  method builds a simple visual tree and passes it to            *
*  DirectComposition.                                             *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnPaint()
{
    HRESULT hr = S_OK;
    IDCompositionSurface *pSurface = nullptr;

    // Create a visual object.          
    hr = m_pDevice->CreateVisual(&m_pVisual);  

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = m_pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        m_pVisual->SetOffsetX(OFFSET_X);  
        m_pVisual->SetOffsetY(OFFSET_Y);  
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
    }

   if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pCompTarget->SetRoot(m_pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Called when the mouse moves in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual, and calls an application-defined function to set the   *
*  visual&#39;s opacity.                                              *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnMouseMove(int xPos, int yPos)
{
    HRESULT hr = S_OK;
    static BOOL fOverImage = FALSE;

    // Determine whether the cursor is over the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        if (!fOverImage)
        {
            // The cursor has moved over the visual, so make the visual 
            // 100% opaque.
            hr = SetVisualOpacity(m_pVisual, OPAQUE);
            fOverImage = TRUE;
        }
    }

    else if (fOverImage)
    {
        // The cursor has moved off the visual, so make the visual
        // 50% opaque.
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
        fOverImage = FALSE;
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Changes the opacity of a visual.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::SetVisualOpacity(IDCompositionVisual *pVisual, float opacity)
{
    HRESULT hr = S_OK;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (opacity > 1.0f || opacity < 0.0f))
        return E_INVALIDARG;

    // Create an effect group object.
    hr = m_pDevice->CreateEffectGroup(&pEffectGroup);

    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = m_pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Free the effect group object.
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  Called when the user clicks in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual and calls an application-defined function to rotate the *
*  visual.                                                        *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnClientClick(int xPos, int yPos)
{
    HRESULT hr = S_OK;

    // Determine whether the mouse cursor is over the visual. If so,
    // rotate the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        hr = RotateVisual(m_pVisual, 360.0f);
    }
    
    return hr;
}

/******************************************************************
*                                                                 *
*  Performs an animated 3D rotation of a visual.                  *
*                                                                 *
******************************************************************/

HRESULT DemoApp::RotateVisual(IDCompositionVisual *pVisual, float degrees)
{
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (degrees > 360.0f || degrees < -360.0f))
        return E_INVALIDARG;

    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }

    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);

        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual&#39;s bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual&#39;s bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_MOUSEMOVE:
                {
                    pDemoApp->OnMouseMove(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_PAINT:
                {
                    pDemoApp->OnPaint();
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}

// CreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    hr =  hBitmap ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Get information about the bitmap.
        bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);
    }

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        m_bitmapWidth = bmp.bmWidth;
        m_bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(m_bitmapWidth, m_bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    hr = pDCSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Create a compatible (DC) and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                m_bitmapWidth, m_bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    SafeRelease(&pDXGISurface);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="6a065-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a065-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a065-157">影響</span><span class="sxs-lookup"><span data-stu-id="6a065-157">Effects</span></span>](effects.md)
</dt> </dl>

 

 