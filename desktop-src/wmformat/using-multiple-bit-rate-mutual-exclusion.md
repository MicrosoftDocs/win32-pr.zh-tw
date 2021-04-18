---
title: 使用多個位速率互斥
description: 使用多個位速率互斥
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- 多重位元速率 (MBR) ，相互排除
- MBR (多位元率) ，相互排除
- '相互排除、多重位元速率 (MBR) '
- '設定檔，多位元率 (MBR) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77c7615845d10d07982676dfdb4dc8c617cebe
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314223"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a><span data-ttu-id="4cd40-107">使用多個位速率互斥</span><span class="sxs-lookup"><span data-stu-id="4cd40-107">Using Multiple Bit Rate Mutual Exclusion</span></span>

<span data-ttu-id="4cd40-108">當您想要針對各種不同的播放案例編碼內容時， (MBR) 互斥的多重位元速率很有用。</span><span class="sxs-lookup"><span data-stu-id="4cd40-108">Multiple bit rate (MBR) mutual exclusion is useful when you want to encode content for a variety of playback scenarios.</span></span> <span data-ttu-id="4cd40-109">MBR 影片輸出包含單一輸入編碼多次，每個輸入都有不同的位元速率設定。</span><span class="sxs-lookup"><span data-stu-id="4cd40-109">An MBR video output consists of a single input encoded multiple times, each with different bit-rate settings.</span></span> <span data-ttu-id="4cd40-110">當讀取具有 MBR 編碼的檔案時，讀取器會根據可用的頻寬來決定要使用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="4cd40-110">When a file with MBR encoding is read, the reader will determine which stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="4cd40-111">Windows Media Format SDK 支援適用于影片和音訊串流的 MBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="4cd40-111">The Windows Media Format SDK supports MBR encoding for both video and audio streams.</span></span> <span data-ttu-id="4cd40-112">此外，您還可以建立一種特殊類型的 MBR 編碼，稱為多重影片大小的 MBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="4cd40-112">In addition, you can create a special type of MBR encoding called multiple-video-size MBR encoding.</span></span> <span data-ttu-id="4cd40-113">多個影片大小 MBR 影片的功能與一般 MBR 影片相同，不同之處在于您可以針對相互排除的影片資料流程指定不同的影像大小。</span><span class="sxs-lookup"><span data-stu-id="4cd40-113">Multiple-video-size MBR video functions identically to normal MBR video except that you can specify different image sizes for the video streams in the mutual exclusion.</span></span>

<span data-ttu-id="4cd40-114">下列範例示範如何為具有多種影片大小的 MBR 影片設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="4cd40-114">The following example demonstrates how to set up a profile for MBR video with multiple video sizes.</span></span> <span data-ttu-id="4cd40-115">它會建立新的設定檔，其中包含三個不同位速率和大小的影片串流，並將它們包含在相互排除物件中。</span><span class="sxs-lookup"><span data-stu-id="4cd40-115">It creates a new profile with three video streams of varying bit rates and sizes, and includes them in a mutual exclusion object.</span></span>


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="4cd40-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cd40-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd40-117">**IWMMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="4cd40-117">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="4cd40-118">**IWMMutualExclusion 介面**</span><span class="sxs-lookup"><span data-stu-id="4cd40-118">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="4cd40-119">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="4cd40-119">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="4cd40-120">**IWMStreamConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="4cd40-120">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="4cd40-121">**使用相互排除**</span><span class="sxs-lookup"><span data-stu-id="4cd40-121">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="4cd40-122">**WM \_ 媒體 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="4cd40-122">**WM\_MEDIA\_TYPE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 




