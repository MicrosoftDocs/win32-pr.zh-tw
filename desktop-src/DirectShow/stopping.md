---
description: 停止中
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: 停止中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851383"
---
# <a name="stopping"></a><span data-ttu-id="fca0d-103">停止中</span><span class="sxs-lookup"><span data-stu-id="fca0d-103">Stopping</span></span>

<span data-ttu-id="fca0d-104">**Stop** 方法必須解除封鎖 **接收** 方法，並取消認可篩選器的配置器。</span><span class="sxs-lookup"><span data-stu-id="fca0d-104">The **Stop** method must unblock the **Receive** method and decommit the filter's allocators.</span></span> <span data-ttu-id="fca0d-105">Decommitting 配置器會強制任何暫止的 **GetBuffer** 呼叫傳回，這會解除封鎖正在等候範例的上游篩選。</span><span class="sxs-lookup"><span data-stu-id="fca0d-105">Decommitting an allocator forces any pending **GetBuffer** calls to return, which unblocks upstream filters that are waiting for samples.</span></span> <span data-ttu-id="fca0d-106">**Stop** 方法會保存篩選鎖定，然後呼叫 [**CBaseFilter：： Stop**](cbasefilter-stop.md)方法，此方法會在所有篩選器的釘選上呼叫 [**CBasePin：：非**](cbasepin-inactive.md)使用中：</span><span class="sxs-lookup"><span data-stu-id="fca0d-106">The **Stop** method holds the filter lock and then calls the [**CBaseFilter::Stop**](cbasefilter-stop.md) method, which calls [**CBasePin::Inactive**](cbasepin-inactive.md) on all of the filter's pins:</span></span>


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



<span data-ttu-id="fca0d-107">覆寫輸入 pin 的 **非** 使用中方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fca0d-107">Override the input pin's **Inactive** method as follows:</span></span>


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



