---
title: 尋找資料流程號碼和輸出編號
description: 尋找資料流程號碼和輸出編號
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF) 、串流號碼
- ASF (Advanced Systems Format) ，建立數位
- Advanced Systems Format (ASF) ，尋找輸出數位
- ASF (Advanced Systems Format) ，尋找輸出數位
- 同步讀取器，資料流程編號
- 同步讀取器，尋找輸出數位
- 串流，尋找數位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681400"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="cee23-110">尋找資料流程號碼和輸出編號</span><span class="sxs-lookup"><span data-stu-id="cee23-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="cee23-111">同步讀取器支援更簡化的資料流程和輸出數目切換，而不是非同步讀取器的播放。</span><span class="sxs-lookup"><span data-stu-id="cee23-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="cee23-112">因此，更重要的是，能夠找出哪些串流號碼等於哪些輸出數位，或相反的方式。</span><span class="sxs-lookup"><span data-stu-id="cee23-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="cee23-113">若要尋找對應于資料流程號碼的輸出編號，請呼叫 [**IWMSyncReader：： GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream)。</span><span class="sxs-lookup"><span data-stu-id="cee23-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="cee23-114">若要尋找對應到輸出編號的資料流程號碼，請呼叫 [ **IWMSyncReader：： GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="cee23-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cee23-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="cee23-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee23-116">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="cee23-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="cee23-117">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="cee23-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="cee23-118">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="cee23-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




