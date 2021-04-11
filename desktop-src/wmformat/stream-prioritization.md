---
title: 資料流程優先順序
description: 資料流程優先順序
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK，資料流程優先順序
- Advanced Systems Format (ASF) 、串流優先順序
- ASF (Advanced 系統格式) 、串流優先順序
- Windows Media 格式 SDK，資料流程的優先權順序
- Advanced Systems Format (ASF) ，資料流程的優先順序順序
- ASF (Advanced Systems Format) ，資料流程的優先順序順序
- 資料流程，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023058"
---
# <a name="stream-prioritization"></a><span data-ttu-id="f2981-110">資料流程優先順序</span><span class="sxs-lookup"><span data-stu-id="f2981-110">Stream Prioritization</span></span>

<span data-ttu-id="f2981-111">當您建立 ASF 檔案時，可以為其組成的資料流程指定優先權順序。</span><span class="sxs-lookup"><span data-stu-id="f2981-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="f2981-112">如果您串流處理優先順序的檔案，而且可用的頻寬不足以傳遞所有資料流程，則讀取器會以反向優先權順序來卸載資料流程。</span><span class="sxs-lookup"><span data-stu-id="f2981-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="f2981-113">如此一來，您可以確保檔案中最重要的資料流程不會因為網路問題而卸載。</span><span class="sxs-lookup"><span data-stu-id="f2981-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="f2981-114">資料流程優先順序設定是以資料流程優先順序物件來設定，並新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="f2981-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="f2981-115">設定檔只能包含一個資料流程優先順序物件。</span><span class="sxs-lookup"><span data-stu-id="f2981-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2981-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2981-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2981-117">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="f2981-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="f2981-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="f2981-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="f2981-119">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="f2981-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="f2981-120">**IWMProfile3::RemoveStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="f2981-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="f2981-121">**IWMProfile3::SetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="f2981-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="f2981-122">**IWMStreamPrioritization 介面**</span><span class="sxs-lookup"><span data-stu-id="f2981-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="f2981-123">**使用資料流程優先順序**</span><span class="sxs-lookup"><span data-stu-id="f2981-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




