---
title: 使用資料流程優先順序
description: 使用資料流程優先順序
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media Format SDK，資料流程優先順序
- 設定檔，資料流程優先順序
- 資料流程，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932911"
---
# <a name="using-stream-prioritization"></a><span data-ttu-id="5c69b-106">使用資料流程優先順序</span><span class="sxs-lookup"><span data-stu-id="5c69b-106">Using Stream Prioritization</span></span>

<span data-ttu-id="5c69b-107">串流優先順序可讓您在設定檔中指定資料流程的優先順序，讓您能夠更充分掌控內容的播放。</span><span class="sxs-lookup"><span data-stu-id="5c69b-107">Stream prioritization enables you to have more control over the playback of content by allowing you to specify priority order for the streams in a profile.</span></span> <span data-ttu-id="5c69b-108">當讀取器和串流伺服器在播放期間遇到頻寬短缺時，可能必須卸載範例，以提供不中斷的播放。</span><span class="sxs-lookup"><span data-stu-id="5c69b-108">When the reader and streaming server encounter a bandwidth shortage during playback, samples may have to be dropped to provide uninterrupted playback.</span></span> <span data-ttu-id="5c69b-109">如果您在設定檔中指定具有資料流程優先權物件的優先權順序，則會先從最低優先順序的資料流程中卸載範例。</span><span class="sxs-lookup"><span data-stu-id="5c69b-109">If you specify a priority order with a stream prioritization object in the profile, samples will be dropped from the lowest priority streams first.</span></span>

<span data-ttu-id="5c69b-110">不同于頻寬共用和相互排除物件，資料流程優先順序物件不會使用 [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) 介面來追蹤資料流程清單。</span><span class="sxs-lookup"><span data-stu-id="5c69b-110">Unlike bandwidth sharing and mutual exclusion objects, a stream prioritization object does not use the [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) interface to keep track of the list of streams.</span></span> <span data-ttu-id="5c69b-111">相反地，您必須使用 [**WM \_ 資料流程 \_ 優先權 \_ 記錄**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="5c69b-111">Instead, you must use an array of [**WM\_STREAM\_PRIORITY\_RECORD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) structures.</span></span> <span data-ttu-id="5c69b-112">結構必須以優先順序的遞減順序組織在陣列中。</span><span class="sxs-lookup"><span data-stu-id="5c69b-112">The structures must be organized in the array in descending order of priority.</span></span> <span data-ttu-id="5c69b-113">除了保存資料流程號碼之外，資料流程優先權結構也可讓您指定資料流程是否為強制性。</span><span class="sxs-lookup"><span data-stu-id="5c69b-113">In addition to holding a stream number, the stream priority structure also enables you to specify whether a stream is mandatory.</span></span> <span data-ttu-id="5c69b-114">不會卸載強制資料流程，不論其在清單中的位置為何。</span><span class="sxs-lookup"><span data-stu-id="5c69b-114">Mandatory streams will not be dropped, regardless of their position in the list.</span></span>

<span data-ttu-id="5c69b-115">下列範例程式碼示範如何在設定檔中包含資料流程優先權。</span><span class="sxs-lookup"><span data-stu-id="5c69b-115">The following example code shows how to include a stream prioritization in a profile.</span></span> <span data-ttu-id="5c69b-116">此設定檔適用于教室簡報、講師說話的音訊串流、講師的影片串流，以及用來捕捉簡報投影片的影片串流。</span><span class="sxs-lookup"><span data-stu-id="5c69b-116">This profile is for a classroom presentation, with an audio stream of the lecturer speaking, a video stream of the lecturer, and a video stream capturing the presentation slides.</span></span> <span data-ttu-id="5c69b-117">音訊串流是最重要的，而且將是強制性的。</span><span class="sxs-lookup"><span data-stu-id="5c69b-117">The audio stream is the most important and will be mandatory.</span></span> <span data-ttu-id="5c69b-118">簡報投影片的優先順序最低，因為影像將會很大，因此在此有幾個框架，而不會有太大的差異。</span><span class="sxs-lookup"><span data-stu-id="5c69b-118">The presentation slides will have the lowest priority because the image will be pretty constant, so a few frames lost here and there won't make much difference.</span></span>


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="5c69b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c69b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c69b-120">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="5c69b-120">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




