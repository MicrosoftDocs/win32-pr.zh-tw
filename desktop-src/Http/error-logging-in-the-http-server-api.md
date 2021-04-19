---
title: HTTP 伺服器 API 中的錯誤記錄
description: 某些類型的錯誤是由 HTTP 伺服器 API 處理，而不是傳回給應用程式進行處理，因為這類錯誤的頻率可能會產生事件記錄檔或應用程式處理常式。
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- HTTP 伺服器 API，錯誤記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966182"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="7830c-104">HTTP 伺服器 API 中的錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="7830c-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="7830c-105">某些類型的錯誤是由 HTTP 伺服器 API 處理，而不是傳回給應用程式進行處理，因為這類錯誤的頻率可能會產生事件記錄檔或應用程式處理常式。</span><span class="sxs-lookup"><span data-stu-id="7830c-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="7830c-106">下列三個主題說明 HTTP 伺服器 API 錯誤記錄的不同層面：</span><span class="sxs-lookup"><span data-stu-id="7830c-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="7830c-107">[](configuring-http-server-api-error-logging.md)設定登錄設定可控制 HTTP 伺服器 API 是否會記錄錯誤、可允許的記錄檔大小上限，以及記錄檔的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="7830c-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="7830c-108">[記錄檔格式](format-of-the-http-server-api-error-logs.md) HTTP 伺服器 API 會建立符合全球資訊網協會 (W3C) 記錄檔慣例的記錄檔，而且可以使用標準工具進行剖析。</span><span class="sxs-lookup"><span data-stu-id="7830c-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="7830c-109">不過，與 W3C 記錄檔不同的是，HTTP 伺服器 API 記錄檔不包含資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="7830c-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="7830c-110">[記錄的錯誤類型](types-of-errors-logged-by-the-http-server-api.md) HTTP 伺服器 API 會記錄各種常見的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7830c-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




