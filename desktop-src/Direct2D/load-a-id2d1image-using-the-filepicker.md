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
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>如何使用 FilePicker 將影像載入 Direct2D 效果

顯示如何使用 [**Windows：： Storage：:P ickers：： FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) 將影像載入 [Direct2D 效果](effects-overview.md)。 如果您想要讓使用者從 Windows Store 應用程式中的儲存體選取影像檔案，建議您使用 [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D 效果](effects-overview.md)
-   [**Windows：： Storage：:P ickers：： FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>必要條件

-   您需要 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 物件來建立效果。
-   您需要用來建立 WIC 物件的 [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) 物件。

## <a name="instructions"></a>指示

### <a name="step-1-open-the-file-picker"></a>步驟1：開啟檔案選擇器

建立 [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) 物件，並設定 *ViewMode*、 *SuggestedStartLocation* 和 *FileTypeFilter* 來選取影像。 呼叫 [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) 方法。


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



[**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync)完成後，您會從它所傳回的 [**iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85))介面取得檔案資料流程。

### <a name="step-2-get-a-file-stream"></a>步驟2：取得檔案資料流程

在檔案選擇器非同步作業傳回之後，宣告要執行的完成處理常式。 您可以使用 [**GetResults**](/previous-versions//br205815(v=vs.85)) 方法來取出檔案，以及取得檔案資料流程物件。


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



在下一個步驟中，您會將 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))物件轉換成可傳遞給 [WIC](/windows/desktop/wic/-wic-api)的 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 。

### <a name="step-3-convert-the-file-stream"></a>步驟3：轉換檔案資料流程

使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) 函式來轉換檔案資料流程。 Windows 執行階段 Api 代表 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))的資料流程，而 [WIC](/windows/desktop/wic/-wic-api) 會使用 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。


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
> 若要使用 [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream)函式，您應該在專案中包含 *shcore。*

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>步驟4：建立 WIC 解碼並取得框架

使用 [**IWICImagingFactory：： CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法來建立 [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder)物件。


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



使用 [**IWICBitmapDecoder：： GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) 方法，從解碼器取得映射的第一個畫面格。


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>步驟5：建立 WIC 轉換器並初始化

使用 [WIC](/windows/desktop/wic/-wic-api)將影像轉換為 BGRA 色彩格式。 [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) 會傳回影像的原生像素格式，例如，jpeg 會儲存在 GUID \_ WICPixelFormat24bppBGR 中。 不過，若要使用 Direct2D 進行效能優化，建議您將轉換成 WICPixelFormat32bppPBGRA。

1.  使用 [**IWICImagingFactory：： CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)方法來建立 [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)物件。

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  初始化格式轉換器，以使用 WICPixelFormat32bppPBGRA 並傳入點陣圖框架。

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

    

[**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)介面衍生自 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)介面，因此您可以將轉換器傳遞給 [點陣圖來源](bitmap-source.md)效果。

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>步驟6：建立效果並傳入 IWICBitmapSource

使用 [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法，以使用 [Direct2D](getting-started-with-direct2d.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)建立 [點陣圖來源](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)物件。

使用 [**ID2D1Effect：： SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法，將 *D2D1 BITMAPSOURCE 屬性 \_ \_ \_ WIC \_ BITMAP BITMAP \_ SOURCE* 屬性設定為 [WIC](/windows/desktop/wic/-wic-api) [**格式轉換器**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)。

> [!Note]  
> [點陣圖來源](bitmap-source.md)效果不會採用 [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput)方法的輸入，例如許多 [Direct2D 效果](effects-overview.md)。 相反地， [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) 物件會指定為屬性。

 


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



現在您已有 [點陣圖來源](bitmap-source.md) 效果，您可以使用它做為任何 [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) 的輸入，並建立效果圖形。

## <a name="complete-example"></a>完整範例

以下是此範例的完整程式碼。


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



 

 