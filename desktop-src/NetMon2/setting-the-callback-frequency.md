---
description: 使用下列程式碼設定回呼頻率。
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: 設定回呼頻率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318523"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="0a418-103">設定回呼頻率</span><span class="sxs-lookup"><span data-stu-id="0a418-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="0a418-104">使用下列程式碼設定回呼頻率：</span><span class="sxs-lookup"><span data-stu-id="0a418-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="0a418-105">**DWORD** 值 = 1;</span><span class="sxs-lookup"><span data-stu-id="0a418-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="0a418-106">此程式碼片段會將回呼頻率設定為1秒， (最小值) 。</span><span class="sxs-lookup"><span data-stu-id="0a418-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="0a418-107">最大值必須大於1。</span><span class="sxs-lookup"><span data-stu-id="0a418-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="0a418-108">如果網路封包提供者 (NPP) 緩衝區已滿，則 NPP 會儘快呼叫監視器。</span><span class="sxs-lookup"><span data-stu-id="0a418-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



