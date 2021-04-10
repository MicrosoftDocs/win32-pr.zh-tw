---
title: 擷取 CD 燒錄介面
description: 擷取 CD 燒錄介面
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，正在抓取 IWMPCdromCollection 介面
- 燒錄 Cd，正在抓取 IWMPCdromCollection 介面
- IWMPCdromCollection 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023157"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="36328-113">擷取 CD 燒錄介面</span><span class="sxs-lookup"><span data-stu-id="36328-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="36328-114">若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="36328-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="36328-115">您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="36328-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="36328-116">藉由使用 **get \_ count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="36328-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="36328-117">**IWMPCdrom** 介面代表個別的 CD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="36328-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="36328-118">開始燒錄 CD 之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="36328-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="36328-119">下列程式碼範例示範如何取出介面，以將 CD 燒錄到特定磁片磁碟機：</span><span class="sxs-lookup"><span data-stu-id="36328-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="36328-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="36328-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36328-121">**燒錄 CD**</span><span class="sxs-lookup"><span data-stu-id="36328-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="36328-122">**啟動燒錄流程**</span><span class="sxs-lookup"><span data-stu-id="36328-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="36328-123">**清除可讀寫 CD**</span><span class="sxs-lookup"><span data-stu-id="36328-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="36328-124">**正在抓取磁片磁碟機和光碟狀態**</span><span class="sxs-lookup"><span data-stu-id="36328-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="36328-125">**正在取出燒錄狀態**</span><span class="sxs-lookup"><span data-stu-id="36328-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="36328-126">**IWMPCdromCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="36328-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




