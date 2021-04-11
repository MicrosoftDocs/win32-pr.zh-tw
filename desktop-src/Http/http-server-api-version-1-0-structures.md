---
title: HTTP 伺服器 API 版本1.0 結構
description: HTTP 伺服器 API 版本1.0 結構
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- HTTP 伺服器 API 結構
- 結構 HTTP，HTTP 伺服器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375229"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="093ee-105">HTTP 伺服器 API 版本1.0 結構</span><span class="sxs-lookup"><span data-stu-id="093ee-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="093ee-106">HTTP 伺服器 API 提供下列結構：</span><span class="sxs-lookup"><span data-stu-id="093ee-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="093ee-107">**HTTPAPI.DLL \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="093ee-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="093ee-108">**HTTP \_ 位元組 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="093ee-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="093ee-109">**HTTP 快取 \_ \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="093ee-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="093ee-110">**HTTP \_ 處理後 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="093ee-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="093ee-111">**HTTP \_ 資料 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="093ee-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="093ee-112">**HTTP \_ 已知 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="093ee-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="093ee-113">[**HTTP \_ 要求**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="093ee-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="093ee-114">**HTTP \_ 要求 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="093ee-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="093ee-115">**HTTP \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="093ee-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="093ee-116">**HTTP \_ 回應 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="093ee-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="093ee-117">**HTTP \_ 服務 \_ 設定 \_ IP \_ 接聽 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="093ee-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="093ee-118">**HTTP \_ 服務 \_ 設定 \_ IP \_ 接聽 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="093ee-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="093ee-119">**HTTP \_ 服務 \_ 設定 \_ SSL \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="093ee-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="093ee-120">**HTTP \_ 服務 \_ 設定 \_ SSL \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="093ee-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="093ee-121">**HTTP \_ 服務 \_ 設定 \_ SSL \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="093ee-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="093ee-122">**HTTP \_ 服務 \_ \_ 設定 SSL \_ 組**</span><span class="sxs-lookup"><span data-stu-id="093ee-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="093ee-123">**HTTP \_ 服務 \_ 設定 \_ SSL \_ SNI \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="093ee-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="093ee-124">**HTTP \_ 服務 \_ 設定 \_ SSL \_ SNI \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="093ee-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="093ee-125">**HTTP \_ 服務 \_ \_ 設定 SSL \_ SNI \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="093ee-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="093ee-126">**HTTP \_ 服務 \_ 設定 \_ URLACL \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="093ee-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="093ee-127">**HTTP \_ 服務 \_ 設定 \_ URLACL \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="093ee-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="093ee-128">**HTTP \_ 服務 \_ 設定 \_ URLACL \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="093ee-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="093ee-129">**HTTP \_ 服務 \_ \_ 設定 URLACL \_ 集**</span><span class="sxs-lookup"><span data-stu-id="093ee-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="093ee-130">**HTTP \_ SSL \_ 用戶端憑證 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="093ee-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="093ee-131">**HTTP \_ SSL \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="093ee-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="093ee-132">**HTTP \_ 傳輸 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="093ee-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="093ee-133">**HTTP \_ 未知的 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="093ee-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="093ee-134">**HTTP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="093ee-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="093ee-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="093ee-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="093ee-136">HTTP 伺服器 API 版本1.0 函式</span><span class="sxs-lookup"><span data-stu-id="093ee-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 