---
description: WinHTTP 支援的網際網路架構。
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: 'INTERNET_SCHEME (WinHTTP. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851676"
---
# <a name="internet_scheme"></a><span data-ttu-id="23253-103">網際網路 \_ 配置</span><span class="sxs-lookup"><span data-stu-id="23253-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="23253-104">WinHTTP 支援的網際網路架構。</span><span class="sxs-lookup"><span data-stu-id="23253-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="23253-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**網際網路 \_ 配置 \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="23253-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23253-106">1</span><span class="sxs-lookup"><span data-stu-id="23253-106">1</span></span>
</dt> <dt>



<span data-ttu-id="23253-107">HTTP 網際網路配置。</span><span class="sxs-lookup"><span data-stu-id="23253-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23253-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**網際網路 \_ 配置 \_ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="23253-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23253-109">2</span><span class="sxs-lookup"><span data-stu-id="23253-109">2</span></span>
</dt> <dt>



<span data-ttu-id="23253-110">HTTPS (SSL) 網際網路配置。</span><span class="sxs-lookup"><span data-stu-id="23253-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23253-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**網際網路 \_ 配置 \_ FTP**</span><span class="sxs-lookup"><span data-stu-id="23253-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23253-112">3</span><span class="sxs-lookup"><span data-stu-id="23253-112">3</span></span>
</dt> <dt>



<span data-ttu-id="23253-113">FTP 網際網路配置。</span><span class="sxs-lookup"><span data-stu-id="23253-113">An FTP internet scheme.</span></span> <span data-ttu-id="23253-114">此配置僅支援在 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 和 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)中使用。</span><span class="sxs-lookup"><span data-stu-id="23253-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23253-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**網際網路 \_ 配置 \_ SOCKS**</span><span class="sxs-lookup"><span data-stu-id="23253-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23253-116">4</span><span class="sxs-lookup"><span data-stu-id="23253-116">4</span></span>
</dt> <dt>



<span data-ttu-id="23253-117">SOCKS 網際網路配置。</span><span class="sxs-lookup"><span data-stu-id="23253-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="23253-118">此配置僅支援在 [**WINHTTP \_ PROXY \_ 結果 \_ 專案**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)中使用。</span><span class="sxs-lookup"><span data-stu-id="23253-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23253-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="23253-119">Requirements</span></span>



| <span data-ttu-id="23253-120">需求</span><span class="sxs-lookup"><span data-stu-id="23253-120">Requirement</span></span> | <span data-ttu-id="23253-121">值</span><span class="sxs-lookup"><span data-stu-id="23253-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23253-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23253-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23253-123">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23253-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="23253-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23253-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23253-125">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="23253-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="23253-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23253-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="23253-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="23253-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23253-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23253-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23253-129">**WINHTTP \_ PROXY \_ 結果 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="23253-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




