---
description: 設定中的媒體類型
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: 設定中的媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974768"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="10df4-103">設定中的媒體類型</span><span class="sxs-lookup"><span data-stu-id="10df4-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="10df4-104">在 SQL-DMO 可以處理任何資料之前，用戶端必須設定每個資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="10df4-105"> (此規則有一個次要例外狀況;請參閱 [選擇性資料流程](optional-streams.md)。 ) 若要尋找資料流程的數目，請呼叫 [**IMediaObject：： GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) 方法：</span><span class="sxs-lookup"><span data-stu-id="10df4-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="10df4-106">這個方法會傳回兩個值，也就是輸入數目和輸出數目。</span><span class="sxs-lookup"><span data-stu-id="10df4-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="10df4-107">這些值在每個的存留期都是固定的。</span><span class="sxs-lookup"><span data-stu-id="10df4-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="10df4-108">**慣用類型**</span><span class="sxs-lookup"><span data-stu-id="10df4-108">**Preferred Types**</span></span>

<span data-ttu-id="10df4-109">針對每個資料流程，每個資料流程會依喜好設定指派可能媒體類型的清單。</span><span class="sxs-lookup"><span data-stu-id="10df4-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="10df4-110">例如，慣用的類型可能是 32-RGB、24位 RGB 和16位 RGB （依該順序）。</span><span class="sxs-lookup"><span data-stu-id="10df4-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="10df4-111">當用戶端設定媒體類型時，它可以使用這些清單做為提示。</span><span class="sxs-lookup"><span data-stu-id="10df4-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="10df4-112">若要取得資料流程的慣用型別，請呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) 方法或 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) 方法。</span><span class="sxs-lookup"><span data-stu-id="10df4-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="10df4-113">指定從零) 開始 (類型的資料流程號碼和索引值。</span><span class="sxs-lookup"><span data-stu-id="10df4-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="10df4-114">例如，下列程式碼會從第一個輸入資料流程抓取第一個慣用的型別：</span><span class="sxs-lookup"><span data-stu-id="10df4-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="10df4-115">若要列舉給定資料流程上所有慣用的媒體類型，請使用會遞增類型索引的迴圈，直到該方法傳回 SQL-DMO \_ E \_ NO \_ 其他 \_ 專案，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="10df4-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="10df4-116">您應該注意下列關於慣用類型的重點：</span><span class="sxs-lookup"><span data-stu-id="10df4-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="10df4-117">SQL-DMO 可能會傳回沒有格式區塊的型別。</span><span class="sxs-lookup"><span data-stu-id="10df4-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="10df4-118">例如，當您不提供影像的寬度和高度時，可以指定像24位 RGB 的影片類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="10df4-119">但是，當您設定型別時，您必須提供完整的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="10df4-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="10df4-120"> (部分媒體類型（例如 MIDI）永遠不需要格式區塊，在這種情況下，此備註不適用。 ) </span><span class="sxs-lookup"><span data-stu-id="10df4-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="10df4-121">不需要用來支援它所傳回的每個慣用類型組合。</span><span class="sxs-lookup"><span data-stu-id="10df4-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="10df4-122">比方說，如果有兩個數據流，而每個資料流程有四個慣用型別，則有16個可能的組合，但並非全部都保證有效。</span><span class="sxs-lookup"><span data-stu-id="10df4-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="10df4-123">當用戶端設定某個資料流程的媒體類型時，每個資料流程可能會更新慣用的類型，以反映新的狀態。</span><span class="sxs-lookup"><span data-stu-id="10df4-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="10df4-124">但是，不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="10df4-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="10df4-125">若為某些資料流程，則： < 可能無法提供任何慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="10df4-126">一般情況下，您應該至少在某些資料流程上提供一些慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="10df4-127">您不需要使用 SQL-DMO 來提供可接受之媒體類型的完整清單。</span><span class="sxs-lookup"><span data-stu-id="10df4-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="10df4-128">您可能會有 "unadvertised" 類型，例如，</span><span class="sxs-lookup"><span data-stu-id="10df4-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="10df4-129">簡單地說，用戶端應該將慣用的型別視為指導方針。</span><span class="sxs-lookup"><span data-stu-id="10df4-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="10df4-130">若要瞭解支援的特定類型，唯一的方法是進行測試，如下一節所述。</span><span class="sxs-lookup"><span data-stu-id="10df4-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="10df4-131">**設定資料流程上的媒體類型**</span><span class="sxs-lookup"><span data-stu-id="10df4-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="10df4-132">您可以使用 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) 和 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) 方法來設定每個資料流程的類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="10df4-133">您必須提供包含媒體類型完整描述的一 **\_ \_ 種媒體類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="10df4-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="10df4-134">下列範例會使用 44.1-kHz 16 位的身歷聲 PCM 音訊，設定輸入資料流程0上的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="10df4-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="10df4-135">若要在不設定的情況下測試媒體類型， 請使用 Sql-dmo  \_ SET \_ TYPEF \_ test \_ ONLY 旗標來呼叫 SetInputType 或 SetOutputType。</span><span class="sxs-lookup"><span data-stu-id="10df4-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="10df4-136">\_如果類型是可接受的，則方法會傳回 s OK， \_ 否則傳回 FALSE：</span><span class="sxs-lookup"><span data-stu-id="10df4-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="10df4-137">因為某個資料流程上的設定可能會影響另一個資料流程，所以您可能需要清除資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="10df4-138">若要這樣做，請呼叫 **SetInputType** 或 **SetOutputType** ，並使用 sql-dmo \_ SET \_ TYPEF \_ CLEAR 旗標。</span><span class="sxs-lookup"><span data-stu-id="10df4-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="10df4-139">若是的是解碼器，用戶端通常會先設定輸入型別，然後選擇輸出型別。</span><span class="sxs-lookup"><span data-stu-id="10df4-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="10df4-140">針對編碼器，用戶端會先設定輸出類型，然後再設定輸入類型。</span><span class="sxs-lookup"><span data-stu-id="10df4-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10df4-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="10df4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10df4-142">直接裝載</span><span class="sxs-lookup"><span data-stu-id="10df4-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



