---
title: 設定應用程式特定的超時
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- 設定應用程式特定超時 HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021387"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="c71af-104">設定應用程式特定的超時</span><span class="sxs-lookup"><span data-stu-id="c71af-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="c71af-105">HTTP 伺服器 API 範圍的設定適用于電腦上的所有伺服器會話和 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="c71af-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="c71af-106">應用程式可以藉由設定應用程式特定的超時值來覆寫這些設定。</span><span class="sxs-lookup"><span data-stu-id="c71af-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="c71af-107">伺服器會話超時會覆寫 HTTP 伺服器 API 範圍的超時，並套用至在其下建立的所有 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="c71af-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="c71af-108">設定 URL 群組的超時屬性，會覆寫群組中所有 Url 的伺服器會話超時。</span><span class="sxs-lookup"><span data-stu-id="c71af-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="c71af-109">針對 URL 群組的 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構中的任何計時器指定零，會導致 HTTP 伺服器 api 還原成伺服器會話超時（如果存在的話），如果伺服器會話超時不存在，則會使用 HTTP 伺服器 api 預設設定。</span><span class="sxs-lookup"><span data-stu-id="c71af-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="c71af-110">例如，當 URL 群組上有 [伺服器 timeout] 屬性，而 **EntityBody** 計時器為零時，就會使用伺服器會話超時。</span><span class="sxs-lookup"><span data-stu-id="c71af-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="c71af-111">如果未在伺服器會話上設定 [超時] 屬性，則會使用 HTTP 伺服器 API 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="c71af-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="c71af-112">若要停用計時器，請將值設定為 **MAXUSHORT**，但設定為 **MAXULONG** 的 **MinSendRate** 計時器除外。</span><span class="sxs-lookup"><span data-stu-id="c71af-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="c71af-113">HTTP 伺服器 API 只能設定應用程式特定的 **HeaderWait** ，而且只有在收到第一個要求之後， **IdleConnection** 計時器才會生效。</span><span class="sxs-lookup"><span data-stu-id="c71af-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="c71af-114">在收到第一個要求之前，會強制執行 HTTP 伺服器 API 範圍的超時值。</span><span class="sxs-lookup"><span data-stu-id="c71af-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="c71af-115">第一個要求抵達並與要求佇列相關聯後，就可以套用應用程式特定的 **HeaderWait** 和 **IdleConnection** 計時器。</span><span class="sxs-lookup"><span data-stu-id="c71af-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="c71af-116">應用程式專屬的計時器會套用至所有後續的要求，這些要求會抵達 keep-alive 連接的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="c71af-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="c71af-117">如需設定計時器的詳細資訊，請參閱設定 [URL 群組](configuring-the-url-group.md) 和設定 [伺服器會話](configuring-the-server-session.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="c71af-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




