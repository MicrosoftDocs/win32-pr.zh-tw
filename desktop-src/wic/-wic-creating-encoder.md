---
description: 編碼器會將影像資料寫入資料流程。 編碼器可以在將影像圖元寫入串流之前，以數種方式壓縮、加密和更改影像圖元。
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: 編碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549483"
---
# <a name="encoding-overview"></a><span data-ttu-id="ff149-104">編碼總覽</span><span class="sxs-lookup"><span data-stu-id="ff149-104">Encoding Overview</span></span>

<span data-ttu-id="ff149-105">編碼器會將影像資料寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="ff149-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="ff149-106">編碼器可以在將影像圖元寫入串流之前，以數種方式壓縮、加密和更改影像圖元。</span><span class="sxs-lookup"><span data-stu-id="ff149-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="ff149-107">使用某些編碼器會產生取捨，例如，JPEG 會以較佳的方式來交易色彩資訊以提升壓縮。</span><span class="sxs-lookup"><span data-stu-id="ff149-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="ff149-108">其他編碼器不會造成這類遺失，例如點陣圖 (BMP) 。</span><span class="sxs-lookup"><span data-stu-id="ff149-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="ff149-109">因為許多編解碼器使用專屬技術來達到更佳的壓縮和影像精確度，所以如何編碼影像的詳細資料是由編解碼器開發人員所組成。</span><span class="sxs-lookup"><span data-stu-id="ff149-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="ff149-110">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ff149-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="ff149-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ff149-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="ff149-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ff149-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="ff149-113">TIFF 編碼範例</span><span class="sxs-lookup"><span data-stu-id="ff149-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="ff149-114">編碼器選項使用方式</span><span class="sxs-lookup"><span data-stu-id="ff149-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="ff149-115">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="ff149-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="ff149-116">編碼器選項範例</span><span class="sxs-lookup"><span data-stu-id="ff149-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="ff149-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff149-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="ff149-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ff149-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="ff149-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 是將影像編碼為目標格式的主要介面，用來將影像的元件（例如縮圖 ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) 和框架 ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)) ）序列化至影像檔案。</span><span class="sxs-lookup"><span data-stu-id="ff149-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="ff149-120">序列化程式的運作方式和時機，會留給編解碼器開發人員。</span><span class="sxs-lookup"><span data-stu-id="ff149-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="ff149-121">目的檔案格式內的每個資料區塊都應該能夠獨立于順序以外的設定，但同樣地，這是編解碼器開發人員的決策。</span><span class="sxs-lookup"><span data-stu-id="ff149-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="ff149-122">不過，一旦呼叫 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) 方法之後，就不應該允許變更影像，而且應該關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="ff149-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="ff149-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ff149-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="ff149-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 是用於編碼影像個別框架的介面。</span><span class="sxs-lookup"><span data-stu-id="ff149-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="ff149-125">它提供了設定個別框架影像處理元件的方法，例如縮圖和框架，以及影像尺寸、DPI 和像素格式。</span><span class="sxs-lookup"><span data-stu-id="ff149-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="ff149-126">個別的框架可以使用框架專屬的中繼資料進行編碼，讓 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 透過 [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 方法提供中繼資料寫入器的存取權。</span><span class="sxs-lookup"><span data-stu-id="ff149-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="ff149-127">框架的 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 方法會認可個別畫面格的所有變更，並指出該框架的變更應該不會再被接受。</span><span class="sxs-lookup"><span data-stu-id="ff149-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="ff149-128">TIFF 編碼範例</span><span class="sxs-lookup"><span data-stu-id="ff149-128">TIFF Encoding Example</span></span>

<span data-ttu-id="ff149-129">在下列範例中，標記的影像檔案格式 (TIFF) 影像是使用 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)進行編碼。</span><span class="sxs-lookup"><span data-stu-id="ff149-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="ff149-130">TIFF 輸出是使用 [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) 自訂的，而點陣圖框架則是使用指定的選項來初始化。</span><span class="sxs-lookup"><span data-stu-id="ff149-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="ff149-131">使用 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)建立映射之後，就會使用 [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 認可框架，然後使用 [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)來儲存映射。</span><span class="sxs-lookup"><span data-stu-id="ff149-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="ff149-132">編碼器選項使用方式</span><span class="sxs-lookup"><span data-stu-id="ff149-132">Encoder Options Usage</span></span>

<span data-ttu-id="ff149-133">不同格式的不同編碼器需要針對影像的編碼方式公開不同的選項。</span><span class="sxs-lookup"><span data-stu-id="ff149-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="ff149-134">Windows 影像處理元件 (WIC) 提供一致的機制，用來表示是否需要編碼選項，同時仍然讓應用程式使用多個編碼器，而不需要特定格式的知識。</span><span class="sxs-lookup"><span data-stu-id="ff149-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="ff149-135">這是藉由在 [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)方法和 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)方法上提供 [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)參數來完成。</span><span class="sxs-lookup"><span data-stu-id="ff149-135">This is accomplished by providing an [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="ff149-136">元件 factory 提供建立編碼器選項屬性包的簡單建立點。</span><span class="sxs-lookup"><span data-stu-id="ff149-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="ff149-137">如果用戶端需要提供簡單、直覺且不衝突的編碼器選項群組合，則編解碼器可以使用此服務。</span><span class="sxs-lookup"><span data-stu-id="ff149-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="ff149-138">您必須在建立時使用與該編解碼器相關的所有編碼器選項來初始化映射屬性包。</span><span class="sxs-lookup"><span data-stu-id="ff149-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="ff149-139">針對標準集中的編碼器選項，值範圍會在寫入時強制執行。</span><span class="sxs-lookup"><span data-stu-id="ff149-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="ff149-140">為了更先進的需要，編解碼器應該撰寫自己的屬性包執行。</span><span class="sxs-lookup"><span data-stu-id="ff149-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="ff149-141">應用程式會在畫面格建立期間提供編碼器選項包，並且必須在初始化編碼器框架之前設定任何值。</span><span class="sxs-lookup"><span data-stu-id="ff149-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="ff149-142">針對 UI 導向的應用程式，它可以為標準編碼器選項提供固定的 UI，並針對剩餘的選項提供先進的觀點。</span><span class="sxs-lookup"><span data-stu-id="ff149-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="ff149-143">您可以透過 Write 方法一次建立一個變更，任何錯誤都會透過 IErrorLog 回報。</span><span class="sxs-lookup"><span data-stu-id="ff149-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="ff149-144">變更後，UI 應用程式應該一律重新讀取並顯示所有選項，以防變更造成 cascade 效果。</span><span class="sxs-lookup"><span data-stu-id="ff149-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="ff149-145">應用程式應該準備好處理編解碼器的失敗畫面格初始化，只透過其屬性包提供基本的錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="ff149-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="ff149-146">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="ff149-146">Encoder Options</span></span>

<span data-ttu-id="ff149-147">應用程式可能預期會遇到下列一組編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="ff149-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="ff149-148">編碼器選項反映編碼器和基礎容器格式的功能，因此其本質並不是與編解碼器無關。</span><span class="sxs-lookup"><span data-stu-id="ff149-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="ff149-149">可能的話，應該將新選項正規化，以便將它們套用至出現的新編解碼器。</span><span class="sxs-lookup"><span data-stu-id="ff149-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="ff149-150">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ff149-150">Property Name</span></span>      | <span data-ttu-id="ff149-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ff149-151">VARTYPE</span></span>  | <span data-ttu-id="ff149-152">值</span><span class="sxs-lookup"><span data-stu-id="ff149-152">Value</span></span>                                                                     | <span data-ttu-id="ff149-153">適用的編解碼器</span><span class="sxs-lookup"><span data-stu-id="ff149-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="ff149-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="ff149-154">ImageQuality</span></span>       | <span data-ttu-id="ff149-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="ff149-155">VT\_R4</span></span>   | <span data-ttu-id="ff149-156">0-1。0</span><span class="sxs-lookup"><span data-stu-id="ff149-156">0-1.0</span></span>                                                                     | <span data-ttu-id="ff149-157">JPEG、HDPhoto</span><span class="sxs-lookup"><span data-stu-id="ff149-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="ff149-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="ff149-158">CompressionQuality</span></span> | <span data-ttu-id="ff149-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="ff149-159">VT\_R4</span></span>   | <span data-ttu-id="ff149-160">0-1。0</span><span class="sxs-lookup"><span data-stu-id="ff149-160">0-1.0</span></span>                                                                     | <span data-ttu-id="ff149-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="ff149-161">TIFF</span></span>              |
| <span data-ttu-id="ff149-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="ff149-162">Lossless</span></span>           | <span data-ttu-id="ff149-163">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ff149-163">VT\_BOOL</span></span> | <span data-ttu-id="ff149-164">**TRUE**， **FALSE**</span><span class="sxs-lookup"><span data-stu-id="ff149-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="ff149-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="ff149-165">HDPhoto</span></span>           |
| <span data-ttu-id="ff149-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="ff149-166">BitmapTransform</span></span>    | <span data-ttu-id="ff149-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="ff149-167">VT\_UI1</span></span>  | [<span data-ttu-id="ff149-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="ff149-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="ff149-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="ff149-169">JPEG</span></span>              |



 

<span data-ttu-id="ff149-170">0.0 的 ImageQualty 表示最小的精確度轉譯和1.0 表示最高的精確度，這也可能表示因編解碼器而異。</span><span class="sxs-lookup"><span data-stu-id="ff149-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="ff149-171">CompressionQuality 0.0 表示最有效率的壓縮配置，通常會產生快速編碼但較大的輸出。</span><span class="sxs-lookup"><span data-stu-id="ff149-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="ff149-172">值為1.0 表示最有效率的可用配置，通常需要更多時間進行編碼，但產生較小的輸出。</span><span class="sxs-lookup"><span data-stu-id="ff149-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="ff149-173">視編解碼器的功能而定，此範圍可能會對應到一組不同的可用壓縮方法。</span><span class="sxs-lookup"><span data-stu-id="ff149-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="ff149-174">無失真表示編解碼器會將影像編碼為無失真，而不會遺失影像資料。</span><span class="sxs-lookup"><span data-stu-id="ff149-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="ff149-175">如果已啟用無損，則會忽略 ImageQuality。</span><span class="sxs-lookup"><span data-stu-id="ff149-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="ff149-176">除了上述的一般編碼器選項以外，WIC 提供的編解碼器也支援下列選項。</span><span class="sxs-lookup"><span data-stu-id="ff149-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="ff149-177">如果編解碼器必須支援與這些提供的編解碼器使用方式一致的選項，則建議您這樣做。</span><span class="sxs-lookup"><span data-stu-id="ff149-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="ff149-178">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ff149-178">Property Name</span></span>           | <span data-ttu-id="ff149-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ff149-179">VARTYPE</span></span>           | <span data-ttu-id="ff149-180">值</span><span class="sxs-lookup"><span data-stu-id="ff149-180">Value</span></span>                                                                             | <span data-ttu-id="ff149-181">適用的編解碼器</span><span class="sxs-lookup"><span data-stu-id="ff149-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="ff149-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="ff149-182">InterlaceOption</span></span>         | <span data-ttu-id="ff149-183">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ff149-183">VT\_BOOL</span></span>          | <span data-ttu-id="ff149-184">開啟/關閉</span><span class="sxs-lookup"><span data-stu-id="ff149-184">On/Off</span></span>                                                                            | <span data-ttu-id="ff149-185">PNG</span><span class="sxs-lookup"><span data-stu-id="ff149-185">PNG</span></span>               |
| <span data-ttu-id="ff149-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="ff149-186">FilterOption</span></span>            | <span data-ttu-id="ff149-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="ff149-187">VT\_UI1</span></span>           | [<span data-ttu-id="ff149-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="ff149-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="ff149-189">PNG</span><span class="sxs-lookup"><span data-stu-id="ff149-189">PNG</span></span>               |
| <span data-ttu-id="ff149-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="ff149-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="ff149-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="ff149-191">VT\_UI1</span></span>           | [<span data-ttu-id="ff149-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="ff149-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="ff149-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="ff149-193">TIFF</span></span>              |
| <span data-ttu-id="ff149-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="ff149-194">Luminance</span></span>               | <span data-ttu-id="ff149-195">VT \_ UI4/vt \_ 陣列</span><span class="sxs-lookup"><span data-stu-id="ff149-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="ff149-196">64專案 (DCT) </span><span class="sxs-lookup"><span data-stu-id="ff149-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="ff149-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="ff149-197">JPEG</span></span>              |
| <span data-ttu-id="ff149-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="ff149-198">Chrominance</span></span>             | <span data-ttu-id="ff149-199">VT \_ UI4/vt \_ 陣列</span><span class="sxs-lookup"><span data-stu-id="ff149-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="ff149-200">64專案 (DCT) </span><span class="sxs-lookup"><span data-stu-id="ff149-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="ff149-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="ff149-201">JPEG</span></span>              |
| <span data-ttu-id="ff149-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="ff149-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="ff149-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="ff149-203">VT\_UI1</span></span>           | [<span data-ttu-id="ff149-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="ff149-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="ff149-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="ff149-205">JPEG</span></span>              |
| <span data-ttu-id="ff149-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="ff149-206">SuppressApp0</span></span>            | <span data-ttu-id="ff149-207">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ff149-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="ff149-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="ff149-208">JPEG</span></span>              |
| <span data-ttu-id="ff149-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="ff149-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="ff149-210">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ff149-210">VT\_BOOL</span></span>          | <span data-ttu-id="ff149-211">開啟/關閉</span><span class="sxs-lookup"><span data-stu-id="ff149-211">On/Off</span></span>                                                                            | <span data-ttu-id="ff149-212">BMP</span><span class="sxs-lookup"><span data-stu-id="ff149-212">BMP</span></span>               |



 

<span data-ttu-id="ff149-213">使用 **VT \_ EMPTY** 表示 **\* \* 未設定** 為預設值。</span><span class="sxs-lookup"><span data-stu-id="ff149-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="ff149-214">如果已設定其他屬性，但不支援這些屬性，則編碼器應忽略它們;如果應用程式想要有可能存在或可能不存在的功能，這可讓應用程式以較少的邏輯編寫程式碼。</span><span class="sxs-lookup"><span data-stu-id="ff149-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="ff149-215">編碼器選項範例</span><span class="sxs-lookup"><span data-stu-id="ff149-215">Encoder Options Examples</span></span>

<span data-ttu-id="ff149-216">在上述的 [TIFF 編碼範例](#tiff-encoding-example) 中，已設定特定的編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="ff149-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="ff149-217">PROPBAG2 結構的 *pstrName* 成員會設定為適當的屬性名稱，而 VARIANT 會設定為對應的 VARTYPE 和所需的值，在此例中是 [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="ff149-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="ff149-218">若要使用預設編碼器選項，只要使用建立框架時傳回的屬性包來初始化點陣圖框架。</span><span class="sxs-lookup"><span data-stu-id="ff149-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="ff149-219">如果未考慮任何編碼器選項，也可以消除屬性包。</span><span class="sxs-lookup"><span data-stu-id="ff149-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ff149-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff149-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff149-221">**概念**</span><span class="sxs-lookup"><span data-stu-id="ff149-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff149-222">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ff149-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ff149-223">解碼總覽</span><span class="sxs-lookup"><span data-stu-id="ff149-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="ff149-224">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="ff149-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ff149-225">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ff149-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
