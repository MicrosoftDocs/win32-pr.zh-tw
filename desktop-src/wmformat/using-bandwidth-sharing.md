---
title: 使用頻寬共用
description: 使用頻寬共用
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK，頻寬共用
- 頻寬共用、關於
- 設定檔，頻寬共用
- 串流，頻寬共用
- 頻寬共用，IWMProfile 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374813"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="3b3f8-108">使用頻寬共用</span><span class="sxs-lookup"><span data-stu-id="3b3f8-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="3b3f8-109">您可以使用頻寬共用物件來指定特定資料流程合併時，不會使用超過指定的頻寬。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="3b3f8-110">頻寬共用物件中的資訊不會由寫入器產生或驗證，讀取器也不會使用它來進行任何作業。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="3b3f8-111">寫入設定檔中有頻寬共用資訊的檔案時，資料會儲存在其標頭區段中。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="3b3f8-112">播放檔案時，您可以使用讀取器中的 [**IWMProfile**](iwmprofile.md) 介面來檢查頻寬共用資訊。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="3b3f8-113">每個頻寬共用物件都是由兩個設定所定義。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="3b3f8-114">第一個是頻寬，如頻寬和緩衝區視窗所定義。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="3b3f8-115">第二個設定是頻寬共用類型，可以是專有或部分。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="3b3f8-116">獨佔頻寬共用表示會一次播放一次組成的資料流程，而部分表示資料流程會同時傳遞。</span><span class="sxs-lookup"><span data-stu-id="3b3f8-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b3f8-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b3f8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3f8-118">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="3b3f8-119">**IWMProfile3::AddBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="3b3f8-120">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="3b3f8-121">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="3b3f8-122">**IWMProfile3::GetBandwidthSharingCount**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="3b3f8-123">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="3b3f8-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




