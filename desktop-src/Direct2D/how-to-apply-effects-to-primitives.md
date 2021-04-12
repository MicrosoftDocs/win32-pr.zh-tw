---
title: 如何將效果套用至基本專案
description: 本主題說明如何將一連串效果套用至 Direct2D 和 DirectWrite 基本專案。
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376153"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="5461d-103">如何將效果套用至基本專案</span><span class="sxs-lookup"><span data-stu-id="5461d-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="5461d-104">本主題說明如何將一連串效果套用至 [Direct2D](./direct2d-portal.md) 和 [DirectWrite](direct2d-and-directwrite.md) 基本專案。</span><span class="sxs-lookup"><span data-stu-id="5461d-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="5461d-105">您可以使用 [Direct2D 效果 API](effects-overview.md) ，將效果圖形套用至 [Direct2D](./direct2d-portal.md) 轉譯成影像的基本專案。</span><span class="sxs-lookup"><span data-stu-id="5461d-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="5461d-106">這裡的範例有兩個圓角矩形和文字 "Direct2D"。</span><span class="sxs-lookup"><span data-stu-id="5461d-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="5461d-107">使用 Direct2D 繪製矩形和 [DirectWrite](direct2d-and-directwrite.md) 來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="5461d-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![內有文字 "direct2d" 的矩形。](images/direct2d-rounded.png)

<span data-ttu-id="5461d-109">您可以使用 [Direct2D 效果](effects-overview.md)，讓影像看起來像下圖。</span><span class="sxs-lookup"><span data-stu-id="5461d-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="5461d-110">將 [高斯模糊](gaussian-blur.md)、 [點反射光源](specular-lighting.md)、 [算術複合](arithmetic-composite.md)和 [複合](composite.md) 效果套用至2d 基本專案，以在此處建立影像。</span><span class="sxs-lookup"><span data-stu-id="5461d-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![套用數個效果之後，會在其中包含文字 "direct2d" 的矩形。](images/direct2d-svg.png)

<span data-ttu-id="5461d-112">將矩形和文字轉譯成中繼介面之後，您可以使用這個作為影像圖形中 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件的輸入。</span><span class="sxs-lookup"><span data-stu-id="5461d-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="5461d-113">在此範例中，請將原始影像設定為 [高斯模糊效果](gaussian-blur.md) 的輸入，然後將模糊的輸出設定為 [點反射光源效果](specular-lighting.md)的輸入。</span><span class="sxs-lookup"><span data-stu-id="5461d-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="5461d-114">然後，這項效果的結果會與原始影像組成兩次，以取得呈現至視窗的最終影像。</span><span class="sxs-lookup"><span data-stu-id="5461d-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="5461d-115">以下是影像圖形的圖表。</span><span class="sxs-lookup"><span data-stu-id="5461d-115">Here is a diagram of the image graph.</span></span>

![效果圖表。](images/effect-graph.png)

<span data-ttu-id="5461d-117">此效果圖形包含四個 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件，每個物件都代表不同的內建效果。</span><span class="sxs-lookup"><span data-stu-id="5461d-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="5461d-118">您可以使用 [**ID1D1Factory1：： RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)，以相同的方式建立和連接自訂效果。</span><span class="sxs-lookup"><span data-stu-id="5461d-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="5461d-119">此處的程式碼會建立效果、設定屬性，並連接稍早所示的效果圖形。</span><span class="sxs-lookup"><span data-stu-id="5461d-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="5461d-120">使用 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法建立 [高斯模糊](gaussian-blur.md)效果，並指定適當的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="5461d-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="5461d-121">內建效果的 Clsid 定義于 d2d1effects 中。</span><span class="sxs-lookup"><span data-stu-id="5461d-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="5461d-122">然後，您可以使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法來設定模糊的標準差。</span><span class="sxs-lookup"><span data-stu-id="5461d-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    <span data-ttu-id="5461d-123">[高斯模糊](gaussian-blur.md)效果會模糊影像的所有通道，包括 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="5461d-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="5461d-124">建立 [反射光源](point-specular.md) 效果並設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5461d-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="5461d-125">光線的位置是3個浮點數的向量，因此您必須將它宣告為個別的變數，並將它傳遞給 [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法。</span><span class="sxs-lookup"><span data-stu-id="5461d-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    <span data-ttu-id="5461d-126">[反射光源](point-specular.md)效果使用輸入的 Alpha 通道來建立光源的高度地圖。</span><span class="sxs-lookup"><span data-stu-id="5461d-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="5461d-127">有兩個不同的複合效果，您可以使用 [複合](composite.md) 效果和 [算術複合](arithmetic-composite.md)。</span><span class="sxs-lookup"><span data-stu-id="5461d-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="5461d-128">此效果圖形同時使用這兩者。</span><span class="sxs-lookup"><span data-stu-id="5461d-128">This effect graph uses both.</span></span>

    <span data-ttu-id="5461d-129">建立 [複合](composite.md) 效果，並在中將模式設定為 D2D1 \_ 複合 \_ 模式 \_ 來源 \_ ，以輸出來源和目的影像的交集。</span><span class="sxs-lookup"><span data-stu-id="5461d-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="5461d-130">[算術複合](arithmetic-composite.md)效果會根據全球資訊網協會 (W3C) 針對可調整向量圖形 (SVG) 標準所定義的公式來撰寫兩個輸入影像。</span><span class="sxs-lookup"><span data-stu-id="5461d-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="5461d-131">建立算術複合並設定公式的係數。</span><span class="sxs-lookup"><span data-stu-id="5461d-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    <span data-ttu-id="5461d-132">[算術複合](arithmetic-composite.md)效果的係數如下所示。</span><span class="sxs-lookup"><span data-stu-id="5461d-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="5461d-133">在此效果圖形中，這兩個複合效果會將其他效果的輸出和中繼介面視為輸入，並將它們合成。</span><span class="sxs-lookup"><span data-stu-id="5461d-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="5461d-134">最後，您可以將輸入設定為適當的影像和點陣圖，以連接圖形的效果。</span><span class="sxs-lookup"><span data-stu-id="5461d-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="5461d-135">第一個效果（ [高斯模糊](gaussian-blur.md)）會從您呈現基本專案的中繼介面接收其輸入。</span><span class="sxs-lookup"><span data-stu-id="5461d-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="5461d-136">您可以使用 [**ID2D1Effect：： SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) 方法來設定輸入，並指定 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="5461d-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="5461d-137">高斯模糊和 [反射光源](point-specular.md) 效果只有單一輸入。</span><span class="sxs-lookup"><span data-stu-id="5461d-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="5461d-138">反射光源效果使用亮度模糊的模糊 Alpha 色板</span><span class="sxs-lookup"><span data-stu-id="5461d-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="5461d-139">[複合](composite.md)和[算術複合](arithmetic-composite.md)效果具有多個輸入。</span><span class="sxs-lookup"><span data-stu-id="5461d-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="5461d-140">為確保映射會以正確的順序放在一起，您必須為每個輸入影像指定正確的索引。</span><span class="sxs-lookup"><span data-stu-id="5461d-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  <span data-ttu-id="5461d-141">將 [算術複合](arithmetic-composite.md) 效果物件傳遞至 [**ID2DDeviceCoNtext：:D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) 方法，並處理和繪製圖形的輸出。</span><span class="sxs-lookup"><span data-stu-id="5461d-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 