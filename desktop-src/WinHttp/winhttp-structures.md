---
description: 本主題將識別 WinHTTP 使用的結構。
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191354"
---
# <a name="winhttp-structures"></a><span data-ttu-id="7da17-103">WinHTTP 結構</span><span class="sxs-lookup"><span data-stu-id="7da17-103">WinHTTP structures</span></span>

<span data-ttu-id="7da17-104">WinHTTP 使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="7da17-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="7da17-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="7da17-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="7da17-106">包含全域 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="7da17-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="7da17-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="7da17-108">包含 URL 的組成部分。</span><span class="sxs-lookup"><span data-stu-id="7da17-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="7da17-109">此結構會搭配 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 和 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7da17-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="7da17-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="7da17-111">包含對非同步函式之呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="7da17-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="7da17-112">此結構會與 [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 原型搭配使用。</span><span class="sxs-lookup"><span data-stu-id="7da17-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="7da17-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="7da17-114">用來向 [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 函式指出是否要指定 Proxy 自動設定 (PAC) 檔的 url，或自動找出具有網路 DHCP 或 DNS 查詢的 url。</span><span class="sxs-lookup"><span data-stu-id="7da17-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="7da17-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="7da17-116">包含從伺服器傳回的憑證資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="7da17-117">[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="7da17-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-118">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="7da17-118">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="7da17-119">包含產生回應之要求的來源和目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7da17-119">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-120">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="7da17-120">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="7da17-121">包含用於伺服器和 proxy 驗證的使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-121">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="7da17-122">此結構已被取代。</span><span class="sxs-lookup"><span data-stu-id="7da17-122">This structure has been deprecated.</span></span> <span data-ttu-id="7da17-123">相反地，建議使用 [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) 結構。</span><span class="sxs-lookup"><span data-stu-id="7da17-123">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-124">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="7da17-124">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="7da17-125">包含用於伺服器和 proxy 驗證的使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-125">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="7da17-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="7da17-127">包含 Internet Explorer proxy 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-127">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-128">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="7da17-128">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="7da17-129">包含會話或預設 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="7da17-129">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-130">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="7da17-130">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="7da17-131">[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)提供的 proxy 結果專案集合。</span><span class="sxs-lookup"><span data-stu-id="7da17-131">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-132">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="7da17-132">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="7da17-133">呼叫 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)的結果專案。</span><span class="sxs-lookup"><span data-stu-id="7da17-133">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-134">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="7da17-134">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="7da17-135">包含要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7da17-135">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-136">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="7da17-136">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="7da17-137">包含要求的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-137">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-138">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="7da17-138">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="7da17-139">包含要求的安全通道連接和密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="7da17-139">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="7da17-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="7da17-141">WebSocket 操作的結果狀態。</span><span class="sxs-lookup"><span data-stu-id="7da17-141">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="7da17-142">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="7da17-142">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="7da17-143">WebSocket 操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="7da17-143">Status of a WebSocket operation.</span></span>

</dd> </dl>
