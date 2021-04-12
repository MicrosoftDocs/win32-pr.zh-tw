---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109281"
---
# <a name="receiveconnection"></a><span data-ttu-id="3d6ed-103">ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="3d6ed-103">ReceiveConnection</span></span>

<span data-ttu-id="3d6ed-104">當新的格式需要較大的緩衝區時，此機制可讓輸出釘選將格式變更建議給其下游對等。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="3d6ed-105">輸出圖釘會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3d6ed-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="3d6ed-106">在下游輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="3d6ed-107">如果 `ReceiveConnection` 成功，則在輸入 pin 上呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="3d6ed-108">此外，輸出 pin 可能需要呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) ，然後取消認可和重新認可配置器，以便變更緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="3d6ed-109">在變更緩衝區大小之前，請務必以舊格式傳遞所有暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="3d6ed-110">有些 MPEG-2 的解碼器會使用這種機制，在 MPEG-2 和 MPEG-2 輸出之間切換，或在影片大小變更時切換。</span><span class="sxs-lookup"><span data-stu-id="3d6ed-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



