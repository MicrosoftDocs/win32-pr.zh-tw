---
title: 關於 HTTP 伺服器 API
description: HTTP 伺服器 API 為開發人員提供了低層級的介面，可與 RFC 2616 中定義的 HTTP 功能伺服器端搭配使用。
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- HTTP 伺服器 API，總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374603"
---
# <a name="about-http-server-api"></a><span data-ttu-id="d02dc-104">關於 HTTP 伺服器 API</span><span class="sxs-lookup"><span data-stu-id="d02dc-104">About HTTP Server API</span></span>

<span data-ttu-id="d02dc-105">HTTP 伺服器 API 為開發人員提供了低層級的介面，可與 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)中定義的 HTTP 功能伺服器端搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d02dc-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="d02dc-106">API 可讓應用程式接收導向至 Url 的 HTTP 要求，並傳送 HTTP 回應。</span><span class="sxs-lookup"><span data-stu-id="d02dc-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="d02dc-107">若要傳送動態回應，建議使用 ISAPI 或 ASP.NET 介面。</span><span class="sxs-lookup"><span data-stu-id="d02dc-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="d02dc-108">HTTP 伺服器 API 可讓多個應用程式並存于系統上，並共用相同的 TCP 埠 (例如，HTTP 的埠80或 HTTPS) 的埠443，以及提供 URL 命名空間的不同部分。</span><span class="sxs-lookup"><span data-stu-id="d02dc-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="d02dc-109">HTTP 伺服器 API 需要知道 C 程式設計語言，並熟悉 Windows API 程式設計。</span><span class="sxs-lookup"><span data-stu-id="d02dc-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="d02dc-110">不需要低層級 HTTP 存取的應用程式應該使用 IIS ISAPI 或適用于 HTTP 解決方案的 .NET Framework 類別。</span><span class="sxs-lookup"><span data-stu-id="d02dc-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




