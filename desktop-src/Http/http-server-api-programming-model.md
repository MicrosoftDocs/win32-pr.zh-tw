---
title: 程式設計模型
description: HTTP 伺服器 API 程式設計模型包含五個活動群組。
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def54ac8a34d6c53ea4e2825ef39884f0141df99
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104558984"
---
# <a name="programming-model"></a><span data-ttu-id="e8f2b-103">程式設計模型</span><span class="sxs-lookup"><span data-stu-id="e8f2b-103">Programming Model</span></span>

<span data-ttu-id="e8f2b-104">HTTP 伺服器 API 程式設計模型包含五個活動群組：</span><span class="sxs-lookup"><span data-stu-id="e8f2b-104">The HTTP Server API programming model includes five groups of activities:</span></span>

-   [<span data-ttu-id="e8f2b-105">設定組態</span><span class="sxs-lookup"><span data-stu-id="e8f2b-105">Setup configuration</span></span>](setup-configuration.md)
-   [<span data-ttu-id="e8f2b-106">執行階段設定</span><span class="sxs-lookup"><span data-stu-id="e8f2b-106">Run-time configuration</span></span>](run-time-configuration.md)
-   [<span data-ttu-id="e8f2b-107">建立和系結至要求佇列</span><span class="sxs-lookup"><span data-stu-id="e8f2b-107">Creating and binding to a request queue</span></span>](creating-and-binding-to-a-request-queue.md)
-   [<span data-ttu-id="e8f2b-108">處理要求</span><span class="sxs-lookup"><span data-stu-id="e8f2b-108">Processing requests</span></span>](processing-requests.md)
-   [<span data-ttu-id="e8f2b-109">關機和清除</span><span class="sxs-lookup"><span data-stu-id="e8f2b-109">Shutdown and cleanup</span></span>](shutdown-and-cleanup.md)

![顯示 H T T P Server A P I 程式設計模型的圖表。](images/http-server-api-programming-model.png)

<span data-ttu-id="e8f2b-111">如需示範如何處理 HTTP GET 和 POST 要求動作的範例應用程式，以及如何在應用程式未處理的要求中出現動作時傳送 503 (**未 \_ 執行**) 錯誤，請參閱 [HTTP 伺服器範例應用程式](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f2b-111">For a sample application that shows how to handle the HTTP GET and POST request actions and how to send a 503 (**NOT\_IMPLEMENTED**) error if actions are present in the request that the application does not handle, see [HTTP Server Sample Application](http-server-sample-application.md).</span></span>

 

 




