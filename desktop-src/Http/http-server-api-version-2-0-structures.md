---
title: HTTP 伺服器 API 版本2.0 結構
description: HTTP 伺服器 API 2.0 版提供下列撰寫應用程式的結構
ms.assetid: 5a8e28e9-f85b-4550-929e-53f38eca6a8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5e41016592e16fcf159188cc1ebc760568f807
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372217"
---
# <a name="http-server-api-version-20-structures"></a><span data-ttu-id="3be7b-103">HTTP 伺服器 API 版本2.0 結構</span><span class="sxs-lookup"><span data-stu-id="3be7b-103">HTTP Server API Version 2.0 Structures</span></span>

<span data-ttu-id="3be7b-104">HTTP 伺服器 API 2.0 版提供下列撰寫應用程式的結構：</span><span class="sxs-lookup"><span data-stu-id="3be7b-104">The HTTP Server API version 2.0 provides the following structures for writing applications:</span></span>

-   [<span data-ttu-id="3be7b-105">**HTTP \_ 頻寬 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-105">**HTTP\_BANDWIDTH\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)
-   [<span data-ttu-id="3be7b-106">**HTTP 系結 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-106">**HTTP\_BINDING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_binding_info)
-   [<span data-ttu-id="3be7b-107">**HTTP \_ 通道系結 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-107">**HTTP\_CHANNEL\_BIND\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_channel_bind_info)
-   [<span data-ttu-id="3be7b-108">**HTTP \_ 連接 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-108">**HTTP\_CONNECTION\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_connection_limit_info)
-   [<span data-ttu-id="3be7b-109">**HTTP \_ FLOWRATE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-109">**HTTP\_FLOWRATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_flowrate_info)
-   [<span data-ttu-id="3be7b-110">**HTTP \_ 接聽 \_ 端點 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-110">**HTTP\_LISTEN\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_listen_endpoint_info)
-   [<span data-ttu-id="3be7b-111">**HTTP \_ 記錄檔 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="3be7b-111">**HTTP\_LOG\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_data)
-   [<span data-ttu-id="3be7b-112">**HTTP \_ 記錄 \_ 欄位 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="3be7b-112">**HTTP\_LOG\_FIELDS\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_fields_data)
-   [<span data-ttu-id="3be7b-113">**HTTP \_ 記錄 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-113">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
-   [<span data-ttu-id="3be7b-114">**HTTP \_ 多個 \_ 已知 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="3be7b-114">**HTTP\_MULTIPLE\_KNOWN\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)
-   [<span data-ttu-id="3be7b-115">**HTTP \_ 屬性 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="3be7b-115">**HTTP\_PROPERTY\_FLAGS**</span></span>](/windows/desktop/api/Http/ns-http-http_property_flags)
-   [<span data-ttu-id="3be7b-116">**HTTP \_ QOS \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-116">**HTTP\_QOS\_SETTING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_qos_setting_info)
-   [<span data-ttu-id="3be7b-117">**HTTP \_ 要求 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-117">**HTTP\_REQUEST\_AUTH\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_auth_info)
-   [<span data-ttu-id="3be7b-118">**HTTP \_ 要求 \_ 通道系結 \_ \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="3be7b-118">**HTTP\_REQUEST\_CHANNEL\_BIND\_STATUS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_channel_bind_status)
-   [<span data-ttu-id="3be7b-119">**HTTP \_ 要求 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-119">**HTTP\_REQUEST\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_info)
-   [<span data-ttu-id="3be7b-120">**HTTP \_ 要求 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="3be7b-120">**HTTP\_REQUEST\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v1)
-   [<span data-ttu-id="3be7b-121">**HTTP \_ 要求 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="3be7b-121">**HTTP\_REQUEST\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v2)
-   [<span data-ttu-id="3be7b-122">**HTTP \_ 回應 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-122">**HTTP\_RESPONSE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_response_info)
-   [<span data-ttu-id="3be7b-123">**HTTP \_ 回應 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="3be7b-123">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
-   [<span data-ttu-id="3be7b-124">**HTTP \_ 回應 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="3be7b-124">**HTTP\_RESPONSE\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v2)
-   [<span data-ttu-id="3be7b-125">**HTTP \_ 伺服器 \_ 驗證 \_ 基本 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="3be7b-125">**HTTP\_SERVER\_AUTHENTICATION\_BASIC\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_basic_params)
-   [<span data-ttu-id="3be7b-126">**HTTP \_ 伺服器 \_ 驗證 \_ 摘要 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="3be7b-126">**HTTP\_SERVER\_AUTHENTICATION\_DIGEST\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_digest_params)
-   [<span data-ttu-id="3be7b-127">**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-127">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
-   [<span data-ttu-id="3be7b-128">**HTTP \_ 服務系結 \_ \_ A**</span><span class="sxs-lookup"><span data-stu-id="3be7b-128">**HTTP\_SERVICE\_BINDING\_A**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_a)
-   [<span data-ttu-id="3be7b-129">**HTTP \_ 服務系結 \_ \_ W**</span><span class="sxs-lookup"><span data-stu-id="3be7b-129">**HTTP\_SERVICE\_BINDING\_W**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_w)
-   [<span data-ttu-id="3be7b-130">**HTTP \_ 服務系結 \_ \_ 基底**</span><span class="sxs-lookup"><span data-stu-id="3be7b-130">**HTTP\_SERVICE\_BINDING\_BASE**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_base)
-   [<span data-ttu-id="3be7b-131">**HTTP \_ 服務系結 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3be7b-131">**HTTP\_SERVICE\_BINDING\_TYPE**</span></span>](/windows/desktop/api/Http/ne-http-http_service_binding_type)
-   [<span data-ttu-id="3be7b-132">**HTTP \_ 服務 \_ 設定快取 \_ \_ 集**</span><span class="sxs-lookup"><span data-stu-id="3be7b-132">**HTTP\_SERVICE\_CONFIG\_CACHE\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_cache_set)
-   [<span data-ttu-id="3be7b-133">**HTTP \_ 服務 \_ \_ 設定超時 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="3be7b-133">**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)
-   [<span data-ttu-id="3be7b-134">**HTTP \_ 狀態 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-134">**HTTP\_STATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_state_info)
-   [<span data-ttu-id="3be7b-135">**HTTP \_ 超時 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3be7b-135">**HTTP\_TIMEOUT\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

 

 




