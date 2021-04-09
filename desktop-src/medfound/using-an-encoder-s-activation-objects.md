---
description: 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。 若要使用這些編碼器，必須向系統註冊。
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: 使用編碼器啟用物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848699"
---
# <a name="using-an-encoders-activation-objects"></a><span data-ttu-id="bfff0-104">使用編碼器的啟用物件</span><span class="sxs-lookup"><span data-stu-id="bfff0-104">Using an Encoder's Activation Objects</span></span>

<span data-ttu-id="bfff0-105">若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。</span><span class="sxs-lookup"><span data-stu-id="bfff0-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="bfff0-106">若要使用這些編碼器，必須向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="bfff0-106">To use these encoders, they must be registered with the system.</span></span>

<span data-ttu-id="bfff0-107">如需編碼器註冊的相關資訊，請參閱具現 [化編碼器 MFT](instantiating-the-encoder-mft.md)。</span><span class="sxs-lookup"><span data-stu-id="bfff0-107">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="bfff0-108">使用編碼器的啟用物件</span><span class="sxs-lookup"><span data-stu-id="bfff0-108">Using an Encoder's Activation Objects</span></span>](#using-an-encoders-activation-objects)
-   [<span data-ttu-id="bfff0-109">Windows 7 和更新版本中的編碼器列舉</span><span class="sxs-lookup"><span data-stu-id="bfff0-109">Encoder Enumeration in Windows 7 and Later</span></span>](#encoder-enumeration-in-windows-7-and-later)
-   [<span data-ttu-id="bfff0-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfff0-110">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-activation-objects"></a><span data-ttu-id="bfff0-111">使用編碼器的啟用物件</span><span class="sxs-lookup"><span data-stu-id="bfff0-111">Using an Encoder's Activation Objects</span></span>

<span data-ttu-id="bfff0-112">另一種方法是使用編碼器的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面 (在 [使用 CoCreateInstance 建立編碼器](using-an-encoder-s-imftransform--interface.md)) 中所述，您可以為編碼器建立啟用物件的實例。</span><span class="sxs-lookup"><span data-stu-id="bfff0-112">As an alternative to using an encoder's [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface (described in [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md)), you can create an instance of the activation object for the encoder.</span></span> <span data-ttu-id="bfff0-113">啟用物件有助於建立編碼器，媒體基礎為此方法提供下列兩個功能：</span><span class="sxs-lookup"><span data-stu-id="bfff0-113">Activation objects facilitates encoder creation and Media Foundation provides the following two functions for this approach:</span></span>

-   <span data-ttu-id="bfff0-114">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 可具現化 Windows Media 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="bfff0-114">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) for instantiating the Windows Media audio encoder.</span></span>
-   <span data-ttu-id="bfff0-115">用來具現化 Windows Media video 編碼器的 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) 。</span><span class="sxs-lookup"><span data-stu-id="bfff0-115">[**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) for instantiating the Windows Media video encoder.</span></span>

<span data-ttu-id="bfff0-116">這兩個函式都需要您先建立目標媒體類型並設定編碼屬性，然後再呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="bfff0-116">Both these functions require that you create the target media type and set the encoding properties before calling these functions.</span></span> <span data-ttu-id="bfff0-117">如果您的應用程式使用 [管線層 ASF 元件](pipeline-layer-asf-components.md) 將檔案編碼為 asf 格式，而且已經建立並設定 [asf 媒體接收器](asf-media-sinks.md)，您就可以從 asf 媒體接收器取得這組資訊。</span><span class="sxs-lookup"><span data-stu-id="bfff0-117">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, and have already created and configured the [ASF Media Sinks](asf-media-sinks.md), you can get this set of information from the ASF media sink.</span></span>

<span data-ttu-id="bfff0-118">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) 會將編碼器的輸出類型設定為應用程式所指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bfff0-118">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) and [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) set the output type of the encoder to the media type specified by the application.</span></span>

<span data-ttu-id="bfff0-119">**注意**  如果您使用 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) ，則可以藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來啟用編碼器，但無法變更編碼器的輸入和輸出媒體類型，也不能變更任何編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="bfff0-119">**Note**  If you are using [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) and [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) you can activate the encoder by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) but you cannot change the input and the output media types of the encoder nor can you change any of the encoding properties.</span></span>

<span data-ttu-id="bfff0-120">如需使用啟用物件建立媒體基礎物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="bfff0-120">For more information about creating Media Foundation objects by using activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="bfff0-121">**從 ASF 媒體接收器取得目標媒體類型**</span><span class="sxs-lookup"><span data-stu-id="bfff0-121">**To get the target media type from the ASF media sink**</span></span>

1.  <span data-ttu-id="bfff0-122">藉由在 ASF 媒體接收上呼叫 **IMFMediaSink：： QueryInterface** ，並傳遞 **IID \_ IMFASFContentInfo** 作為介面識別碼，取得 asf 媒體接收器的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標指標。</span><span class="sxs-lookup"><span data-stu-id="bfff0-122">Get a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ASF media sink by calling **IMFMediaSink::QueryInterface** on the ASF media sink and passing **IID\_IMFASFContentInfo** as the interface identifier.</span></span>
2.  <span data-ttu-id="bfff0-123">取得與 ContentInfo 物件相關聯的 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="bfff0-123">Get the ASF profile object associated with the ContentInfo object.</span></span>
3.  <span data-ttu-id="bfff0-124">列舉設定檔中的串流，以取得資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bfff0-124">Enumerate the streams in the profile to get the stream's media type.</span></span>

<span data-ttu-id="bfff0-125">**從 ASF 媒體接收器取得編碼屬性**</span><span class="sxs-lookup"><span data-stu-id="bfff0-125">**To get the encoding properties from the ASF media sink**</span></span>

1.  <span data-ttu-id="bfff0-126">如果您已在 [檔案接收) 中 [設定屬性](setting-properties-in-the-file-sink.md) (所述的媒體接收器中設定 [編碼屬性](configuring-the-encoder.md)，您就可以在 ASF 媒體接收上呼叫 **IMFMediaSink：： QueryInterface** 並傳遞 **IID \_ IPropertyStore** 作為介面識別碼，藉以參考接收的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="bfff0-126">If you have configured the [Encoding Properties](configuring-the-encoder.md) in the media sink (described in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md)), you can a reference to the sink's property store by calling **IMFMediaSink::QueryInterface** on the ASF media sink and passing **IID\_IPropertyStore** as the interface identifier.</span></span>
2.  <span data-ttu-id="bfff0-127">如果您有接收器 ContentInfo 物件的指標，您可以呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 來取得媒體接收器屬性存放區的參考。</span><span class="sxs-lookup"><span data-stu-id="bfff0-127">If you have a pointer to the sink's ContentInfo object, you can call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get a reference to the media sink's property store.</span></span>

    <span data-ttu-id="bfff0-128">請確定在 ASF 媒體接收上設定的所有編碼屬性都會反映在傳遞給 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)的屬性存放區中。</span><span class="sxs-lookup"><span data-stu-id="bfff0-128">Make sure that all of encoding properties that are set on the ASF media sink are reflected in the property store passed to [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) and [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span> <span data-ttu-id="bfff0-129">編碼器會根據應用程式所指定的設定自動設定。</span><span class="sxs-lookup"><span data-stu-id="bfff0-129">The encoder is configured automatically based on the settings specified by the application.</span></span>

<span data-ttu-id="bfff0-130">在編碼拓撲中建立轉換節點時，您可以將物件類型設定為在這兩個呼叫中收到的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。</span><span class="sxs-lookup"><span data-stu-id="bfff0-130">While creating the transform node in the encoding topology, you can set the object type as an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer received in these two calls.</span></span> <span data-ttu-id="bfff0-131">當拓撲解決之後，媒體會話會使用啟用物件來建立編碼器 MFT 的實例。</span><span class="sxs-lookup"><span data-stu-id="bfff0-131">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="encoder-enumeration-in-windows-7-and-later"></a><span data-ttu-id="bfff0-132">Windows 7 和更新版本中的編碼器列舉</span><span class="sxs-lookup"><span data-stu-id="bfff0-132">Encoder Enumeration in Windows 7 and Later</span></span>

<span data-ttu-id="bfff0-133">針對在 Windows 7 上執行的應用程式，除了 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 之外，您還可以藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)來列舉編碼器 MFTs。</span><span class="sxs-lookup"><span data-stu-id="bfff0-133">For applications that are running on Windows 7, in addition to [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) you can enumerate the encoder MFTs by calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="bfff0-134">此函式會傳回編碼器 MFT 之啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="bfff0-134">This function returns a pointer to the activation object of the encoder MFT.</span></span> <span data-ttu-id="bfff0-135">函式的結構與上述 **MFTEnum** 非常類似，但 **MFTEnumEx** 會針對符合搜尋準則的編碼器 MFTs 傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="bfff0-135">The structure of the function is very similar to **MFTEnum** described above except **MFTEnumEx** returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers for the encoder MFTs that match the search criteria.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfff0-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfff0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfff0-137">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="bfff0-137">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="bfff0-138">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="bfff0-138">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> <dt>

[<span data-ttu-id="bfff0-139">啟用物件</span><span class="sxs-lookup"><span data-stu-id="bfff0-139">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 



