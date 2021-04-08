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
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>如何將 Direct2D 內容儲存至影像檔案

本主題說明如何使用 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)將 ID2D1Image 形式的內容以 [](/windows/win32/api/d2d1/nn-d2d1-id2d1image)形式儲存至編碼的影像檔案，例如 JPEG。 如果您要撰寫 Windows Store 應用程式，可以讓使用者使用 [**Windows：： Storage：:P ickers：： FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)來選取目的地檔案。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D 效果](effects-overview.md)
-   [**Windows：： Storage：:P ickers：： FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>必要條件

-   您需要一個 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 物件和一個包含 [Direct2D](./direct2d-portal.md) 內容的物件，以執行 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) ，例如 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 或 [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)。

## <a name="instructions"></a>指示

### <a name="step-1-get-a-destination-file-and-stream"></a>步驟1：取得目的地檔案和資料流程

如果您想要讓使用者選取目的地檔案，您可以使用 [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)，開啟傳回的檔案，並取得要搭配 WIC 使用的 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 。

建立 [**Windows：： Storage：:P ickers：： FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) ，並設定影像檔案的參數。 呼叫 [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) 方法。


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



在檔案選擇器非同步作業傳回之後，宣告要執行的完成處理常式。 您可以使用 [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) 方法來取出檔案，以及取得檔案資料流程物件。


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



在檔案上呼叫 [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync)並取得非同步作業的結果，以取得 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) 。


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



最後，使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) 方法來轉換檔案資料流程。 Windows 執行階段 Api 代表 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))的資料流程，而 WIC 會使用 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> 若要使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream)函式，您應該在專案中包含 **shcore。**

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>步驟2：取得 WIC 點陣圖和框架編碼器

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) 和 [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) 提供將映射資料儲存為編碼檔案格式的功能。

建立並初始化編碼器物件。


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



### <a name="step-3-get-an-iwicimageencoder"></a>步驟3：取得 IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) 是 Windows 8 中的新介面。 它可以從 [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)建立，它可延伸 **IWICImagingFactory** ，也是 Windows 8 的新功能。


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



呼叫 [**IWICImagingFactory2：： CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)。 第一個參數是 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) ，而且必須是您要編碼之影像建立所在的裝置–您無法在單一 [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)中混合來自不同資源網域的影像。


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>步驟4：使用 IWICImageEncoder 寫入 Direct2D 內容

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) 可以將 [Direct2D](./direct2d-portal.md) 影像寫入影像框架、框架縮圖或容器縮圖中。 然後，您可以使用 [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) 和 [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) ，以正常方式將映射資料編碼為檔案。

將 [Direct2D](./direct2d-portal.md) 影像寫入框架。 在此程式碼片段中，我們會撰寫包含柵格化 Direct2D 內容的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。 但是，您可以提供任何可執行 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)的介面。


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
> [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)參數必須建立在傳遞至 [**IWICImagingFactory2：： CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)的 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)上。

 

認可 WIC 和 stream 資源，以完成作業。


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
> 某些 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 的執行不會執行 [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) 方法，並傳回 **E \_ >notimpl**。

 

現在您有一個包含 [Direct2D](./direct2d-portal.md) 映射的檔案。

## <a name="complete-example"></a>完整範例

以下是此範例的完整程式碼。

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



 

 