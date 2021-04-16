---
title: 堆積
description: 堆積會追蹤一組以一個單位來釋放的配置。
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- 適用于 Windows 的堆積 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383349"
---
# <a name="heap"></a>堆積

堆積會追蹤一組以一個單位來釋放的配置。

這可讓您避免在使用 WWSAPI 時，配置和解除配置記憶體的複雜模式。


每個訊息都有相關聯的堆積。 傳送訊息或接收訊息時，訊息的堆積會用於任何與該特定訊息相關的配置。 傳送或接收訊息之後，就會重設堆積 (這會清除與特定訊息) 相關的任何配置。

堆積也可以用來儲存訊息的存留期以外的訊息資料。 許多 API 在讀取資料時所使用的堆積允許規格，可讓您明確控制讀取的任何資料存留期。

來自堆積的配置保證至少會對齊8個位元組的界限。

零位元組配置會傳回非 Null 指標。

在 Windows 7 中，如果啟用 PageHeap，則會使用從 HeapCreate 傳回的堆積來管理記憶體。 在此情況下， [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) 會直接對應至 HeapAlloc，並將 [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) 對應至 HeapDestroy。

下列列舉會搭配堆積使用：

-   [**WS \_ 堆積 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

下列函式會搭配堆積使用：

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

下列控制碼會搭配堆積使用：

-   [WS \_ 堆積](ws-heap.md)

下列結構會搭配堆積使用：

-   [**WS \_ 堆積 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**WS \_ 堆積 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




