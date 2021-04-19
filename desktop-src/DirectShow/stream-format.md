---
description: 資料流程格式
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: 資料流程格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980602"
---
# <a name="stream-format"></a><span data-ttu-id="072df-103">資料流程格式</span><span class="sxs-lookup"><span data-stu-id="072df-103">Stream Format</span></span>

<span data-ttu-id="072df-104">MSDV 和 UVC 驅動程式都可以輸出兩種 DV 格式：交錯音訊-影片或僅限影片。</span><span class="sxs-lookup"><span data-stu-id="072df-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="072df-105">交錯音訊-影片是來自裝置的原始格式。</span><span class="sxs-lookup"><span data-stu-id="072df-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="072df-106">僅限影片的格式包含相同的資料，但範例標示為沒有音訊資料。</span><span class="sxs-lookup"><span data-stu-id="072df-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="072df-107">僅限影片的格式存在，主要是為了與使用適用于 Windows 的影片的應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="072df-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="072df-108">如需詳細資訊，請參閱 [type-1 與 type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md)。</span><span class="sxs-lookup"><span data-stu-id="072df-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="072df-109">**MSDV 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="072df-109">**MSDV Driver**</span></span>

<span data-ttu-id="072df-110">MSDV 驅動程式有兩個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="072df-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="072df-111">第一個輸出圖釘會傳送交錯的資料，而第二個輸出圖釘會傳送僅限影片的資料。</span><span class="sxs-lookup"><span data-stu-id="072df-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="072df-112">一次只能連接一個輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="072df-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="072df-113">若要選取格式，請連接適當的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="072df-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="072df-114">您可以在輸出釘選上使用 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面，以找出格式。</span><span class="sxs-lookup"><span data-stu-id="072df-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="072df-115">**UVC 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="072df-115">**UVC Driver**</span></span>

<span data-ttu-id="072df-116">與 MSDV 驅動程式不同的是，UVC 驅動程式會從相同的 pin 提供這兩種格式。</span><span class="sxs-lookup"><span data-stu-id="072df-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="072df-117">預設格式為僅限影片。</span><span class="sxs-lookup"><span data-stu-id="072df-117">The default format is video-only.</span></span> <span data-ttu-id="072df-118">若要選取格式，請在輸出釘選上使用 **IAMStreamConfig** 介面。</span><span class="sxs-lookup"><span data-stu-id="072df-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="072df-119">呼叫 **GetStreamCaps** 方法，以列舉輸出釘選上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="072df-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="072df-120">針對每個媒體類型，如果主要類型符合所需的格式，請呼叫 **SetFormat** 並傳入該媒體類型。</span><span class="sxs-lookup"><span data-stu-id="072df-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="072df-121">格式</span><span class="sxs-lookup"><span data-stu-id="072df-121">Format</span></span>                      | <span data-ttu-id="072df-122">主要類型</span><span class="sxs-lookup"><span data-stu-id="072df-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="072df-123">交錯音訊和影片</span><span class="sxs-lookup"><span data-stu-id="072df-123">Interleaved audio and video</span></span> | <span data-ttu-id="072df-124">媒體的 \_ 交錯</span><span class="sxs-lookup"><span data-stu-id="072df-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="072df-125">僅影片</span><span class="sxs-lookup"><span data-stu-id="072df-125">Video only</span></span>                  | <span data-ttu-id="072df-126">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="072df-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="072df-127">下列函式會根據主要型別 GUID 來設定格式。</span><span class="sxs-lookup"><span data-stu-id="072df-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="072df-128">MSDV 驅動程式也支援 **IAMStreamConfig**，因此您可以撰寫適用于這兩種裝置類型的程式碼。</span><span class="sxs-lookup"><span data-stu-id="072df-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="072df-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="072df-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="072df-130">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="072df-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



