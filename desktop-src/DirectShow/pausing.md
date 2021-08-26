---
description: 正在暫停
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: 正在暫停
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997278"
---
# <a name="pausing"></a>正在暫停

所有篩選準則狀態變更都必須保留篩選鎖定。 在 **Pause** 方法中，建立篩選器所需的任何資源：


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



[**CBaseFilter：:P ause**](cbasefilter-pause.md)方法會將篩選 (狀態的正確狀態設定為 \_ 暫停) ，並在篩選器中的每個連接的釘選上呼叫 [**CBasePin：： Active**](cbasepin-active.md)方法。 使用 **中的方法會** 通知釘選篩選已變成使用中狀態。 如果 pin 建立資源，請覆寫 **使用中** 的方法，如下所示：


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



