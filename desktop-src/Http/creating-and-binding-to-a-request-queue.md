---
title: 建立和系結至要求佇列
description: 要求佇列是保留特定應用程式暫止要求的服務佇列。
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372433"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="b2c66-103">建立和系結至要求佇列</span><span class="sxs-lookup"><span data-stu-id="b2c66-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="b2c66-104">要求佇列是保留特定應用程式暫止要求的服務佇列。</span><span class="sxs-lookup"><span data-stu-id="b2c66-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="b2c66-105">應用程式會藉由呼叫 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 函式來建立獨立于 URL 群組或伺服器會話的要求佇列，並藉由呼叫 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 函數來設定要求佇列屬性。</span><span class="sxs-lookup"><span data-stu-id="b2c66-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="b2c66-106">這些屬性是503回應的詳細資訊、佇列的最大長度，以及活動狀態。</span><span class="sxs-lookup"><span data-stu-id="b2c66-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="b2c66-107">為了將要求路由傳送至其要求佇列，應用程式會藉 [**由呼叫**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) *Property* 參數中指定的 **HttpServerBindingProperty** ，將其建立為 [執行時間](run-time-configuration.md)設定一部分的 URL 群組系結至佇列。</span><span class="sxs-lookup"><span data-stu-id="b2c66-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="b2c66-108">從群組中的 Url 傳入的要求會路由傳送至指定的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="b2c66-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




