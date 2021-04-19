---
title: Url
description: WWSAPI URL API 元素提供將 Url 分割及 unescape 至元件元件的機制，以及將元件元件換成 URL 並將其合併回 URL。
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- 適用于 Windows 的 Url Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/20/2020
ms.locfileid: "106967468"
---
# <a name="url"></a>Url

WWSAPI URL API 元素提供將 Url 分割及 unescape 至元件元件的機制，以及將元件元件換成 URL 並將其合併回 URL。

-   若要將 Url 分割並 unescape 為元件部分，請使用 [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) 函式。
-   若要將元件元件換成 URL 並將其合併回 URL，請使用 [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) 函數。
-   若要將相對 Url 與構成絕對 URL 的絕對基底 URL 合併，請使用 [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) 函數。

下列列舉是 URL 的一部分：

-   [**WS \_ URL \_ 旗標**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**WS \_ URL \_ 配置 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

下列函數是 URL 的一部分：

-   [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

下列結構是 URL 的一部分：

-   [**WS \_ HTTPS \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**WS \_ HTTP \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**WS \_ NETPIPE \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**WS \_ NETTCP \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**WS \_ SOAPUDP \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**WS \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




