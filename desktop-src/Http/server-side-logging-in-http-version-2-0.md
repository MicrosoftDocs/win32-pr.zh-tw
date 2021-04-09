---
title: Server-Side 記錄
description: 伺服器端記錄可在 URL 群組或伺服器會話上取得。
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840376"
---
# <a name="server-side-logging"></a><span data-ttu-id="27140-103">Server-Side 記錄</span><span class="sxs-lookup"><span data-stu-id="27140-103">Server-Side Logging</span></span>

<span data-ttu-id="27140-104">伺服器端記錄可在 URL 群組或伺服器會話上取得。</span><span class="sxs-lookup"><span data-stu-id="27140-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="27140-105">當伺服器會話啟用記錄功能時，它會以集中式形式記錄伺服器會話下的所有 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="27140-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="27140-106">在 URL 群組上啟用記錄功能時，只會在路由至 URL 群組的要求上執行記錄。</span><span class="sxs-lookup"><span data-stu-id="27140-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="27140-107">HTTP 伺服器 API 支援下列記錄類型：</span><span class="sxs-lookup"><span data-stu-id="27140-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="27140-108">[W3C 記錄](w3c-logging.md)：適用于伺服器會話和 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="27140-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="27140-109">[NCSA 記錄](ncsa-logging.md)：可在 URL 群組上使用。</span><span class="sxs-lookup"><span data-stu-id="27140-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="27140-110">[IIS 記錄](iis-logging.md)：可在 URL 群組上使用。</span><span class="sxs-lookup"><span data-stu-id="27140-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="27140-111">[集中式二進位記錄](centralized-binary-logging.md)：適用于伺服器會話。</span><span class="sxs-lookup"><span data-stu-id="27140-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="27140-112">為了利用 HTTP 記錄功能，應用程式會在伺服器會話或 URL 群組上啟用及設定一種記錄。</span><span class="sxs-lookup"><span data-stu-id="27140-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="27140-113">如需詳細資訊，請參閱設定 [和啟用伺服器端記錄](configuring-and-enabling-server-side-logging.md)</span><span class="sxs-lookup"><span data-stu-id="27140-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




