---
title: 啟動燒錄流程
description: 啟動燒錄流程
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，開始進行燒錄流程
- 燒錄 Cd，開始進行燒錄流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932944"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="94415-112">啟動燒錄流程</span><span class="sxs-lookup"><span data-stu-id="94415-112">Starting the Burn Process</span></span>

<span data-ttu-id="94415-113">開始燒錄之前，您必須指派要燒錄的播放清單。</span><span class="sxs-lookup"><span data-stu-id="94415-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="94415-114">使用 [IWMPCdromBurn：:p \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) ] 來指定燒錄播放清單。</span><span class="sxs-lookup"><span data-stu-id="94415-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="94415-115">如需使用播放清單的詳細資訊，請參閱 [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)。</span><span class="sxs-lookup"><span data-stu-id="94415-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="94415-116">若要開始燒錄作業，請呼叫 [IWMPCdromBurn：： startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)。</span><span class="sxs-lookup"><span data-stu-id="94415-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="94415-117">您可以藉由呼叫 [IWMPCdromBurn：： stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)來停止燒錄操作。</span><span class="sxs-lookup"><span data-stu-id="94415-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="94415-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="94415-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94415-119">**燒錄 CD**</span><span class="sxs-lookup"><span data-stu-id="94415-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="94415-120">**擷取 CD 燒錄介面**</span><span class="sxs-lookup"><span data-stu-id="94415-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="94415-121">**清除可讀寫 CD**</span><span class="sxs-lookup"><span data-stu-id="94415-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="94415-122">**正在抓取磁片磁碟機和光碟狀態**</span><span class="sxs-lookup"><span data-stu-id="94415-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="94415-123">**正在取出燒錄狀態**</span><span class="sxs-lookup"><span data-stu-id="94415-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




