---
description: 下列範例示範如何將影像和其中繼資料重新編碼為相同格式的新檔案。
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: 如何使用中繼資料重新編碼 JPEG 影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13851af04c6af742dbc68acc31fd674c3602ebeb16bec6903a3570f8cb1e0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088160"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>如何使用中繼資料重新編碼 JPEG 影像

下列範例示範如何將影像和其中繼資料重新編碼為相同格式的新檔案。 此外，這個範例會加入中繼資料來示範查詢寫入器所使用的單一專案運算式。

本主題包含下列各節。

-   [必要條件](#prerequisites)
-   [第1部分：將影像解碼](#part-1-decode-an-image)
-   [第2部分：建立和初始化影像編碼器](#part-2-create-and-initialize-the-image-encoder)
-   [第3部分：複製已解碼的框架資訊](#part-3-copy-decoded-frame-information)
-   [第4部分：複製中繼資料](#part-4-copy-the-metadata)
-   [第5部分：新增額外的中繼資料](#part-5-add-additional-metadata)
-   [第6部分：完成編碼的影像](#part-6-finalize-the-encoded-image)
-   [JPEG 重新編碼範例程式碼](#jpeg-re-encode-example-code)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該熟悉[wic 中繼資料總覽](-wic-about-metadata.md)中所述的 Windows 影像處理元件 (wic) 中繼資料系統。 您也應該熟悉 WIC 編解碼器元件，如[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)中所述。

## <a name="part-1-decode-an-image"></a>第1部分：將影像解碼

在您可以將影像資料或中繼資料複製到新的影像檔案之前，您必須先為要重新編碼的現有映射建立一個解碼器。 下列程式碼示範如何為影像檔案 test.jpg 建立 WIC 解碼器。


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



對 **CreateDecoderFromFilename** 的呼叫會使用 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 列舉中 WICDecodeMetadataCacheOnDemand 的值做為第四個參數。 這會告知解碼器在需要中繼資料時快取中繼資料，方法是取得查詢讀取器，或使用基礎中繼資料讀取器。 使用這個選項可讓您將資料流程保留在中繼資料中，這是執行快速中繼資料編碼的必要項，並且可讓 JPEG 影像進行不失真的解碼和編碼。 或者，您可以使用其他 **WICDecodeOptions** 值 WICDecodeMetadataCacheOnLoad，這會在載入映射時立即快取內嵌影像中繼資料。

## <a name="part-2-create-and-initialize-the-image-encoder"></a>第2部分：建立和初始化影像編碼器

下列程式碼示範如何建立您將用來編碼先前解碼之影像的編碼器。


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



建立並初始化 WIC 檔案資料流程 piFileStream，以寫入影像檔案 "test2.jpg"。 接著會使用 piFileStream 來初始化編碼器，並通知編碼器在編碼完成時寫入影像位的位置。

## <a name="part-3-copy-decoded-frame-information"></a>第3部分：複製已解碼的框架資訊

下列程式碼會將影像的每個畫面格複製到編碼器的新畫面。 此複本包含大小、解析度和像素格式;所有這些都是建立有效框架的必要項。

> [!Note]  
> JPEG 影像只會有一個畫面格，而且下面的迴圈並不是必要的，但也會納入以示範支援它之格式的多重畫面使用方式。

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



下列程式碼會執行快速檢查，以判斷來源和目的地影像格式是否相同。 這是必要的，因為第4部分所顯示的作業只有在來源和目的地格式相同時才受支援。


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>第4部分：複製中繼資料

> [!Note]  
> 此區段中的程式碼只有在來源和目的影像格式相同時才有效。 編碼為不同的影像格式時，無法在單一作業中複製映射的所有中繼資料。

 

若要在將影像重新編碼為相同的影像格式時保留中繼資料，有方法可在單一作業中複製所有中繼資料。 這些作業都遵循類似的模式;每個都會將已解碼的框架中繼資料直接設定為所編碼的新框架。 請注意，這是針對每個個別的影像框架進行的。

複製中繼資料的慣用方法是使用已解碼框架的區塊讀取器來初始化新框架的區塊寫入器。 下列程式碼示範這個方法。


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



在此範例中，您只需從來源畫面格和目的框架分別取得區塊讀取器和封鎖寫入器。 區塊寫入器接著會從封鎖讀取器初始化。 這會以封鎖讀取器預先填入的中繼資料初始化區塊寫入器。 若要瞭解複製中繼資料的其他方法，請參閱 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)中的寫入中繼資料一節。

同樣地，此作業只適用于來源和目的映射具有相同的格式時。 這是因為不同的影像格式會將中繼資料區塊儲存在不同的位置。 例如，JPEG 和標記的影像檔案格式 (TIFF) 支援可延伸的中繼資料平臺 (XMP) 中繼資料區塊。 在 JPEG 影像中，XMP 區塊位於「 [WIC 中繼資料」總覽](-wic-about-metadata.md)中所述的根中繼資料區塊。 不過，在 TIFF 影像中，XMP 區塊內嵌于根的 IFD 區塊中。

## <a name="part-5-add-additional-metadata"></a>第5部分：新增額外的中繼資料

下列範例示範如何將中繼資料新增至目的映射。 這是藉由使用查詢運算式和儲存在 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)中的資料呼叫查詢寫入器的 **SetMetadataByName** 方法來完成。


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



如需查詢運算式的詳細資訊，請參閱 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)。

## <a name="part-6-finalize-the-encoded-image"></a>第6部分：完成編碼的影像

複製映射的最後步驟是撰寫框架的圖元資料、將畫面格認可至編碼器，以及認可編碼器。 認可編碼器會將影像串流寫入檔案。


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



框架的 **WriteSource** 方法是用來寫入影像的圖元資料。 請注意，這是在寫入中繼資料之後完成的。 這是必要的，以確保中繼資料在影像檔案內有足夠的空間。 寫入圖元資料之後，會使用框架的 **Commit** 方法將框架寫入資料流程。 處理完所有框架之後，編碼器 (，因此會使用編碼器的 **Commit** 方法來完成映射) 。

認可框架之後，您必須釋放在迴圈中建立的 COM 物件。

## <a name="jpeg-re-encode-example-code"></a>JPEG 重新編碼範例程式碼

以下是一個 convienient 區塊中第1到6部分的程式碼。


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[中繼資料擴充性總覽](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
