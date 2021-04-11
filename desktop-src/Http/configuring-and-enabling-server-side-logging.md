---
title: 設定和啟用伺服器端記錄
description: 設定和啟用伺服器端記錄
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372166"
---
# <a name="configuring-and-enabling-server-side-logging"></a><span data-ttu-id="2bed2-103">設定和啟用伺服器端記錄</span><span class="sxs-lookup"><span data-stu-id="2bed2-103">Configuring and Enabling Server Side Logging</span></span>

<span data-ttu-id="2bed2-104">應用程式會在使用 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)傳送回應之前，先在伺服器會話或 URL 群組上啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="2bed2-104">The application enables logging on the server session or the URL group before sending the response with [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span> <span data-ttu-id="2bed2-105">下列範例顯示如何設定和啟用 W3C 類型伺服器端記錄：</span><span class="sxs-lookup"><span data-stu-id="2bed2-105">The following example shows how to configure and enable W3C type server side logging:</span></span>

1.  <span data-ttu-id="2bed2-106">應用程式會使用 **格式** 成員中指定的 **HttpLoggingTypeW3C** 來初始化 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)結構，並使用 **欄位** 成員中 [**HTTP \_ 記錄 \_ 欄位**](http-log-field--constants.md)常數的位元遮罩來初始化。</span><span class="sxs-lookup"><span data-stu-id="2bed2-106">The application initializes the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure with **HttpLoggingTypeW3C** specified in the **Format** member, and a bitmask of the [**HTTP\_LOG\_FIELD**](http-log-field--constants.md) constants in the **Fields** member.</span></span>
2.  <span data-ttu-id="2bed2-107">應用程式會使用在 *Property* 參數中指定的 **HttpServerLoggingProperty** 來呼叫 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)或 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並呼叫 *pPropertyInformation* 參數中的 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)結構指標。</span><span class="sxs-lookup"><span data-stu-id="2bed2-107">The application calls [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) or [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerLoggingProperty** specified in the *Property* parameter and a pointer to the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure in the *pPropertyInformation* parameter.</span></span>

<span data-ttu-id="2bed2-108">[**HTTP \_ 記錄 \_ 欄位**](http-log-field--constants.md)常數的位元遮罩包含可在 W3C 記錄檔中記錄的欄位。</span><span class="sxs-lookup"><span data-stu-id="2bed2-108">The bitmask of the [**HTTP\_LOG\_FIELD**](http-log-field--constants.md) constants contain the fields that may be logged in the W3C log file.</span></span> <span data-ttu-id="2bed2-109">請注意，在伺服器會話或 URL 群組上設定 **HttpServerLoggingProperty** 屬性，並不表示將會記錄 HTTP 回應。</span><span class="sxs-lookup"><span data-stu-id="2bed2-109">Note that setting the **HttpServerLoggingProperty** property on a server session or a URL group does not mean that HTTP responses will be logged.</span></span> <span data-ttu-id="2bed2-110">當 W3C 在 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 或 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)的呼叫中啟用時，會以每個要求為基礎執行記錄。</span><span class="sxs-lookup"><span data-stu-id="2bed2-110">Logging is performed on a per request basis when W3C is enabled in the call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) or [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

<span data-ttu-id="2bed2-111">若要針對每個要求啟用 W3C 回應記錄，應用程式會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2bed2-111">To enable W3C response logging on a per request basis, the application performs the following steps:</span></span>

1.  <span data-ttu-id="2bed2-112">應用程式會使用將針對該回應記錄的欄位資訊，初始化 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data) 的成員。</span><span class="sxs-lookup"><span data-stu-id="2bed2-112">The application initializes the members of the [**HTTP\_LOG\_FIELDS\_DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) with the field information that will be logged for that response.</span></span>
2.  <span data-ttu-id="2bed2-113">[**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data)結構的 **基底. 類型** 成員應初始化為 **HttpLogDataTypeFields**。</span><span class="sxs-lookup"><span data-stu-id="2bed2-113">The **Base.Type** member of the [**HTTP\_LOG\_FIELDS\_DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) structure should be initialized to **HttpLogDataTypeFields**.</span></span> <span data-ttu-id="2bed2-114">**Base. Type** 欄位可確保結構和 API 未來的擴充性。</span><span class="sxs-lookup"><span data-stu-id="2bed2-114">The **Base.Type** field ensures the future extensibility of the structure and API.</span></span>
3.  <span data-ttu-id="2bed2-115">應用程式會使用 *pLogData* 參數中 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data)結構的指標，呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)或 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 。</span><span class="sxs-lookup"><span data-stu-id="2bed2-115">The application calls [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) or [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) with a pointer to the [**HTTP\_LOG\_FIELDS\_DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) structure in the *pLogData* parameter.</span></span> <span data-ttu-id="2bed2-116">應用程式應該輸入轉換 [**PHTTP \_ 記錄 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_data)的指標。</span><span class="sxs-lookup"><span data-stu-id="2bed2-116">The application should type cast the pointer to [**PHTTP\_LOG\_DATA**](/windows/desktop/api/Http/ns-http-http_log_data).</span></span>

 

 




