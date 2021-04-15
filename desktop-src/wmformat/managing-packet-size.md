---
title: 管理封包大小
description: 管理封包大小
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK，管理封包大小
- Windows Media Format SDK，封包大小
- 設定檔，封包大小
- 設定檔，管理封包大小
- 封包，大小
- 封包，IWMPacketSize 介面
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374800"
---
# <a name="managing-packet-size"></a><span data-ttu-id="3fa9d-110">管理封包大小</span><span class="sxs-lookup"><span data-stu-id="3fa9d-110">Managing Packet Size</span></span>

<span data-ttu-id="3fa9d-111">寫入器是設計用來管理內部的封包大小。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="3fa9d-112">不過，您可能會有應用程式的特定需求，而這些需求會以手動方式控制您所撰寫之 ASF 檔案中的封包大小。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="3fa9d-113">Windows Media Format SDK 提供兩種介面： [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) 和 [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) ，可讓您控制封包大小的最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="3fa9d-114">這兩個封包大小介面都會公開于設定檔物件中。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="3fa9d-115">讀取器物件也可以使用它們。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-115">They are also available to the reader object.</span></span> <span data-ttu-id="3fa9d-116">如同其他設定檔相關的介面，讀取器只能存取讀取方法。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="3fa9d-117">封包大小對效能有一些影響。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="3fa9d-118">一般而言，封包大小越小，檔案內的資料就越分散。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="3fa9d-119">檔案越分散，重建它的效率就愈低。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="3fa9d-120">在串流處理案例中，這可能不是很重要的考慮，因為從網際網路來源讀取檔案的程式通常沒有效率。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="3fa9d-121">不過，在本機處理檔案時，這可能是一個考慮。</span><span class="sxs-lookup"><span data-stu-id="3fa9d-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fa9d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fa9d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fa9d-123">**IWMPacketSize 介面**</span><span class="sxs-lookup"><span data-stu-id="3fa9d-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="3fa9d-124">**IWMPacketSize2 介面**</span><span class="sxs-lookup"><span data-stu-id="3fa9d-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="3fa9d-125">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="3fa9d-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




