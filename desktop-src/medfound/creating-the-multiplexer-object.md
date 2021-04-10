---
description: 建立多工器物件
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: 建立多工器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191075"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="0abdc-103">建立多工器物件</span><span class="sxs-lookup"><span data-stu-id="0abdc-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="0abdc-104">ASF 多工器是一種 WMContainer 層物件，可與 [ASF 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠為媒體資料流程產生 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="0abdc-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="0abdc-105">多工器物件會公開 [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) 介面。</span><span class="sxs-lookup"><span data-stu-id="0abdc-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="0abdc-106">若要建立多工器，請呼叫 [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="0abdc-107">此函數會傳回空物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0abdc-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="0abdc-108">如果應用程式正在撰寫新的 ASF 檔案，應用程式必須使用 ContentInfo 物件初始化多工器。</span><span class="sxs-lookup"><span data-stu-id="0abdc-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="0abdc-109">若要這樣做，請呼叫 [**IMFASFMultiplexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="0abdc-110">指定的 ContentInfo 物件代表新檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="0abdc-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="0abdc-111">如需有關為新檔案建立及初始化 ContentInfo 物件的詳細資訊，請參閱 [初始化新 ASF 檔案的 ContentInfo 物件](initializing-the-contentinfo-object-of-a-new-asf-file.md)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="0abdc-112">[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會剖析 ContentInfo 物件，以收集資料流程設定資訊，例如資料流程數目、封包大小、預先處理。</span><span class="sxs-lookup"><span data-stu-id="0abdc-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="0abdc-113">（選擇性）多工器也可能需要有漏洞值區參數和承載延伸模組單位。</span><span class="sxs-lookup"><span data-stu-id="0abdc-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="0abdc-114">需要這項資訊，才能產生符合 ASF 標頭物件中所定義之需求的資料封包。</span><span class="sxs-lookup"><span data-stu-id="0abdc-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="0abdc-115">**Initialize** 方法會根據資料流程的媒體類型和設定來設定多工器。</span><span class="sxs-lookup"><span data-stu-id="0abdc-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="0abdc-116">例如，如果資料流程設定為具有承載延伸 (請參閱) [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md) ，然後將多工器設定為將這些值新增至產生的資料封包。</span><span class="sxs-lookup"><span data-stu-id="0abdc-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="0abdc-117">[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法也會取得初始資料物件的控制碼，該物件是建立 ContentInfo 物件以進行寫入時所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="0abdc-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="0abdc-118">產生資料封包時，多工器會將封包新增至資料物件，並適當地加以更新。</span><span class="sxs-lookup"><span data-stu-id="0abdc-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="0abdc-119">當多工器產生所有的資料封包之後，它會更新提供的 ContentInfo 物件，以便更新特定的值，例如資料封包數目。</span><span class="sxs-lookup"><span data-stu-id="0abdc-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="0abdc-120">下列程式碼範例顯示如何建立多工器，並使用 ContentInfo 物件將它初始化。</span><span class="sxs-lookup"><span data-stu-id="0abdc-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="0abdc-121">若要查看完整應用程式中使用的此函式，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。</span><span class="sxs-lookup"><span data-stu-id="0abdc-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="0abdc-122">多工器初始化和有漏洞 Bucket 設定</span><span class="sxs-lookup"><span data-stu-id="0abdc-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="0abdc-123">[**IMFASFMultiplexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會設定多工器，以判斷有漏洞值區資料流程。</span><span class="sxs-lookup"><span data-stu-id="0abdc-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="0abdc-124">若要設定這些參數，請確定已在指定的 ContentInfo 物件上設定下列屬性值。</span><span class="sxs-lookup"><span data-stu-id="0abdc-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="0abdc-125">如需有關設定這些屬性的詳細資訊，請參閱 [設定 ContentInfo 物件中的屬性](setting-properties-in-the-contentinfo-object.md)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="0abdc-126">[**MFPKEY \_ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) 屬性：這表示多工器是否需要自動調整位元速率，以維護有漏洞 bucket 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0abdc-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="0abdc-127">藉由呼叫 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) 並傳遞 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標，應用程式可以變更此設定。</span><span class="sxs-lookup"><span data-stu-id="0abdc-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="0abdc-128">[**MFPKEY \_ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) 屬性： send time 會指出將釋放有漏洞 bucket 內的承載。</span><span class="sxs-lookup"><span data-stu-id="0abdc-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="0abdc-129">傳送時間必須等於或早于呈現時間，因為承載必須有時間才能在呈現時間之前取得目的地。</span><span class="sxs-lookup"><span data-stu-id="0abdc-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="0abdc-130">這個屬性值是第一個傳送時間。</span><span class="sxs-lookup"><span data-stu-id="0abdc-130">This property value is the first send time.</span></span> <span data-ttu-id="0abdc-131">多工器會使用此值來計算後續的傳送時間，以確保資料會穩定地流經值區。</span><span class="sxs-lookup"><span data-stu-id="0abdc-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="0abdc-132">如果已在多工器上設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標，則多工器將會調整位元速率，如此當緩衝區視窗接近已滿時，就會送出承載。</span><span class="sxs-lookup"><span data-stu-id="0abdc-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="0abdc-133">如果未設定旗標，則多工器無法產生資料封包，因為頻寬溢出。</span><span class="sxs-lookup"><span data-stu-id="0abdc-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="0abdc-134">多工器會從與 [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) 方法中指定之 ContentInfo 物件相關聯的 ASF 設定檔取得串流設定資訊。</span><span class="sxs-lookup"><span data-stu-id="0abdc-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="0abdc-135">串流設定資訊包括有漏洞 bucket 參數。</span><span class="sxs-lookup"><span data-stu-id="0abdc-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="0abdc-136">多工器需要此值，才能產生資料封包。</span><span class="sxs-lookup"><span data-stu-id="0abdc-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="0abdc-137">若要指定有漏洞值區參數，請在代表設定檔中之資料流程的串流設定物件上，設定 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="0abdc-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="0abdc-138">若要使用編碼器所使用的緩衝區視窗值，請呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="0abdc-139">只有在設定編碼器的輸出媒體類型之後，才知道實際的緩衝區視窗值。</span><span class="sxs-lookup"><span data-stu-id="0abdc-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="0abdc-140">如需設定輸出媒體類型的相關資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="0abdc-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="0abdc-141">編碼器所使用的有漏洞值區值，在用來建立多工器的 ASF 設定檔所提供的 ContentInfo 物件中可能不同。</span><span class="sxs-lookup"><span data-stu-id="0abdc-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="0abdc-142">[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會更新 ContentInfo 物件，讓正確的值反映在最終的 ASF 標頭物件中。</span><span class="sxs-lookup"><span data-stu-id="0abdc-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0abdc-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="0abdc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0abdc-144">ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="0abdc-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="0abdc-145">產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="0abdc-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
