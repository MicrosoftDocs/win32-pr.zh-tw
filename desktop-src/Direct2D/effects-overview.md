---
title: 效果 (Direct2D)
description: Direct2D 效果的總覽。
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023843"
---
# <a name="effects"></a><span data-ttu-id="41227-103">效果</span><span class="sxs-lookup"><span data-stu-id="41227-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="41227-104">什麼是 Direct2D 效果？</span><span class="sxs-lookup"><span data-stu-id="41227-104">What are Direct2D effects?</span></span>

<span data-ttu-id="41227-105">您可以使用 Direct2D 將一或多個高品質效果套用至影像或一組影像。</span><span class="sxs-lookup"><span data-stu-id="41227-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="41227-106">效果 Api 是在 [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) 上建立的，並利用 GPU 功能來處理圖像。</span><span class="sxs-lookup"><span data-stu-id="41227-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="41227-107">您可以在效果圖形中連鎖效果，並撰寫或 blend 效果的輸出。</span><span class="sxs-lookup"><span data-stu-id="41227-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="41227-108">Direct2D 效果會執行影像工作，例如變更亮度、對影像進行飽和，或建立陰影。</span><span class="sxs-lookup"><span data-stu-id="41227-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="41227-109">效果可以接受零個以上的輸入影像、公開多個控制其作業的屬性，以及產生單一輸出影像。</span><span class="sxs-lookup"><span data-stu-id="41227-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="41227-110">每個效果都會建立由個別轉換所組成的內部轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="41227-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="41227-111">每個轉換都代表單一映射作業。</span><span class="sxs-lookup"><span data-stu-id="41227-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="41227-112">轉換的主要目的是要存放針對每個輸出圖元執行的著色器。</span><span class="sxs-lookup"><span data-stu-id="41227-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="41227-113">這些著色器可以包含圖元著色器、頂點著色器、GPU 的 blend 階段，以及計算著色器。</span><span class="sxs-lookup"><span data-stu-id="41227-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="41227-114">Direct2D 的[](./direct2d-portal.md) [內建效果](built-in-effects.md)，以及您可以使用[自訂效果 API](custom-effects.md)進行的自訂效果，都可透過這種方式運作。</span><span class="sxs-lookup"><span data-stu-id="41227-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="41227-115">其中有各種類別的內 [建效果](built-in-effects.md) ，如下所示。</span><span class="sxs-lookup"><span data-stu-id="41227-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="41227-116">如需完整清單，請參閱 [內建效果](built-in-effects.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="41227-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="41227-117">篩選</span><span class="sxs-lookup"><span data-stu-id="41227-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-118">撰寫和混合</span><span class="sxs-lookup"><span data-stu-id="41227-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-119">透明度</span><span class="sxs-lookup"><span data-stu-id="41227-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-120">色彩</span><span class="sxs-lookup"><span data-stu-id="41227-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-121">光源和 Stylizing</span><span class="sxs-lookup"><span data-stu-id="41227-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-122">轉換和調整</span><span class="sxs-lookup"><span data-stu-id="41227-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="41227-123">來源</span><span class="sxs-lookup"><span data-stu-id="41227-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="41227-124">您可以將效果套用至任何點陣圖，包括： [Windows 影像處理元件 (WIC) ](/windows/desktop/wic/-wic-api)所載入的影像、 [Direct2D](./direct2d-portal.md)所繪製的基本專案、 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)中的文字，或 [Direct3D](/windows/desktop/direct3d10/d3d10-graphics)轉譯的場景。</span><span class="sxs-lookup"><span data-stu-id="41227-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="41227-125">有了 Direct2D 效果，您可以撰寫自己的效果，以用於您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="41227-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="41227-126">自訂效果架構可讓您使用 GPU 功能，例如圖元著色器、頂點著色器和混合單位。</span><span class="sxs-lookup"><span data-stu-id="41227-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="41227-127">您也可以在自訂效果中包含其他內建或自訂效果。</span><span class="sxs-lookup"><span data-stu-id="41227-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="41227-128">建立自訂效果的架構與用來建立 [Direct2D](./direct2d-portal.md)內建效果的架構相同。</span><span class="sxs-lookup"><span data-stu-id="41227-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="41227-129">[Direct2D 效果作者 API](custom-effects.md)提供一組介面，用來建立及註冊效果。</span><span class="sxs-lookup"><span data-stu-id="41227-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="41227-130">其他效果主題</span><span class="sxs-lookup"><span data-stu-id="41227-130">More effects topics</span></span>

<span data-ttu-id="41227-131">本主題的其餘部分將說明 Direct2D 效果的基本概念，例如將效果套用至影像。</span><span class="sxs-lookup"><span data-stu-id="41227-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="41227-132">這裡的表格提供有關效果的其他主題連結。</span><span class="sxs-lookup"><span data-stu-id="41227-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="41227-133">主題</span><span class="sxs-lookup"><span data-stu-id="41227-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="41227-134">描述</span><span class="sxs-lookup"><span data-stu-id="41227-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41227-135">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="41227-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="41227-136">Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。</span><span class="sxs-lookup"><span data-stu-id="41227-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="41227-137">自訂效果</span><span class="sxs-lookup"><span data-stu-id="41227-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="41227-138">說明如何使用標準 HLSL 撰寫您自己的自訂效果。</span><span class="sxs-lookup"><span data-stu-id="41227-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="41227-139">如何使用 FilePicker 將影像載入 Direct2D 效果</span><span class="sxs-lookup"><span data-stu-id="41227-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="41227-140">顯示如何使用 [**Windows：： Storage：:P ickers：： FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) 將影像載入 Direct2D 效果。</span><span class="sxs-lookup"><span data-stu-id="41227-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="41227-141">如何將 Direct2D 內容儲存至影像檔案</span><span class="sxs-lookup"><span data-stu-id="41227-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="41227-142">本主題說明如何使用 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)將 ID2D1Image 形式的內容以 [](/windows/win32/api/d2d1/nn-d2d1-id2d1image)形式儲存至編碼的影像檔案，例如 JPEG。</span><span class="sxs-lookup"><span data-stu-id="41227-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="41227-143">如何將效果套用至基本專案</span><span class="sxs-lookup"><span data-stu-id="41227-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="41227-144">本主題說明如何將一連串效果套用至 [Direct2D](./direct2d-portal.md) 和 [DirectWrite](direct2d-and-directwrite.md) 基本專案。</span><span class="sxs-lookup"><span data-stu-id="41227-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="41227-145">控制效果圖形中的有效位數和數位裁剪</span><span class="sxs-lookup"><span data-stu-id="41227-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="41227-146">使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。</span><span class="sxs-lookup"><span data-stu-id="41227-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="41227-147">將效果套用至影像</span><span class="sxs-lookup"><span data-stu-id="41227-147">Applying an effect to an image</span></span>

<span data-ttu-id="41227-148">您可以使用 Direct2D 效果 API，將轉換套用至影像。</span><span class="sxs-lookup"><span data-stu-id="41227-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="41227-149">此範例假設您已建立 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 和 [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) 物件。</span><span class="sxs-lookup"><span data-stu-id="41227-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="41227-150">如需建立這些物件的詳細資訊，請參閱如何使用 FilePicker 和[裝置和裝置](devices-and-device-contexts.md)內容將[影像載入 Direct2D 效果](load-a-id2d1image-using-the-filepicker.md)。</span><span class="sxs-lookup"><span data-stu-id="41227-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="41227-151">宣告 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)變數，然後使用 [**ID2DDeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法來建立 [點陣圖來源](bitmap-source.md)效果。</span><span class="sxs-lookup"><span data-stu-id="41227-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="41227-152">使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))，將 BitmapSource 屬性設定為 WIC 點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="41227-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="41227-153">宣告 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 變數，然後建立 [高斯模糊](gaussian-blur.md) 效果。</span><span class="sxs-lookup"><span data-stu-id="41227-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="41227-154">設定要從點陣圖來源效果接收影像的輸入。</span><span class="sxs-lookup"><span data-stu-id="41227-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="41227-155">設定 [ [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法] 和 [標準差] 屬性的模糊量。</span><span class="sxs-lookup"><span data-stu-id="41227-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="41227-156">使用裝置內容來繪製產生的影像輸出。</span><span class="sxs-lookup"><span data-stu-id="41227-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="41227-157">[**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))方法必須在 [**ID2DDeviceCoNtext：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)和 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之間呼叫，就像其他 Direct2D 轉譯作業一樣。</span><span class="sxs-lookup"><span data-stu-id="41227-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="41227-158">**DrawImage** 可以取得影像或效果的輸出，並將其轉譯為目標介面。</span><span class="sxs-lookup"><span data-stu-id="41227-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="41227-159">空間轉換</span><span class="sxs-lookup"><span data-stu-id="41227-159">Spatial Transforms</span></span>

<span data-ttu-id="41227-160">Direct2D 提供內建效果，可轉換2D 和3D 空間中的影像，以及進行調整。</span><span class="sxs-lookup"><span data-stu-id="41227-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="41227-161">比例和轉換效果提供各種品質層級，例如：最接近的鄰近、線性、三次、多取樣線性、非等向和高品質的三層。</span><span class="sxs-lookup"><span data-stu-id="41227-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="41227-162">當調整時，非等向模式會產生 mipmap，不過，如果您在輸入轉換的效果 **上將快取的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="41227-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


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



<span data-ttu-id="41227-163">這種使用2D 仿射轉換效果會稍微旋轉點陣圖。</span><span class="sxs-lookup"><span data-stu-id="41227-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="41227-164">之前</span><span class="sxs-lookup"><span data-stu-id="41227-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![影像之前的2d 仿射效果。](images/default-before.jpg)      |
| <span data-ttu-id="41227-166">After</span><span class="sxs-lookup"><span data-stu-id="41227-166">After</span></span>                                                             |
| ![影像之後的2d 仿射效果。](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="41227-168">組合影像</span><span class="sxs-lookup"><span data-stu-id="41227-168">Compositing images</span></span>

<span data-ttu-id="41227-169">某些效果接受多個輸入，並將它們複合成一個產生的影像。</span><span class="sxs-lookup"><span data-stu-id="41227-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="41227-170">內建的複合和算術複合效果提供各種不同的模式。如需詳細資訊，請參閱 [複合](composite.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="41227-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="41227-171">[Blend](blend.md)效果有各種可用的 GPU 加速模式。</span><span class="sxs-lookup"><span data-stu-id="41227-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="41227-172">複合效果會根據您指定的模式，將影像以各種不同的方式結合。</span><span class="sxs-lookup"><span data-stu-id="41227-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="41227-173">圖元調整</span><span class="sxs-lookup"><span data-stu-id="41227-173">Pixel adjustments</span></span>

<span data-ttu-id="41227-174">有幾個內建的 Direct2D 效果可讓您變更圖元資料。</span><span class="sxs-lookup"><span data-stu-id="41227-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="41227-175">例如，您可以使用色彩矩陣效果來變更影像的色彩。</span><span class="sxs-lookup"><span data-stu-id="41227-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


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



<span data-ttu-id="41227-176">此程式碼會採用影像並改變色彩，如這裡的範例影像所示。</span><span class="sxs-lookup"><span data-stu-id="41227-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="41227-177">之前</span><span class="sxs-lookup"><span data-stu-id="41227-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![影像之前的色彩矩陣效果。](images/default-before.jpg) |
| <span data-ttu-id="41227-179">After</span><span class="sxs-lookup"><span data-stu-id="41227-179">After</span></span>                                                           |
| ![影像之後的色彩矩陣效果。](images/15-colormatrix.png)  |



 

<span data-ttu-id="41227-181">如需詳細資訊，請參閱 [色彩內建效果](how-to-create-a-solid-color-brush.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="41227-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="41227-182">建立效果圖形</span><span class="sxs-lookup"><span data-stu-id="41227-182">Building effect graphs</span></span>

<span data-ttu-id="41227-183">您可以將效果串連在一起，以轉換影像。</span><span class="sxs-lookup"><span data-stu-id="41227-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="41227-184">例如，此處的程式碼會套用陰影和2D 轉換，然後將結果合成在一起。</span><span class="sxs-lookup"><span data-stu-id="41227-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


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



<span data-ttu-id="41227-185">以下是結果。</span><span class="sxs-lookup"><span data-stu-id="41227-185">Here is the result.</span></span>

![陰影效果輸出。](images/effect-overview-shadow.png)

<span data-ttu-id="41227-187">效果會將 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) 物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="41227-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="41227-188">您可以使用 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，因為介面衍生自 **ID2D1Image**。</span><span class="sxs-lookup"><span data-stu-id="41227-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="41227-189">您也可以使用 [**ID2D1Effect：： GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) 來取得 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 物件的輸出作為 **ID2D1Image** ，或使用 **SetInputEffect** 方法來為您轉換輸出。</span><span class="sxs-lookup"><span data-stu-id="41227-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="41227-190">在大部分情況下，效果圖表是由直接連結在一起的 **ID2D1Effect** 物件所組成，可讓您輕鬆地將多個效果套用至影像，以建立吸引人的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="41227-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="41227-191">如需詳細資訊，請參閱 [如何將效果套用至基本](how-to-apply-effects-to-primitives.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="41227-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41227-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="41227-192">Related topics</span></span>

[<span data-ttu-id="41227-193">Direct2D 基本影像效果範例</span><span class="sxs-lookup"><span data-stu-id="41227-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="41227-194">內建效果</span><span class="sxs-lookup"><span data-stu-id="41227-194">Built-in Effects</span></span>](built-in-effects.md)