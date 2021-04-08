---
title: 正在抓取磁片磁碟機和光碟狀態
description: 正在抓取磁片磁碟機和光碟狀態
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄、取出磁片磁碟機和光碟狀態
- 燒錄 Cd、取出磁片磁碟機和光碟狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841911"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="2ea31-112">正在抓取磁片磁碟機和光碟狀態</span><span class="sxs-lookup"><span data-stu-id="2ea31-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="2ea31-113">開始 CD 燒錄操作之前，您必須確定所選的 CD-ROM 光碟機支援您要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="2ea31-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="2ea31-114">比方說，您必須先檢查 CD 是否能夠在呼叫 [IWMPCdromBurn：： erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)之前被清除。</span><span class="sxs-lookup"><span data-stu-id="2ea31-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="2ea31-115">下列程式碼顯示使用 [IWMPCdromBurn：： isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) 來判斷是否支援作業的範例：</span><span class="sxs-lookup"><span data-stu-id="2ea31-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="2ea31-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ea31-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ea31-117">**燒錄 CD**</span><span class="sxs-lookup"><span data-stu-id="2ea31-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="2ea31-118">**擷取 CD 燒錄介面**</span><span class="sxs-lookup"><span data-stu-id="2ea31-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="2ea31-119">**啟動燒錄流程**</span><span class="sxs-lookup"><span data-stu-id="2ea31-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="2ea31-120">**清除可讀寫 CD**</span><span class="sxs-lookup"><span data-stu-id="2ea31-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="2ea31-121">**正在取出燒錄狀態**</span><span class="sxs-lookup"><span data-stu-id="2ea31-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




