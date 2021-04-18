---
title: 啟動 Rip 進程
description: 啟動 Rip 進程
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，啟動 rip 進程
- 翻錄 Cd，啟動 rip 進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965415"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="537b9-112">啟動 Rip 進程</span><span class="sxs-lookup"><span data-stu-id="537b9-112">Starting the Rip Process</span></span>

<span data-ttu-id="537b9-113">當您依照上一節所述取出翻錄介面之後，請呼叫 [IWMPCdromRip：： startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)來啟動翻錄程式。</span><span class="sxs-lookup"><span data-stu-id="537b9-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="537b9-114">您可以藉由呼叫 [IWMPCdromRip：： stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)來停止翻錄作業。</span><span class="sxs-lookup"><span data-stu-id="537b9-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="537b9-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="537b9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="537b9-116">**將 CD 翻錄**</span><span class="sxs-lookup"><span data-stu-id="537b9-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="537b9-117">**擷取轉錄介面**</span><span class="sxs-lookup"><span data-stu-id="537b9-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="537b9-118">**正在抓取 Rip 狀態**</span><span class="sxs-lookup"><span data-stu-id="537b9-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="537b9-119">**選取要進行翻錄的專案**</span><span class="sxs-lookup"><span data-stu-id="537b9-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




