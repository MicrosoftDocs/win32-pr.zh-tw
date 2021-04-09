---
title: 設定要求佇列
description: 設定要求佇列
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840012"
---
# <a name="configuring-the-request-queue"></a><span data-ttu-id="11893-103">設定要求佇列</span><span class="sxs-lookup"><span data-stu-id="11893-103">Configuring the Request Queue</span></span>

<span data-ttu-id="11893-104">當要求佇列開啟或建立時，呼叫的應用程式會收到它的控制碼，可用於傳送要求或設定要求佇列。</span><span class="sxs-lookup"><span data-stu-id="11893-104">When the request queue is opened or created, the calling application receives a handle to it that can be used to send requests or configure the request queue.</span></span> <span data-ttu-id="11893-105">使用 **HttpServerBindingProperty** 呼叫 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並在 HTTP 系結 [**\_ \_ 資訊**](/windows/desktop/api/Http/ns-http-http_binding_info)結構中提供要求佇列控制碼（在 *PPROPERTYINFORMATION* 參數中指定），就會將 URL 群組與要求佇列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="11893-105">Calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** and supplying the request queue handle in the [**HTTP\_BINDING\_INFO**](/windows/desktop/api/Http/ns-http-http_binding_info) structure, specified in the *pPropertyInformation* parameter, associates the URL group with the request queue.</span></span> <span data-ttu-id="11893-106">要求佇列屬性只能由建立要求佇列的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="11893-106">Request queue properties are set only by the application that creates the request queue.</span></span> <span data-ttu-id="11893-107">例如，若要設定 server queue length 屬性，建立者應用程式會呼叫 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)指定 *property* 參數中的 **HttpServerQueueLengthProperty** 。</span><span class="sxs-lookup"><span data-stu-id="11893-107">For example, to set the server queue length property, the creator application calls [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specifying **HttpServerQueueLengthProperty** in the *Property* parameter.</span></span>

 

 




