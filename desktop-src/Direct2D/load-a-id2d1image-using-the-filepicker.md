---
title: 如何使用 FilePicker 將影像載入 Direct2D 效果
description: 示範如何使用 Windows 儲存體選擇器 FileOpenPicker 將影像載入 Direct2D 效果。
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346cc0e337374fa41313cb77debf4faca781669
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969110"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a><span data-ttu-id="18a72-105">如何使用 FilePicker 將影像載入 Direct2D 效果</span><span class="sxs-lookup"><span data-stu-id="18a72-105">How to load an image into Direct2D effects using the FilePicker</span></span>

<span data-ttu-id="18a72-106">顯示如何使用 [**Windows：： Storage：:P ickers：： FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) 將影像載入 [Direct2D 效果](effects-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="18a72-106">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="18a72-107">如果您想要讓使用者從 Windows Store 應用程式中的儲存體選取影像檔案，建議您使用 [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)。</span><span class="sxs-lookup"><span data-stu-id="18a72-107">If you want to let the user select an image file from storage in a Windows Store app, we recommend that you use the [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="18a72-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="18a72-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="18a72-109">技術</span><span class="sxs-lookup"><span data-stu-id="18a72-109">Technologies</span></span>

-   [<span data-ttu-id="18a72-110">Direct2D</span><span class="sxs-lookup"><span data-stu-id="18a72-110">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="18a72-111">Direct2D 效果</span><span class="sxs-lookup"><span data-stu-id="18a72-111">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="18a72-112">**Windows：： Storage：:P ickers：： FileOpenPicker**</span><span class="sxs-lookup"><span data-stu-id="18a72-112">**Windows::Storage::Pickers::FileOpenPicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a><span data-ttu-id="18a72-113">必要條件</span><span class="sxs-lookup"><span data-stu-id="18a72-113">Prerequisites</span></span>

-   <span data-ttu-id="18a72-114">您需要 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 物件來建立效果。</span><span class="sxs-lookup"><span data-stu-id="18a72-114">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object for creating effects.</span></span>
-   <span data-ttu-id="18a72-115">您需要用來建立 WIC 物件的 [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) 物件。</span><span class="sxs-lookup"><span data-stu-id="18a72-115">You need an [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) object for creating WIC objects.</span></span>

## <a name="instructions"></a><span data-ttu-id="18a72-116">指示</span><span class="sxs-lookup"><span data-stu-id="18a72-116">Instructions</span></span>

### <a name="step-1-open-the-file-picker"></a><span data-ttu-id="18a72-117">步驟1：開啟檔案選擇器</span><span class="sxs-lookup"><span data-stu-id="18a72-117">Step 1: Open the file picker</span></span>

<span data-ttu-id="18a72-118">建立 [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) 物件，並設定 *ViewMode*、 *SuggestedStartLocation* 和 *FileTypeFilter* 來選取影像。</span><span class="sxs-lookup"><span data-stu-id="18a72-118">Create a [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) object and set the *ViewMode*, *SuggestedStartLocation*, and the *FileTypeFilter* for selecting images.</span></span> <span data-ttu-id="18a72-119">呼叫 [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="18a72-119">Call the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) method.</span></span>


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



<span data-ttu-id="18a72-120">[**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync)完成後，您會從它所傳回的 [**iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85))介面取得檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="18a72-120">After the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) completes, you get a file stream from the [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) interface it returns.</span></span>

### <a name="step-2-get-a-file-stream"></a><span data-ttu-id="18a72-121">步驟2：取得檔案資料流程</span><span class="sxs-lookup"><span data-stu-id="18a72-121">Step 2: Get a file stream</span></span>

<span data-ttu-id="18a72-122">在檔案選擇器非同步作業傳回之後，宣告要執行的完成處理常式。</span><span class="sxs-lookup"><span data-stu-id="18a72-122">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="18a72-123">您可以使用 [**GetResults**](/previous-versions//br205815(v=vs.85)) 方法來取出檔案，以及取得檔案資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="18a72-123">Use the [**GetResults**](/previous-versions//br205815(v=vs.85)) method to retrieve the file and to get the file stream object.</span></span>


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



<span data-ttu-id="18a72-124">在下一個步驟中，您會將 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))物件轉換成可傳遞給 [WIC](/windows/desktop/wic/-wic-api)的 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 。</span><span class="sxs-lookup"><span data-stu-id="18a72-124">In the next step you convert the [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) object to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) that you can pass to [WIC](/windows/desktop/wic/-wic-api).</span></span>

### <a name="step-3-convert-the-file-stream"></a><span data-ttu-id="18a72-125">步驟3：轉換檔案資料流程</span><span class="sxs-lookup"><span data-stu-id="18a72-125">Step 3: Convert the file stream</span></span>

<span data-ttu-id="18a72-126">使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) 函式來轉換檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="18a72-126">Use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function to convert the file stream.</span></span> <span data-ttu-id="18a72-127">Windows 執行階段 Api 代表 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))的資料流程，而 [WIC](/windows/desktop/wic/-wic-api) 會使用 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="18a72-127">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while [WIC](/windows/desktop/wic/-wic-api) consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> <span data-ttu-id="18a72-128">若要使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream)函式，您應該在專案中包含 *shcore。*</span><span class="sxs-lookup"><span data-stu-id="18a72-128">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include *shcore.h* in your project.</span></span>

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a><span data-ttu-id="18a72-129">步驟4：建立 WIC 解碼並取得框架</span><span class="sxs-lookup"><span data-stu-id="18a72-129">Step 4: Create a WIC decoder and get the frame</span></span>

<span data-ttu-id="18a72-130">使用 [**IWICImagingFactory：： CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法來建立 [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder)物件。</span><span class="sxs-lookup"><span data-stu-id="18a72-130">Create an [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object using the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



<span data-ttu-id="18a72-131">使用 [**IWICBitmapDecoder：： GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) 方法，從解碼器取得映射的第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="18a72-131">Get the first frame of the image from the decoder using the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a><span data-ttu-id="18a72-132">步驟5：建立 WIC 轉換器並初始化</span><span class="sxs-lookup"><span data-stu-id="18a72-132">Step 5: Create a WIC converter and initialize</span></span>

<span data-ttu-id="18a72-133">使用 [WIC](/windows/desktop/wic/-wic-api)將影像轉換為 BGRA 色彩格式。</span><span class="sxs-lookup"><span data-stu-id="18a72-133">Convert the image to the BGRA color format using [WIC](/windows/desktop/wic/-wic-api).</span></span> <span data-ttu-id="18a72-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) 會傳回影像的原生像素格式，例如，jpeg 會儲存在 GUID \_ WICPixelFormat24bppBGR 中。</span><span class="sxs-lookup"><span data-stu-id="18a72-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) will return the native pixel format of the image, like JPEGs are stored in GUID\_WICPixelFormat24bppBGR.</span></span> <span data-ttu-id="18a72-135">不過，若要使用 Direct2D 進行效能優化，建議您將轉換成 WICPixelFormat32bppPBGRA。</span><span class="sxs-lookup"><span data-stu-id="18a72-135">However, as a performance optimization with Direct2D we recommend that you convert to WICPixelFormat32bppPBGRA.</span></span>

1.  <span data-ttu-id="18a72-136">使用 [**IWICImagingFactory：： CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)方法來建立 [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)物件。</span><span class="sxs-lookup"><span data-stu-id="18a72-136">Create a [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) object using the [**IWICImagingFactory::CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  <span data-ttu-id="18a72-137">初始化格式轉換器，以使用 WICPixelFormat32bppPBGRA 並傳入點陣圖框架。</span><span class="sxs-lookup"><span data-stu-id="18a72-137">Initialize the format converter to use the WICPixelFormat32bppPBGRA and pass in the bitmap frame.</span></span>

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

<span data-ttu-id="18a72-138">[**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)介面衍生自 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)介面，因此您可以將轉換器傳遞給 [點陣圖來源](bitmap-source.md)效果。</span><span class="sxs-lookup"><span data-stu-id="18a72-138">The [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) interface is derived from the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) interface, so you can pass the converter to the [bitmap source](bitmap-source.md) effect.</span></span>

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a><span data-ttu-id="18a72-139">步驟6：建立效果並傳入 IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="18a72-139">Step 6: Create effect and pass in an IWICBitmapSource</span></span>

<span data-ttu-id="18a72-140">使用 [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法，以使用 [Direct2D](getting-started-with-direct2d.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)建立 [點陣圖來源](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)物件。</span><span class="sxs-lookup"><span data-stu-id="18a72-140">Use the [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method to create a [bitmap source](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object using the [Direct2D](getting-started-with-direct2d.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span>

<span data-ttu-id="18a72-141">使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法，將 *D2D1 BITMAPSOURCE 屬性 \_ \_ \_ WIC \_ BITMAP BITMAP \_ SOURCE* 屬性設定為 [WIC](/windows/desktop/wic/-wic-api) [**格式轉換器**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)。</span><span class="sxs-lookup"><span data-stu-id="18a72-141">Use the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method to set the *D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE* property to the [WIC](/windows/desktop/wic/-wic-api) [**format converter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).</span></span>

> [!Note]  
> <span data-ttu-id="18a72-142">[點陣圖來源](bitmap-source.md)效果不會採用 [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput)方法的輸入，例如許多 [Direct2D 效果](effects-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="18a72-142">The [bitmap source](bitmap-source.md) effect doesn't take an input from the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method like many [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="18a72-143">相反地， [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) 物件會指定為屬性。</span><span class="sxs-lookup"><span data-stu-id="18a72-143">Instead, the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) object is specified as a property.</span></span>

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



<span data-ttu-id="18a72-144">現在您已有 [點陣圖來源](bitmap-source.md) 效果，您可以使用它做為任何 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 的輸入，並建立效果圖形。</span><span class="sxs-lookup"><span data-stu-id="18a72-144">Now that you have the [bitmap source](bitmap-source.md) effect, you can use it as input to any [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) and create an effect graph.</span></span>

## <a name="complete-example"></a><span data-ttu-id="18a72-145">完整範例</span><span class="sxs-lookup"><span data-stu-id="18a72-145">Complete example</span></span>

<span data-ttu-id="18a72-146">以下是此範例的完整程式碼。</span><span class="sxs-lookup"><span data-stu-id="18a72-146">Here is the full code for this example.</span></span>


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 