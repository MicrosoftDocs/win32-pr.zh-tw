---
description: 取得緩衝區
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: 取得緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509796"
---
# <a name="getting-buffers"></a><span data-ttu-id="6a2cc-103">取得緩衝區</span><span class="sxs-lookup"><span data-stu-id="6a2cc-103">Getting Buffers</span></span>

<span data-ttu-id="6a2cc-104">如果您的篩選器具有使用篩選資源的自訂配置器，配置器的 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法應該保留串流鎖定，就像使用其他串流處理方法一樣：</span><span class="sxs-lookup"><span data-stu-id="6a2cc-104">If your filter has a custom allocator that uses filter resources, the allocator's [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method should hold the streaming lock, as with other streaming methods:</span></span>


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a><span data-ttu-id="6a2cc-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a2cc-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a2cc-106">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="6a2cc-106">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



