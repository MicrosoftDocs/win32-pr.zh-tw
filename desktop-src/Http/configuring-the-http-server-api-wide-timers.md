---
title: 設定 HTTP Server API 寬計時器
description: 設定 HTTP Server API 寬計時器
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183545"
---
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="befee-103">設定 HTTP Server API 寬計時器</span><span class="sxs-lookup"><span data-stu-id="befee-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="befee-104">HTTP 伺服器 API 範圍的 **HeaderWait** 和 **IdleConnection** 計時器是藉由呼叫1.0 版 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="befee-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="befee-105">*ConfigId* 參數會設定為 **HttpServiceConfigTimeout** ，而 *pConfigInformation* 參數會指定 [**HTTP 服務設定 \_ \_ \_ TIMEOUT \_ 集**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)結構，其中包含已設定的計時器和計時器的值。</span><span class="sxs-lookup"><span data-stu-id="befee-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="befee-106">設定 HTTP 伺服器 API 範圍的超時會需要系統管理許可權，不過查詢它們並不會。</span><span class="sxs-lookup"><span data-stu-id="befee-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="befee-107">這些設定會針對電腦上的所有應用程式進行設定，並在重新開機 HTTP 服務或重新開機電腦時保存這些設定。</span><span class="sxs-lookup"><span data-stu-id="befee-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="befee-108">若要查詢現有的 HTTP 伺服器整個 API 的超時，應用程式會呼叫 [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)。</span><span class="sxs-lookup"><span data-stu-id="befee-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




