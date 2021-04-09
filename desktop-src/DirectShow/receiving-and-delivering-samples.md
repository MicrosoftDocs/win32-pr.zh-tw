---
description: 接收和傳遞範例
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: 接收和傳遞範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846155"
---
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="aab29-103">接收和傳遞範例</span><span class="sxs-lookup"><span data-stu-id="aab29-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="aab29-104">下列虛擬虛擬顯示如何執行 **IMemInput：： Receive** 方法：</span><span class="sxs-lookup"><span data-stu-id="aab29-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



<span data-ttu-id="aab29-105">**Receive 方法會** 保存串流鎖定，而不是篩選鎖定。</span><span class="sxs-lookup"><span data-stu-id="aab29-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="aab29-106">篩選可能需要等待某個事件，才能處理資料，如下所示，呼叫 **WaitForSingleObject**。</span><span class="sxs-lookup"><span data-stu-id="aab29-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="aab29-107">並非每個篩選都需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="aab29-107">Not every filter will need to do this.</span></span> <span data-ttu-id="aab29-108">[**CBaseInputPin：： Receive 方法會**](cbaseinputpin-receive.md)驗證一些一般串流狀況。</span><span class="sxs-lookup"><span data-stu-id="aab29-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="aab29-109">\_ \_ 如果篩選已停止，則會傳回 VFW E 錯誤的 \_ 狀態， \_ 如果篩選器正在排清，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="aab29-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="aab29-110">S \_ [確定] 以外的任何傳回碼表示 **Receive** 方法應該立即傳回，而不是處理範例。</span><span class="sxs-lookup"><span data-stu-id="aab29-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="aab29-111">處理範例之後，請呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md)，將它傳遞至下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="aab29-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="aab29-112">此 helper 方法會在下游輸入 pin 上呼叫 **IMemInputPin：： Receive** 。</span><span class="sxs-lookup"><span data-stu-id="aab29-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="aab29-113">篩選器可能會將範例傳遞給數個 pin。</span><span class="sxs-lookup"><span data-stu-id="aab29-113">A filter might deliver samples to several pins.</span></span>

 

 



