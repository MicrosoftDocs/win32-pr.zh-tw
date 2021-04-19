---
title: 管理寫入器延遲
description: 管理寫入器延遲
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF) ，管理寫入器延遲
- ASF (Advanced Systems Format) ，管理寫入器延遲
- Advanced Systems Format (ASF) ，寫入器延遲
- ASF (Advanced Systems Format) ，寫入器延遲
- 寫入器延遲
- 延遲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106967658"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="7246f-109">管理寫入器延遲</span><span class="sxs-lookup"><span data-stu-id="7246f-109">To Manage Writer Latency</span></span>

<span data-ttu-id="7246f-110">寫入器會花一些時間來處理範例。</span><span class="sxs-lookup"><span data-stu-id="7246f-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="7246f-111">傳遞輸入範例和寫入輸出範例之間的時間長度，稱為寫入器的延遲。</span><span class="sxs-lookup"><span data-stu-id="7246f-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="7246f-112">有許多因素會導致寫入器延遲，而且您可以透過數種方式來減少。</span><span class="sxs-lookup"><span data-stu-id="7246f-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="7246f-113">寫入器延遲最明顯的因素是壓縮範例所需的時間。</span><span class="sxs-lookup"><span data-stu-id="7246f-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="7246f-114">在大部分的情況下，您將不會有太多控制權。</span><span class="sxs-lookup"><span data-stu-id="7246f-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="7246f-115">如果頻寬不是大問題，您可以使用較少的壓縮來降低延遲。</span><span class="sxs-lookup"><span data-stu-id="7246f-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="7246f-116">當然，您可以傳遞已壓縮的範例來達到最少的延遲。</span><span class="sxs-lookup"><span data-stu-id="7246f-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="7246f-117">下一個因素是您通常有控制權的因素，是範例傳遞給讀取器的順序。</span><span class="sxs-lookup"><span data-stu-id="7246f-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="7246f-118">您可以藉由以簡報時間的順序傳遞範例，以及確保輸入樣本在所有輸入資料流程之間有妥善的同步處理，以達到更好的延遲。</span><span class="sxs-lookup"><span data-stu-id="7246f-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="7246f-119">不同資料流程範例之間的呈現時間差異愈大，就會產生更多延遲。</span><span class="sxs-lookup"><span data-stu-id="7246f-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="7246f-120">您可以藉由呼叫 [**IWMWriterAdvanced：： SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)，設定輸入樣本之間差異的最大值。</span><span class="sxs-lookup"><span data-stu-id="7246f-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7246f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7246f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7246f-122">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="7246f-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




