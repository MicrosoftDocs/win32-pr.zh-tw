---
title: 使用非同步讀取器傳遞壓縮的範例
description: 使用非同步讀取器傳遞壓縮的範例
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- 先進的系統格式 (ASF) ，傳遞壓縮的範例
- ASF (Advanced Systems Format) ，傳遞壓縮的範例
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) 、壓縮的範例
- ASF (Advanced Systems Format) ，壓縮的範例
- 非同步讀取器，傳遞壓縮的範例
- 非同步讀取器，壓縮的範例
- 壓縮的範例，傳遞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681418"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="503eb-112">使用非同步讀取器傳遞壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="503eb-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="503eb-113">非同步讀取器可以從 ASF 檔案中的串流傳遞壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="503eb-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="503eb-114">應用程式通常會在將資料流程從一個檔案複製到另一個檔案時，提供壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="503eb-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="503eb-115">建議您重新壓縮已從壓縮的資料流程重建的資料，因為編碼程式中的資料會遺失。</span><span class="sxs-lookup"><span data-stu-id="503eb-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="503eb-116">已壓縮超過一次的數位媒體將會明顯降低品質。</span><span class="sxs-lookup"><span data-stu-id="503eb-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="503eb-117">Windows Media Format SDK 不提供任何方法，可在資料從 ASF 檔案解壓縮之後進行解碼。</span><span class="sxs-lookup"><span data-stu-id="503eb-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="503eb-118">如果您收到壓縮的範例，之後想要將它們解壓縮，您必須提供自己的程式碼來進行。</span><span class="sxs-lookup"><span data-stu-id="503eb-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="503eb-119">解決這項限制的其中一種方法是將壓縮的範例寫入至新的 ASF 檔案，然後將它們重新讀取為一般、未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="503eb-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="503eb-120">若要使用非同步讀取器來接收壓縮的範例，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="503eb-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="503eb-121">執行 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼。</span><span class="sxs-lookup"><span data-stu-id="503eb-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="503eb-122">此回呼基本上與 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 的函式相同，不同之處在于它會依串流號碼提供範例，且範例仍會進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="503eb-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="503eb-123">開始播放之前，請藉由呼叫 **IWMReader：： QueryInterface** 來取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="503eb-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="503eb-124">藉由呼叫 [**IWMReaderAdvanced：： SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)，設定讀取器以傳遞所需資料流程的壓縮範例。</span><span class="sxs-lookup"><span data-stu-id="503eb-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="503eb-125">針對需要壓縮範例傳遞的每個資料流程重複步驟3。</span><span class="sxs-lookup"><span data-stu-id="503eb-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="503eb-126">影像串流對壓縮的資料流程傳遞而言無效。</span><span class="sxs-lookup"><span data-stu-id="503eb-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="503eb-127">如果您將影像串流從某個檔案複製到另一個檔案，它就無法在新的檔案中使用。</span><span class="sxs-lookup"><span data-stu-id="503eb-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="503eb-128">若要從檔案複製影像串流至檔案，請依輸出號碼抓取影像串流範例，並將它們包含在新的檔案中，如同包含新的影像串流一樣。</span><span class="sxs-lookup"><span data-stu-id="503eb-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="503eb-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="503eb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="503eb-130">**IWMReaderCallbackAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="503eb-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="503eb-131">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="503eb-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




