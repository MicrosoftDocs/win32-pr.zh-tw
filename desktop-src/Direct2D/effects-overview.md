---
title: 效果 (Direct2D)
description: Direct2D 效果的總覽。
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0a88ff64721fc32955416dcfe108b1c9e87f7565a67fc2e1d8192a1eaf369d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317982"
---
# <a name="effects"></a>效果

## <a name="what-are-direct2d-effects"></a>什麼是 Direct2D 效果？

您可以使用 Direct2D 將一或多個高品質效果套用至影像或一組影像。 效果 Api 是在 [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) 上建立的，並利用 GPU 功能來處理圖像。 您可以在效果圖形中連鎖效果，並撰寫或 blend 效果的輸出。

Direct2D 效果會執行影像工作，例如變更亮度、對影像進行飽和，或建立陰影。 效果可以接受零個以上的輸入影像、公開多個控制其作業的屬性，以及產生單一輸出影像。

每個效果都會建立由個別轉換所組成的內部轉換圖形。 每個轉換都代表單一映射作業。 轉換的主要目的是要存放針對每個輸出圖元執行的著色器。 這些著色器可以包含圖元著色器、頂點著色器、GPU 的 blend 階段，以及計算著色器。

Direct2D 的[](./direct2d-portal.md) [內建效果](built-in-effects.md)，以及您可以使用[自訂效果 API](custom-effects.md)進行的自訂效果，都可透過這種方式運作。

其中有各種類別的內 [建效果](built-in-effects.md) ，如下所示。 如需完整清單，請參閱 [內建效果](built-in-effects.md) 一節。

-   [篩選](built-in-effects.md)
-   [撰寫和混合](built-in-effects.md)
-   [透明度](built-in-effects.md)
-   [色彩](built-in-effects.md)
-   [光源和 Stylizing](built-in-effects.md)
-   [轉換和調整](built-in-effects.md)
-   [來源](built-in-effects.md)

您可以將效果套用至任何點陣圖，包括： [Windows 影像處理元件 (WIC) ](/windows/desktop/wic/-wic-api)所載入的影像、 [Direct2D](./direct2d-portal.md)所繪製的基本專案、 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)中的文字，或[Direct3D](/windows/desktop/direct3d10/d3d10-graphics)轉譯的場景。

有了 Direct2D 效果，您可以撰寫自己的效果，以用於您的應用程式。 自訂效果架構可讓您使用 GPU 功能，例如圖元著色器、頂點著色器和混合單位。 您也可以在自訂效果中包含其他內建或自訂效果。 建立自訂效果的架構與用來建立 [Direct2D](./direct2d-portal.md)內建效果的架構相同。 [Direct2D 效果作者 API](custom-effects.md)提供一組介面，用來建立及註冊效果。

### <a name="more-effects-topics"></a>其他效果主題

本主題的其餘部分將說明 Direct2D 效果的基本概念，例如將效果套用至影像。 這裡的表格提供有關效果的其他主題連結。

| 主題                                                                                                                    | 描述                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [效果著色器連結](effect-shader-linking.md)<br/>                                                            | Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。<br/>                                               |
| [自訂效果](custom-effects.md)<br/>                                                                          | 說明如何使用標準 HLSL 撰寫您自己的自訂效果。<br/>                                                                                                                |
| [如何使用 FilePicker 將影像載入 Direct2D 效果](load-a-id2d1image-using-the-filepicker.md)<br/> | 顯示如何使用 [**Windows：：儲存體：:P ickers：： FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)將影像載入 Direct2D 效果。<br/>                                      |
| [如何將 Direct2D 內容儲存至影像檔案](save-direct2d-content-to-an-image-file.md)<br/>                   | 本主題說明如何使用 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)將 ID2D1Image 形式的內容以 [](/windows/win32/api/d2d1/nn-d2d1-id2d1image)形式儲存至編碼的影像檔案，例如 JPEG。<br/> |
| [如何將效果套用至基本專案](how-to-apply-effects-to-primitives.md)<br/>                                  | 本主題說明如何將一連串效果套用至[Direct2D](./direct2d-portal.md)和[DirectWrite](direct2d-and-directwrite.md)基本專案。<br/>                           |
| [控制效果圖形中的有效位數和數位裁剪](precision-and-clipping-in-effect-graphs.md)<br/>  | 使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。 <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>將效果套用至影像

您可以使用 Direct2D 效果 API，將轉換套用至影像。

> [!Note]  
> 此範例假設您已建立 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 和 [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) 物件。 如需建立這些物件的詳細資訊，請參閱如何使用 FilePicker 和[裝置和裝置](devices-and-device-contexts.md)內容將[影像載入 Direct2D 效果](load-a-id2d1image-using-the-filepicker.md)。

 

1.  宣告 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)變數，然後使用 [**ID2DDeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法來建立 [點陣圖來源](bitmap-source.md)效果。

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))，將 BitmapSource 屬性設定為 WIC 點陣圖來源。

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  宣告 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 變數，然後建立 [高斯模糊](gaussian-blur.md) 效果。

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  設定要從點陣圖來源效果接收影像的輸入。 設定 [ [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法] 和 [標準差] 屬性的模糊量。

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  使用裝置內容來繪製產生的影像輸出。

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))方法必須在 [**ID2DDeviceCoNtext：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)和 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之間呼叫，就像其他 Direct2D 轉譯作業一樣。 **DrawImage** 可以取得影像或效果的輸出，並將其轉譯為目標介面。

## <a name="spatial-transforms"></a>空間轉換

Direct2D 提供內建效果，可轉換2D 和3D 空間中的影像，以及進行調整。 比例和轉換效果提供各種品質層級，例如：最接近的鄰近、線性、三次、多取樣線性、非等向和高品質的三層。

> [!Note]  
> 當調整時，非等向模式會產生 mipmap，不過，如果您在輸入轉換的效果 **上將快取的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



這種使用2D 仿射轉換效果會稍微旋轉點陣圖。



| 之前                                                            |
|-------------------------------------------------------------------|
| ![影像之前的2d 仿射效果。](images/default-before.jpg)      |
| After                                                             |
| ![影像之後的2d 仿射效果。](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>組合影像

某些效果接受多個輸入，並將它們複合成一個產生的影像。

內建的複合和算術複合效果提供各種不同的模式。如需詳細資訊，請參閱 [複合](composite.md) 主題。 [Blend](blend.md)效果有各種可用的 GPU 加速模式。


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



複合效果會根據您指定的模式，將影像以各種不同的方式結合。

## <a name="pixel-adjustments"></a>圖元調整

有幾個內建的 Direct2D 效果可讓您變更圖元資料。 例如，您可以使用色彩矩陣效果來變更影像的色彩。


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



此程式碼會採用影像並改變色彩，如這裡的範例影像所示。



| 之前                                                          |
|-----------------------------------------------------------------|
| ![影像之前的色彩矩陣效果。](images/default-before.jpg) |
| After                                                           |
| ![影像之後的色彩矩陣效果。](images/15-colormatrix.png)  |



 

如需詳細資訊，請參閱 [色彩內建效果](how-to-create-a-solid-color-brush.md) 一節。

## <a name="building-effect-graphs"></a>建立效果圖形

您可以將效果串連在一起，以轉換影像。 例如，此處的程式碼會套用陰影和2D 轉換，然後將結果合成在一起。


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



以下是結果。

![陰影效果輸出。](images/effect-overview-shadow.png)

效果會將 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) 物件做為輸入。 您可以使用 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，因為介面衍生自 **ID2D1Image**。 您也可以使用 [**ID2D1Effect：： GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) 來取得 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件的輸出作為 **ID2D1Image** ，或使用 **SetInputEffect** 方法來為您轉換輸出。 在大部分情況下，效果圖表是由直接連結在一起的 **ID2D1Effect** 物件所組成，可讓您輕鬆地將多個效果套用至影像，以建立吸引人的視覺效果。

如需詳細資訊，請參閱 [如何將效果套用至基本](how-to-apply-effects-to-primitives.md) 專案。

## <a name="related-topics"></a>相關主題

[Direct2D 基本影像效果範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[內建效果](built-in-effects.md)