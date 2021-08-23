---
title: 如何將效果套用至基本專案
description: 本主題說明如何將一連串效果套用至 Direct2D 和 DirectWrite 基本專案。
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569576"
---
# <a name="how-to-apply-effects-to-primitives"></a>如何將效果套用至基本專案

本主題說明如何將一連串效果套用至[Direct2D](./direct2d-portal.md)和[DirectWrite](direct2d-and-directwrite.md)基本專案。

您可以使用 [Direct2D 效果 API](effects-overview.md) ，將效果圖形套用至 [Direct2D](./direct2d-portal.md) 轉譯成影像的基本專案。 這裡的範例有兩個圓角矩形和文字 "Direct2D"。 使用 Direct2D 繪製矩形， [DirectWrite](direct2d-and-directwrite.md)繪製文字。

![內有文字 "direct2d" 的矩形。](images/direct2d-rounded.png)

您可以使用 [Direct2D 效果](effects-overview.md)，讓影像看起來像下圖。 將 [高斯模糊](gaussian-blur.md)、 [點反射光源](specular-lighting.md)、 [算術複合](arithmetic-composite.md)和 [複合](composite.md) 效果套用至2d 基本專案，以在此處建立影像。

![套用數個效果之後，會在其中包含文字 "direct2d" 的矩形。](images/direct2d-svg.png)

將矩形和文字轉譯成中繼介面之後，您可以使用這個作為影像圖形中 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件的輸入。

在此範例中，請將原始影像設定為 [高斯模糊效果](gaussian-blur.md) 的輸入，然後將模糊的輸出設定為 [點反射光源效果](specular-lighting.md)的輸入。 然後，這項效果的結果會與原始影像組成兩次，以取得呈現至視窗的最終影像。

以下是影像圖形的圖表。

![效果圖表。](images/effect-graph.png)

此效果圖形包含四個 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件，每個物件都代表不同的內建效果。 您可以使用 [**ID1D1Factory1：： RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)，以相同的方式建立和連接自訂效果。 此處的程式碼會建立效果、設定屬性，並連接稍早所示的效果圖形。

1.  使用 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法建立 [高斯模糊](gaussian-blur.md)效果，並指定適當的 CLSID。 內建效果的 Clsid 定義于 d2d1effects 中。 然後，您可以使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法來設定模糊的標準差。

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

    

    [高斯模糊](gaussian-blur.md)效果會模糊影像的所有通道，包括 Alpha 色板。

2.  建立 [反射光源](point-specular.md) 效果並設定屬性。 光線的位置是3個浮點數的向量，因此您必須將它宣告為個別的變數，並將它傳遞給 [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法。

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

    

    [反射光源](point-specular.md)效果使用輸入的 Alpha 通道來建立光源的高度地圖。

3.  有兩個不同的複合效果，您可以使用 [複合](composite.md) 效果和 [算術複合](arithmetic-composite.md)。 此效果圖形同時使用這兩者。

    建立 [複合](composite.md) 效果，並在中將模式設定為 D2D1 \_ 複合 \_ 模式 \_ 來源 \_ ，以輸出來源和目的影像的交集。

    [算術複合](arithmetic-composite.md)效果會根據全球資訊網協會 (W3C) 針對可調整向量圖形 (SVG) 標準所定義的公式來撰寫兩個輸入影像。 建立算術複合並設定公式的係數。

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

    

    [算術複合](arithmetic-composite.md)效果的係數如下所示。

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    在此效果圖形中，這兩個複合效果會將其他效果的輸出和中繼介面視為輸入，並將它們合成。

4.  最後，您可以將輸入設定為適當的影像和點陣圖，以連接圖形的效果。

    第一個效果（ [高斯模糊](gaussian-blur.md)）會從您呈現基本專案的中繼介面接收其輸入。 您可以使用 [**ID2D1Effect：： SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) 方法來設定輸入，並指定 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) 物件的索引。 高斯模糊和 [反射光源](point-specular.md) 效果只有單一輸入。 反射光源效果使用亮度模糊的模糊 Alpha 色板

    [複合](composite.md)和[算術複合](arithmetic-composite.md)效果具有多個輸入。 為確保映射會以正確的順序放在一起，您必須為每個輸入影像指定正確的索引。

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

    

5.  將 [算術複合](arithmetic-composite.md) 效果物件傳遞至 [**ID2DDeviceCoNtext：:D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) 方法，並處理和繪製圖形的輸出。

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

    

 

 