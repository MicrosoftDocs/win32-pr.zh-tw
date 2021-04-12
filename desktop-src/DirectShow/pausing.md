---
description: 正在暫停
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: 正在暫停
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109509"
---
# <a name="pausing"></a><span data-ttu-id="6f9f1-103">正在暫停</span><span class="sxs-lookup"><span data-stu-id="6f9f1-103">Pausing</span></span>

<span data-ttu-id="6f9f1-104">所有篩選準則狀態變更都必須保留篩選鎖定。</span><span class="sxs-lookup"><span data-stu-id="6f9f1-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="6f9f1-105">在 **Pause** 方法中，建立篩選器所需的任何資源：</span><span class="sxs-lookup"><span data-stu-id="6f9f1-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="6f9f1-106">[**CBaseFilter：:P ause**](cbasefilter-pause.md)方法會將篩選 (狀態的正確狀態設定為 \_ 暫停) ，並在篩選器中的每個連接的釘選上呼叫 [**CBasePin：： Active**](cbasepin-active.md)方法。</span><span class="sxs-lookup"><span data-stu-id="6f9f1-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="6f9f1-107">使用 **中的方法會** 通知釘選篩選已變成使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="6f9f1-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="6f9f1-108">如果 pin 建立資源，請覆寫 **使用中** 的方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6f9f1-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



