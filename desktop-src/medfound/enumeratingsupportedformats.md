---
description: 設定編解碼器 DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: 設定編解碼器 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564c0e6c566d9f583a495238f3ea6f0716d7adde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468628"
---
# <a name="configuring-codec-dmos"></a><span data-ttu-id="18035-103">設定編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="18035-103">Configuring Codec DMOs</span></span>

<span data-ttu-id="18035-104">本主題說明設定編解碼器 DMOs 的流程。</span><span class="sxs-lookup"><span data-stu-id="18035-104">This topic describes the process of configuring the codec DMOs.</span></span> <span data-ttu-id="18035-105">每個編解碼器都有特定的程式，但此處所述的全部資訊都有提供。</span><span class="sxs-lookup"><span data-stu-id="18035-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-dmo-inputs-and-outputs"></a><span data-ttu-id="18035-106">設定 SQL-DMO 輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="18035-106">Configuring DMO Inputs and Outputs</span></span>

<span data-ttu-id="18035-107">每個時都支援特定的輸入和輸出類型。</span><span class="sxs-lookup"><span data-stu-id="18035-107">Every DMO supports specific input and output types.</span></span> <span data-ttu-id="18035-108">您可以針對輸出呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) 來取得輸入和輸出支援的類型，並針對輸出呼叫 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) 。</span><span class="sxs-lookup"><span data-stu-id="18035-108">You can retrieve supported types for inputs and outputs by calling [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) for inputs and [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) for outputs.</span></span> <span data-ttu-id="18035-109">您可以對任一個方法進行重複呼叫來列舉支援的格式，並在每次呼叫時遞增型別索引。</span><span class="sxs-lookup"><span data-stu-id="18035-109">You can enumerate the supported formats by making repeated calls to either method, incrementing the type index with each call.</span></span> <span data-ttu-id="18035-110">當索引超過最終支援的類型時，呼叫會傳回 SQL-DMO \_ E \_ 沒有 \_ 其他 \_ 專案。</span><span class="sxs-lookup"><span data-stu-id="18035-110">When the index exceeds that of the final supported type, the call returns DMO\_E\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="18035-111">針對視頻編解碼器，針對指定的媒體子類型，只會列舉一個輸出類型或輸入類型。</span><span class="sxs-lookup"><span data-stu-id="18035-111">For the video codecs, only one output type or input type is enumerated for a given media subtype.</span></span> <span data-ttu-id="18035-112">針對音訊編解碼器，會列舉每個個別支援的類型。</span><span class="sxs-lookup"><span data-stu-id="18035-112">For the audio codecs, each individual supported type is enumerated.</span></span> <span data-ttu-id="18035-113">如需個別編解碼器支援類型的詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。</span><span class="sxs-lookup"><span data-stu-id="18035-113">For more information about supported types for individual codecs, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

<span data-ttu-id="18035-114">設定輸入和輸出資料流程的媒體類型之後，請分別呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) 和 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) 來設定它們。</span><span class="sxs-lookup"><span data-stu-id="18035-114">After you configure the media types for the input and output streams, set them by calling [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) respectively.</span></span> <span data-ttu-id="18035-115">這兩種方法都會傳回指定類型無效時， **\_ \_ \_ 不 \_ 接受的 E 類型** 。</span><span class="sxs-lookup"><span data-stu-id="18035-115">Both of these methods return **DMO\_E\_TYPE\_NOT\_ACCEPTED** if the specified type is invalid.</span></span>

## <a name="configuring-the-codec-dmos-for-encoding"></a><span data-ttu-id="18035-116">設定編碼的編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="18035-116">Configuring the Codec DMOs for Encoding</span></span>

<span data-ttu-id="18035-117">所有的 Windows Media 音訊和影片編解碼器都支援各種不同的編碼功能。</span><span class="sxs-lookup"><span data-stu-id="18035-117">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="18035-118">這些功能通常是藉由使用 **IPropertyBag** 介面的方法，藉以設定 sql-dmo 上的屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="18035-118">These features are generally configured by setting properties on the DMO by using the methods of the **IPropertyBag** interface.</span></span> <span data-ttu-id="18035-119">有些屬性是使用特製化的編解碼器介面進行設定。</span><span class="sxs-lookup"><span data-stu-id="18035-119">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="18035-120">在 [編解碼器物件](codecobjects.md)的區段中，會列出每個編解碼器的這些介面。</span><span class="sxs-lookup"><span data-stu-id="18035-120">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="18035-121">設定編碼方式的一般作業順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="18035-121">The general order of operations for configuring an encoding DMO is as follows:</span></span>

1.  <span data-ttu-id="18035-122">使用 **IPropertyBag** 的方法來設定所需的編解碼器功能。</span><span class="sxs-lookup"><span data-stu-id="18035-122">Configure codec features as desired by using the methods of **IPropertyBag**.</span></span>
2.  <span data-ttu-id="18035-123">如有需要，請使用編解碼器 SQL-DMO 介面來設定其他功能。</span><span class="sxs-lookup"><span data-stu-id="18035-123">Use the codec DMO interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="18035-124">設定輸入和輸出類型。</span><span class="sxs-lookup"><span data-stu-id="18035-124">Configure the input and output types.</span></span> <span data-ttu-id="18035-125">設定類型的順序會因個別編解碼器而異。</span><span class="sxs-lookup"><span data-stu-id="18035-125">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="18035-126">如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。</span><span class="sxs-lookup"><span data-stu-id="18035-126">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-dmos-for-decoding"></a><span data-ttu-id="18035-127">設定編解碼器 DMOs 進行解碼</span><span class="sxs-lookup"><span data-stu-id="18035-127">Configuring the Codec DMOs for Decoding</span></span>

<span data-ttu-id="18035-128">解碼比編碼更簡單，因為支援的解碼器功能較少。</span><span class="sxs-lookup"><span data-stu-id="18035-128">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="18035-129">設定解碼的一般作業順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="18035-129">The general order of operations for configuring a decoding DMO is as follows:</span></span>

1.  <span data-ttu-id="18035-130">使用 **IPropertyBag** 的方法來設定所需的解碼器功能。</span><span class="sxs-lookup"><span data-stu-id="18035-130">Configure decoder features as desired by using the methods of **IPropertyBag**.</span></span>
2.  <span data-ttu-id="18035-131">將輸入類型設定為用於編碼器輸出的類型。</span><span class="sxs-lookup"><span data-stu-id="18035-131">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="18035-132">設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="18035-132">Configure the output type.</span></span> <span data-ttu-id="18035-133">針對不同的輸入，支援的輸出類型是不同的。</span><span class="sxs-lookup"><span data-stu-id="18035-133">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="18035-134">請務必將相同的媒體類型用於編碼器輸入，如同用於編碼器輸出一樣。</span><span class="sxs-lookup"><span data-stu-id="18035-134">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="18035-135">這是因為 Windows Media 音訊和影片編解碼器使用媒體格式搭配額外的資料。</span><span class="sxs-lookup"><span data-stu-id="18035-135">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="18035-136">這項資料會附加至 PbFormat 成員的 [**成員所指向 \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)的結構， (通常是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="18035-136">This data is appended to the structure pointed to by the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure (usually [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))).</span></span> <span data-ttu-id="18035-137">針對某些類型，額外的資料是列舉編碼器輸出類型的一部分。</span><span class="sxs-lookup"><span data-stu-id="18035-137">For some types the extra data is part of the enumerated encoder output type.</span></span> <span data-ttu-id="18035-138">其他類型則需要您手動附加此資料。</span><span class="sxs-lookup"><span data-stu-id="18035-138">Other types require you to append this data manually.</span></span> <span data-ttu-id="18035-139">如果沒有延伸格式資料，您就無法將壓縮的內容解碼。</span><span class="sxs-lookup"><span data-stu-id="18035-139">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="18035-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="18035-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18035-141">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="18035-141">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
