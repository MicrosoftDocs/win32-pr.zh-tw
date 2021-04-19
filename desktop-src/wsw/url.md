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
# <a name="url"></a><span data-ttu-id="dcf46-106">Url</span><span class="sxs-lookup"><span data-stu-id="dcf46-106">Url</span></span>

<span data-ttu-id="dcf46-107">WWSAPI URL API 元素提供將 Url 分割及 unescape 至元件元件的機制，以及將元件元件換成 URL 並將其合併回 URL。</span><span class="sxs-lookup"><span data-stu-id="dcf46-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="dcf46-108">若要將 Url 分割並 unescape 為元件部分，請使用 [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) 函式。</span><span class="sxs-lookup"><span data-stu-id="dcf46-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="dcf46-109">若要將元件元件換成 URL 並將其合併回 URL，請使用 [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) 函數。</span><span class="sxs-lookup"><span data-stu-id="dcf46-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="dcf46-110">若要將相對 Url 與構成絕對 URL 的絕對基底 URL 合併，請使用 [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) 函數。</span><span class="sxs-lookup"><span data-stu-id="dcf46-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="dcf46-111">下列列舉是 URL 的一部分：</span><span class="sxs-lookup"><span data-stu-id="dcf46-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="dcf46-112">**WS \_ URL \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="dcf46-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="dcf46-113">**WS \_ URL \_ 配置 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="dcf46-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="dcf46-114">下列函數是 URL 的一部分：</span><span class="sxs-lookup"><span data-stu-id="dcf46-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="dcf46-115">**WsCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="dcf46-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="dcf46-116">**WsDecodeUrl**</span><span class="sxs-lookup"><span data-stu-id="dcf46-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="dcf46-117">**WsEncodeUrl**</span><span class="sxs-lookup"><span data-stu-id="dcf46-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="dcf46-118">下列結構是 URL 的一部分：</span><span class="sxs-lookup"><span data-stu-id="dcf46-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="dcf46-119">**WS \_ HTTPS \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="dcf46-120">**WS \_ HTTP \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="dcf46-121">**WS \_ NETPIPE \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="dcf46-122">**WS \_ NETTCP \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="dcf46-123">**WS \_ SOAPUDP \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="dcf46-124">**WS \_ URL**</span><span class="sxs-lookup"><span data-stu-id="dcf46-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




