---
title: 頻寬共用
description: 頻寬共用
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK，頻寬共用
- Advanced Systems Format (ASF) 、頻寬共用
- ASF (Advanced 系統格式) 、頻寬共用
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 頻寬共用、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023062"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="aff09-110">頻寬共用</span><span class="sxs-lookup"><span data-stu-id="aff09-110">Bandwidth Sharing</span></span>

<span data-ttu-id="aff09-111">您可以在檔案中指定資料流程（當兩者一起使用）時，使用的頻寬比其所指定位速率的總和低。</span><span class="sxs-lookup"><span data-stu-id="aff09-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="aff09-112">藉由在設定檔中指定頻寬共用，您將會明確說明如何讀取應用程式，以串流檔案所需的可用頻寬，不是其他可能的情況。</span><span class="sxs-lookup"><span data-stu-id="aff09-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="aff09-113">Windows Media 格式 SDK 的物件都不會變更其行為以回應頻寬共用資訊，而是要讓讀取應用程式能在判斷是否可以在受限的頻寬傳遞中播放檔案時，將它列入考慮。</span><span class="sxs-lookup"><span data-stu-id="aff09-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="aff09-114">頻寬共用的設定是使用頻寬共用物件，並在開始寫入檔案之前新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="aff09-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aff09-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="aff09-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff09-116">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="aff09-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="aff09-117">**頻寬共用物件**</span><span class="sxs-lookup"><span data-stu-id="aff09-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="aff09-118">**IWMBandwidthSharing 介面**</span><span class="sxs-lookup"><span data-stu-id="aff09-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="aff09-119">**IWMProfile3 介面**</span><span class="sxs-lookup"><span data-stu-id="aff09-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="aff09-120">**使用頻寬共用**</span><span class="sxs-lookup"><span data-stu-id="aff09-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




