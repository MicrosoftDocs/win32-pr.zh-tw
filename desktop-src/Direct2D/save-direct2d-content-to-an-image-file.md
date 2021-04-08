---
title: 如何將 Direct2D 內容儲存至影像檔案
description: 本主題說明如何使用 IWICImageEncoder 將 ID2D1Image 形式的內容以形式儲存至編碼的影像檔案，例如 JPEG。
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842387"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="4d6fe-103">如何將 Direct2D 內容儲存至影像檔案</span><span class="sxs-lookup"><span data-stu-id="4d6fe-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="4d6fe-104">本主題說明如何使用 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)將 ID2D1Image 形式的內容以 [](/windows/win32/api/d2d1/nn-d2d1-id2d1image)形式儲存至編碼的影像檔案，例如 JPEG。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="4d6fe-105">如果您要撰寫 Windows Store 應用程式，可以讓使用者使用 [**Windows：： Storage：:P ickers：： FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)來選取目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4d6fe-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="4d6fe-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4d6fe-107">技術</span><span class="sxs-lookup"><span data-stu-id="4d6fe-107">Technologies</span></span>

-   [<span data-ttu-id="4d6fe-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4d6fe-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="4d6fe-109">Direct2D 效果</span><span class="sxs-lookup"><span data-stu-id="4d6fe-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="4d6fe-110">**Windows：： Storage：:P ickers：： FileSavePicker**</span><span class="sxs-lookup"><span data-stu-id="4d6fe-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="4d6fe-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="4d6fe-111">Prerequisites</span></span>

-   <span data-ttu-id="4d6fe-112">您需要一個 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 物件和一個包含 [Direct2D](./direct2d-portal.md) 內容的物件，以執行 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) ，例如 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 或 [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="4d6fe-113">指示</span><span class="sxs-lookup"><span data-stu-id="4d6fe-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="4d6fe-114">步驟1：取得目的地檔案和資料流程</span><span class="sxs-lookup"><span data-stu-id="4d6fe-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="4d6fe-115">如果您想要讓使用者選取目的地檔案，您可以使用 [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)，開啟傳回的檔案，並取得要搭配 WIC 使用的 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="4d6fe-116">建立 [**Windows：： Storage：:P ickers：： FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) ，並設定影像檔案的參數。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="4d6fe-117">呼叫 [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



<span data-ttu-id="4d6fe-118">在檔案選擇器非同步作業傳回之後，宣告要執行的完成處理常式。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="4d6fe-119">您可以使用 [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) 方法來取出檔案，以及取得檔案資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



<span data-ttu-id="4d6fe-120">在檔案上呼叫 [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync)並取得非同步作業的結果，以取得 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="4d6fe-121">最後，使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) 方法來轉換檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="4d6fe-122">Windows 執行階段 Api 代表 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))的資料流程，而 WIC 會使用 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="4d6fe-123">若要使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream)函式，您應該在專案中包含 **shcore。**</span><span class="sxs-lookup"><span data-stu-id="4d6fe-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="4d6fe-124">步驟2：取得 WIC 點陣圖和框架編碼器</span><span class="sxs-lookup"><span data-stu-id="4d6fe-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="4d6fe-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) 和 [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) 提供將映射資料儲存為編碼檔案格式的功能。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="4d6fe-126">建立並初始化編碼器物件。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-126">Create and initialize the encoder objects.</span></span>


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="4d6fe-127">步驟3：取得 IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="4d6fe-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="4d6fe-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) 是 Windows 8 中的新介面。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="4d6fe-129">它可以從 [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)建立，它可延伸 **IWICImagingFactory** ，也是 Windows 8 的新功能。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



<span data-ttu-id="4d6fe-130">呼叫 [**IWICImagingFactory2：： CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="4d6fe-131">第一個參數是 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) ，而且必須是您要編碼之影像建立所在的裝置–您無法在單一 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)中混合來自不同資源網域的影像。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="4d6fe-132">步驟4：使用 IWICImageEncoder 寫入 Direct2D 內容</span><span class="sxs-lookup"><span data-stu-id="4d6fe-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="4d6fe-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) 可以將 [Direct2D](./direct2d-portal.md) 影像寫入影像框架、框架縮圖或容器縮圖中。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="4d6fe-134">然後，您可以使用 [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) 和 [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) ，以正常方式將映射資料編碼為檔案。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="4d6fe-135">將 [Direct2D](./direct2d-portal.md) 影像寫入框架。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="4d6fe-136">在此程式碼片段中，我們會撰寫包含柵格化 Direct2D 內容的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="4d6fe-137">但是，您可以提供任何可執行 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)的介面。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> <span data-ttu-id="4d6fe-138">[**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)參數必須建立在傳遞至 [**IWICImagingFactory2：： CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)的 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)上。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="4d6fe-139">認可 WIC 和 stream 資源，以完成作業。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-139">Commit the WIC and stream resources to finalize the operation.</span></span>


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> <span data-ttu-id="4d6fe-140">某些 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 的執行不會執行 [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) 方法，並傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="4d6fe-141">現在您有一個包含 [Direct2D](./direct2d-portal.md) 映射的檔案。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="4d6fe-142">完整範例</span><span class="sxs-lookup"><span data-stu-id="4d6fe-142">Complete example</span></span>

<span data-ttu-id="4d6fe-143">以下是此範例的完整程式碼。</span><span class="sxs-lookup"><span data-stu-id="4d6fe-143">Here the full code for this example.</span></span>

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 