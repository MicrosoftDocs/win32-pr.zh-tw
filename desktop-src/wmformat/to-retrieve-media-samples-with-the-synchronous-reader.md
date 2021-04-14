---
title: 使用同步讀取器取出媒體範例
description: 使用同步讀取器取出媒體範例
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF) ，正在抓取媒體範例
- ASF (Advanced 系統格式) ，正在抓取媒體範例
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，正在抓取媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374451"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="8f6fa-108">使用同步讀取器取出媒體範例</span><span class="sxs-lookup"><span data-stu-id="8f6fa-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="8f6fa-109">您必須從同步讀取器一次要求一個範例。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="8f6fa-110">這可讓您更充分掌控所收到的範例，以及接收這些樣本的時間。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="8f6fa-111">使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) 方法來取出範例。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="8f6fa-112">您必須將大部分的指標傳遞給變數，這些變數將會填入抓取為參數之範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="8f6fa-113">唯一的輸入參數是 *wStreamNum*。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="8f6fa-114">如果您傳遞串流號碼， **GetNextSample** 將會使用指定的資料流程號碼來取得下一個樣本。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="8f6fa-115">如果您傳遞零給 *wStreamNum*，則會抓取在檔案中時間先後出現的下一個範例。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="8f6fa-116">根據預設，同步讀取器會依時間順序從檔案的輸出中抓取所有範例。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="8f6fa-117">如果您呼叫 **GetNextSample** ，而且沒有其他要取得的範例，它會傳回 NS \_ E \_ no \_ 其他 \_ 範例，也就是失敗的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="8f6fa-118">因此，在撰寫程式碼時，您可以只對範例執行迴圈，直到方法失敗為止。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="8f6fa-119">若要確保同步讀取器能為影片串流提供正確的取樣持續時間，您必須先設定資料流程輸出。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="8f6fa-120">呼叫 [**IWMSyncReader：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) 方法，將 g \_ wszVideoSampleDurations 設定設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="8f6fa-121">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="8f6fa-121">Example Code</span></span>

<span data-ttu-id="8f6fa-122">下列範例程式碼示範如何使用 **GetNextSample** 來取出檔案中的所有範例。</span><span class="sxs-lookup"><span data-stu-id="8f6fa-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="8f6fa-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f6fa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6fa-124">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="8f6fa-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="8f6fa-125">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="8f6fa-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




