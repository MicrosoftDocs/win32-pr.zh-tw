---
description: 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。 瞭解如何使用 CoCreateInstance 建立編碼器。
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: 使用 CoCreateInstance 建立編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068464"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="2f26e-104">使用 CoCreateInstance 建立編碼器</span><span class="sxs-lookup"><span data-stu-id="2f26e-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="2f26e-105">若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。</span><span class="sxs-lookup"><span data-stu-id="2f26e-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="2f26e-106">若要使用這些編碼器，必須向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="2f26e-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="2f26e-107">編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 且必須公開 IMFTransform 介面。</span><span class="sxs-lookup"><span data-stu-id="2f26e-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="2f26e-108">本主題說明應用程式如何取得所需的 MFT 編碼器 IMFTransform 介面的指標，並將其具現化以供使用。</span><span class="sxs-lookup"><span data-stu-id="2f26e-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="2f26e-109">如需編碼器註冊的相關資訊，請參閱具現 [化編碼器 MFT](instantiating-the-encoder-mft.md)。</span><span class="sxs-lookup"><span data-stu-id="2f26e-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="2f26e-110">使用編碼器的 IMFTransform 介面</span><span class="sxs-lookup"><span data-stu-id="2f26e-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="2f26e-111">編碼器建立範例</span><span class="sxs-lookup"><span data-stu-id="2f26e-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="2f26e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f26e-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="2f26e-113">使用編碼器的 IMFTransform 介面</span><span class="sxs-lookup"><span data-stu-id="2f26e-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="2f26e-114">在成功向系統註冊 Windows Media 編碼器之後，應用程式可以藉由呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)來列舉編碼器。</span><span class="sxs-lookup"><span data-stu-id="2f26e-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="2f26e-115">若要搜尋正確的編碼器，您必須指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="2f26e-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="2f26e-116">代表分類的 GUID，也就是 **mft \_ 類別 \_ 音訊 \_ 編碼器** 或 **mft 類別的 \_ \_ 影片 \_ 編碼器**。</span><span class="sxs-lookup"><span data-stu-id="2f26e-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="2f26e-117">要比對的格式。</span><span class="sxs-lookup"><span data-stu-id="2f26e-117">The format to match.</span></span> <span data-ttu-id="2f26e-118">這是設定在 [**MFT 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構中，指定編碼器將在其中產生範例之媒體類型的主要類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="2f26e-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="2f26e-119">此結構會在 *pOutputType* 參數中傳遞。</span><span class="sxs-lookup"><span data-stu-id="2f26e-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="2f26e-120">如需支援類型的詳細資訊，請參閱 [媒體類型 guid](media-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="2f26e-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="2f26e-121">*PInputType* 參數中的輸入類型資訊不是必要的。</span><span class="sxs-lookup"><span data-stu-id="2f26e-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="2f26e-122">這是因為應用程式知道輸入型別，而編碼器預期輸入資料流程的格式不是壓縮。</span><span class="sxs-lookup"><span data-stu-id="2f26e-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="2f26e-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 會傳回符合搜尋準則之編碼器 MFTs 的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標陣列。</span><span class="sxs-lookup"><span data-stu-id="2f26e-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="2f26e-124">您可以呼叫 COM 函式 **CoCreateInstance** 來具現化編碼器，並傳遞您要使用之編碼器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="2f26e-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="2f26e-125">此函式會傳回代表編碼器之 **IMFTransform** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2f26e-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="2f26e-126">如需此函式呼叫的詳細資訊，請參閱 (COM) 的元件物件模型 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="2f26e-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="2f26e-127">編碼器建立範例</span><span class="sxs-lookup"><span data-stu-id="2f26e-127">Encoder Creation Example</span></span>

<span data-ttu-id="2f26e-128">下列程式碼範例顯示如何建立音訊或影片編碼器。</span><span class="sxs-lookup"><span data-stu-id="2f26e-128">The following code example shows how to create an audio or video encoder.</span></span>


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2f26e-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f26e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f26e-130">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="2f26e-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="2f26e-131">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="2f26e-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



