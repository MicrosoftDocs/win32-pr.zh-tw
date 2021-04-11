---
title: 關機和清除
description: 若要讓應用程式正常終止，它必須執行下列清除作業。
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021553"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="e6a50-103">關機和清除</span><span class="sxs-lookup"><span data-stu-id="e6a50-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="e6a50-104">若要讓應用程式正常終止，它必須執行下列清除作業：</span><span class="sxs-lookup"><span data-stu-id="e6a50-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="e6a50-105">藉由呼叫 [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) 函式來取消註冊先前在 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)的呼叫中註冊的 URL，以移除 URL 群組中所有已註冊的 url。</span><span class="sxs-lookup"><span data-stu-id="e6a50-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="e6a50-106">藉由呼叫 [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) 函數來關閉 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="e6a50-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="e6a50-107">在伺服器會話下建立的所有 URL 群組都必須在關閉伺服器會話之前關閉。</span><span class="sxs-lookup"><span data-stu-id="e6a50-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="e6a50-108">藉由呼叫 [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession)來關閉伺服器會話。</span><span class="sxs-lookup"><span data-stu-id="e6a50-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="e6a50-109">藉由呼叫 [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)來關閉要求佇列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e6a50-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="e6a50-110">藉由呼叫 HttpTerminate 函式，針對應用程式最初對 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)所進行的每個呼叫，呼叫具有相符旗標設定的 [](/windows/desktop/api/Http/nf-http-httpterminate)函數，以終止 HTTP 伺服器 API 所建立的資源。</span><span class="sxs-lookup"><span data-stu-id="e6a50-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="e6a50-111">每個呼叫都會結束通話 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)時所建立的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e6a50-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




