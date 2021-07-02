---
description: 本主題將識別 WinHTTP 使用的結構。
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174980"
---
# <a name="winhttp-structures"></a><span data-ttu-id="2ea17-103">WinHTTP 結構</span><span class="sxs-lookup"><span data-stu-id="2ea17-103">WinHTTP structures</span></span>

<span data-ttu-id="2ea17-104">WinHTTP 使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="2ea17-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="2ea17-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="2ea17-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="2ea17-106">包含全域 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="2ea17-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="2ea17-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="2ea17-108">包含 URL 的組成部分。</span><span class="sxs-lookup"><span data-stu-id="2ea17-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="2ea17-109">此結構會搭配 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 和 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="2ea17-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="2ea17-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="2ea17-111">包含對非同步函式之呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="2ea17-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="2ea17-112">此結構會與 [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 原型搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2ea17-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="2ea17-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="2ea17-114">用來向 [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 函式指出是否要指定 Proxy 自動設定 (PAC) 檔的 url，或自動找出具有網路 DHCP 或 DNS 查詢的 url。</span><span class="sxs-lookup"><span data-stu-id="2ea17-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="2ea17-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="2ea17-116">包含從伺服器傳回的憑證資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="2ea17-117">[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="2ea17-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="2ea17-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="2ea17-119">表示連接群組。</span><span class="sxs-lookup"><span data-stu-id="2ea17-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="2ea17-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="2ea17-121">包含產生回應之要求的來源和目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2ea17-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="2ea17-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="2ea17-123">包含用於伺服器和 proxy 驗證的使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="2ea17-124">此結構已被取代。</span><span class="sxs-lookup"><span data-stu-id="2ea17-124">This structure has been deprecated.</span></span> <span data-ttu-id="2ea17-125">相反地，建議使用 [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) 結構。</span><span class="sxs-lookup"><span data-stu-id="2ea17-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="2ea17-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="2ea17-127">包含用於伺服器和 proxy 驗證的使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="2ea17-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="2ea17-129">包含 Internet Explorer proxy 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-130">**WINHTTP_EXTENDED_HEADER**</span><span class="sxs-lookup"><span data-stu-id="2ea17-130">**WINHTTP_EXTENDED_HEADER**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

<span data-ttu-id="2ea17-131">以名稱/值字串組表示 HTTP 要求標頭。</span><span class="sxs-lookup"><span data-stu-id="2ea17-131">Represents an HTTP request header as a name/value string pair.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-132">**WINHTTP_HEADER_NAME**</span><span class="sxs-lookup"><span data-stu-id="2ea17-132">**WINHTTP_HEADER_NAME**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

<span data-ttu-id="2ea17-133">表示 HTTP 要求標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="2ea17-133">Represents an HTTP request header name.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-134">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="2ea17-134">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="2ea17-135">代表連接群組的集合。</span><span class="sxs-lookup"><span data-stu-id="2ea17-135">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-136">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="2ea17-136">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="2ea17-137">表示連接的 GUID，以供連接比對之用。</span><span class="sxs-lookup"><span data-stu-id="2ea17-137">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-138">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="2ea17-138">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="2ea17-139">包含會話或預設 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="2ea17-139">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-140">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="2ea17-140">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="2ea17-141">[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)提供的 proxy 結果專案集合。</span><span class="sxs-lookup"><span data-stu-id="2ea17-141">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-142">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="2ea17-142">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="2ea17-143">呼叫 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)的結果專案。</span><span class="sxs-lookup"><span data-stu-id="2ea17-143">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="2ea17-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="2ea17-145">表示 WinHttp 連接的目前狀態原因。</span><span class="sxs-lookup"><span data-stu-id="2ea17-145">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-146">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="2ea17-146">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="2ea17-147">包含要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2ea17-147">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-148">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="2ea17-148">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="2ea17-149">包含要求的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-149">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-150">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="2ea17-150">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="2ea17-151">包含要求的安全通道連接和密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="2ea17-151">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="2ea17-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="2ea17-153">WebSocket 操作的結果狀態。</span><span class="sxs-lookup"><span data-stu-id="2ea17-153">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="2ea17-154">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="2ea17-154">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="2ea17-155">WebSocket 操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="2ea17-155">Status of a WebSocket operation.</span></span>

</dd> </dl>
