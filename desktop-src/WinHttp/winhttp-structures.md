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
# <a name="winhttp-structures"></a>WinHTTP 結構

WinHTTP 使用下列結構：

<dl> <dt>

[**HTTP_VERSION_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

包含全域 HTTP 版本。

</dd> <dt>

[**URL_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

包含 URL 的組成部分。 此結構會搭配 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 和 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 函數使用。

</dd> <dt>

[**WINHTTP_ASYNC_RESULT**](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

包含對非同步函式之呼叫的結果。 此結構會與 [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 原型搭配使用。

</dd> <dt>

[**WINHTTP_AUTOPROXY_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

用來向 [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 函式指出是否要指定 Proxy 自動設定 (PAC) 檔的 url，或自動找出具有網路 DHCP 或 DNS 查詢的 url。

</dd> <dt>

[**WINHTTP_CERTIFICATE_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

包含從伺服器傳回的憑證資訊。 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)函數會使用這個結構。

</dd> <dt>

[**WINHTTP_CONNECTION_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

包含產生回應之要求的來源和目的地 IP 位址。

</dd> <dt>

[**WINHTTP_CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

包含用於伺服器和 proxy 驗證的使用者認證資訊。

> [!Note]
> 此結構已被取代。 相反地，建議使用 [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) 結構。

</dd> <dt>

[**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

包含用於伺服器和 proxy 驗證的使用者認證資訊。

</dd> <dt>

[**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

包含 Internet Explorer proxy 設定資訊。

</dd> <dt>

[**WINHTTP_PROXY_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

包含會話或預設 proxy 設定。

</dd> <dt>

[**WINHTTP_PROXY_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)提供的 proxy 結果專案集合。

</dd> <dt>

[**WINHTTP_PROXY_RESULT_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

呼叫 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)的結果專案。

</dd> <dt>

[**WINHTTP_REQUEST_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

包含要求的統計資料。

</dd> <dt>

[**WINHTTP_REQUEST_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

包含要求的計時資訊。

</dd> <dt>

[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

包含要求的安全通道連接和密碼資訊。

</dd> <dt>

[**WINHTTP_WEB_SOCKET_ASYNC_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

WebSocket 操作的結果狀態。

</dd> <dt>

[**WINHTTP_WEB_SOCKET_STATUS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

WebSocket 操作的狀態。

</dd> </dl>
