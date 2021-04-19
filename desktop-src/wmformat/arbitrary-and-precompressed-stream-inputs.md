---
title: 任意和 Precompressed 的資料流程輸入
description: 任意和 Precompressed 的資料流程輸入
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF) 、任意資料流程輸入
- ASF (Advanced Systems Format) ，任意資料流程輸入
- 設定檔，任意資料流程輸入
- 編解碼器，任意資料流程輸入
- Advanced Systems Format (ASF) 、precompressed 資料流程輸入
- ASF (Advanced 系統格式) 、precompressed 資料流程輸入
- 設定檔，precompressed 資料流程輸入
- 編解碼器，precompressed 資料流程輸入
- precompressed 資料流程輸入
- 任意資料流程輸入
- 資料流程，任意資料流程輸入
- 資料流程，precompressed 資料流程輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106996561"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="606af-115">任意和 Precompressed 的資料流程輸入</span><span class="sxs-lookup"><span data-stu-id="606af-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="606af-116">只有其中一個 Windows Media 編解碼器所壓縮的輸入有多個可能的輸入。</span><span class="sxs-lookup"><span data-stu-id="606af-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="606af-117">其他類型的可能輸入為任意輸入和 precompressed 輸入。</span><span class="sxs-lookup"><span data-stu-id="606af-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="606af-118">本節將說明這些類型之輸入格式的需求。</span><span class="sxs-lookup"><span data-stu-id="606af-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="606af-119">任意資料流程輸入</span><span class="sxs-lookup"><span data-stu-id="606af-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="606af-120">任意資料流程類型的輸入與設定檔中所述的資料流程格式相同。</span><span class="sxs-lookup"><span data-stu-id="606af-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="606af-121">您不應該設定這些類型的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="606af-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="606af-122">Precompressed 資料流程輸入</span><span class="sxs-lookup"><span data-stu-id="606af-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="606af-123">將資料流程從某個檔案複製到另一個檔案時，您會傳遞已壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="606af-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="606af-124">在此情況下，您必須將 [輸入屬性] 物件設定為 **Null** ，以通知寫入器不需要驗證您要傳入的資料。</span><span class="sxs-lookup"><span data-stu-id="606af-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="606af-125">若要將輸入格式設定為 **Null**，請呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，並傳遞 **Null** 做為第二個參數。</span><span class="sxs-lookup"><span data-stu-id="606af-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="606af-126">使用 **Null** 參數呼叫這個方法時，您必須在呼叫 [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="606af-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="606af-127">使用 precompressed 串流時，您必須在寫入之前，手動將編解碼器資訊複製到檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="606af-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="606af-128">若要取得編解碼器資訊，請呼叫 [**IWMHeaderInfo2：： GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) 和 [**IWMHeaderInfo2：： GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) ，以列舉讀取器中與檔案相關聯的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="606af-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="606af-129">選取符合 precompressed 資料流程之資料流程設定的編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="606af-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="606af-130">然後藉由呼叫 [**IWMHeaderInfo3：： AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)來設定寫入器中的編解碼器資訊，傳遞從讀取器取得的資訊。</span><span class="sxs-lookup"><span data-stu-id="606af-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="606af-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="606af-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="606af-132">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="606af-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




