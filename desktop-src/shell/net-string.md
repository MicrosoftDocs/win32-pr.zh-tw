---
description: 代表網路位址類型。 使用一或多個 (作為下列常數的位元組合) ，以建立與宏 NetAddr SetAllowType 搭配使用的網路位址遮罩 \_ 。
title: 'NET_STRING (Iphlpapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991110"
---
# <a name="net_string"></a><span data-ttu-id="59d55-104">NET \_ 字串</span><span class="sxs-lookup"><span data-stu-id="59d55-104">NET\_STRING</span></span>

<span data-ttu-id="59d55-105">代表網路位址類型。</span><span class="sxs-lookup"><span data-stu-id="59d55-105">Represent network address types.</span></span> <span data-ttu-id="59d55-106">使用一或多個 (作為下列常數的位元組合) ，以建立與宏 [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)搭配使用的網路位址遮罩。</span><span class="sxs-lookup"><span data-stu-id="59d55-106">Use one or more (as a bitwise combination) of the following constants to create a network address mask to use with the macro [**NetAddr\_SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).</span></span>



| <span data-ttu-id="59d55-107">常數</span><span class="sxs-lookup"><span data-stu-id="59d55-107">Constant</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="59d55-108">描述</span><span class="sxs-lookup"><span data-stu-id="59d55-108">Description</span></span>                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <span data-ttu-id="59d55-109"><dt>**NET \_ STRING \_ IPV4 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-109"><dt>**NET\_STRING\_IPV4\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-110">字串會使用常值位址 (埠或不允許的首碼) 來識別 IPv4 主機/路由器。</span><span class="sxs-lookup"><span data-stu-id="59d55-110">The string identifies an IPv4 host/router using literal address (port or prefix not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <span data-ttu-id="59d55-111"><dt>**NET \_ STRING \_ IPV4 \_ 服務**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-111"><dt>**NET\_STRING\_IPV4\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-112">字串會使用常值位址 (埠來識別 IPv4 服務;) 不允許前置詞。</span><span class="sxs-lookup"><span data-stu-id="59d55-112">The string identifies an IPv4 service using literal address (port required; prefix not allowed).</span></span><br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <span data-ttu-id="59d55-113"><dt>**NET \_ STRING \_ IPV4 \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-113"><dt>**NET\_STRING\_IPV4\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-114">字串會識別所需的 IPv4 網路 (首碼;) 不允許埠。</span><span class="sxs-lookup"><span data-stu-id="59d55-114">The string identifies an IPv4 network (prefix required; port not allowed).</span></span><br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <span data-ttu-id="59d55-115"><dt>**.NET \_ 字串 \_ IPV6 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-115"><dt>**NET\_STRING\_IPV6\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-116">字串會使用常值位址 (埠或不允許的首碼來識別 IPv6 主機/路由器;允許範圍識別碼。 ) </span><span class="sxs-lookup"><span data-stu-id="59d55-116">The string identifies an IPv6 Host/router using literal address (port or prefix not allowed; scope-id allowed.)</span></span><br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <span data-ttu-id="59d55-117"><dt>**淨 \_ 字串 \_ IPV6 \_ 位址 \_ 沒有 \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-117"><dt>**NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="59d55-118">字串會使用常值位址識別 IPv6 主機/路由器，其中介面內容已已知 (埠或首碼不允許;不允許) 範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d55-118">The string identifies an IPv6 Host/router using literal address where the interface context is already known (port or prefix not allowed; scope-id not allowed).</span></span><br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <span data-ttu-id="59d55-119"><dt>**.NET \_ 字串 \_ IPV6 \_ 服務**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-119"><dt>**NET\_STRING\_IPV6\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-120">字串會使用常值位址 (埠來識別 IPv6 服務;不允許前置詞;允許) 範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d55-120">The string identifies an IPv6 service using literal address (port required; prefix not allowed; scope-id allowed).</span></span><br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <span data-ttu-id="59d55-121"><dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-121"><dt>**NET\_STRING\_IPV6\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="59d55-122">字串會使用常值位址來識別已已知介面內容 (埠所需的 IPv6 服務;不允許前置詞;不允許) 範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d55-122">The string identifies an IPv6 service using literal address where the interface context is already known (port required; prefix not allowed; scope-id not allowed).</span></span><br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <span data-ttu-id="59d55-123"><dt>**NET \_ STRING \_ IPV6 \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-123"><dt>**NET\_STRING\_IPV6\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="59d55-124">字串會識別 IPv6 網路， (需要的首碼;) 不允許埠或範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d55-124">The string identifies an IPv6 network (prefix required; port or scope-id not allowed).</span></span><br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <span data-ttu-id="59d55-125"><dt>**\_ \_ 名稱為 \_ ADDRESS 的 NET 字串**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-125"><dt>**NET\_STRING\_NAMED\_ADDRESS**</dt></span></span> </dl>                           | <span data-ttu-id="59d55-126">字串會使用 DNS (埠或前置詞或範圍識別碼) 不允許的網際網路主機識別。</span><span class="sxs-lookup"><span data-stu-id="59d55-126">The string identifies an Internet Host using the DNS(port or prefix or scope-id not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <span data-ttu-id="59d55-127"><dt>**\_ \_ 名為 \_ SERVICE 的 NET 字串**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-127"><dt>**NET\_STRING\_NAMED\_SERVICE**</dt></span></span> </dl>                           | <span data-ttu-id="59d55-128">字串會使用需要的 DNS (埠來識別網際網路服務;) 不允許前置詞或範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d55-128">The string identifies an Internet service using DNS (port required; prefix or scope-id not allowed).</span></span><br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <span data-ttu-id="59d55-129"><dt>**NET \_ STRING \_ IP \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-129"><dt>**NET\_STRING\_IP\_ADDRESS**</dt></span></span> </dl>                                    | <span data-ttu-id="59d55-130">NET \_ string \_ IPV4 \_ address \| net \_ string \_ IPV6 \_ 位址。</span><span class="sxs-lookup"><span data-stu-id="59d55-130">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <span data-ttu-id="59d55-131"><dt>**淨 \_ 字串 \_ IP \_ 位址 \_ 沒有 \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-131"><dt>**NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="59d55-132">NET \_ string \_ IPV4 \_ address \| net \_ string \_ IPV6 \_ address \_ NO \_ SCOPE。</span><span class="sxs-lookup"><span data-stu-id="59d55-132">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE.</span></span> <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <span data-ttu-id="59d55-133"><dt>**NET \_ STRING \_ IP \_ 服務**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-133"><dt>**NET\_STRING\_IP\_SERVICE**</dt></span></span> </dl>                                    | <span data-ttu-id="59d55-134">NET \_ string \_ IPV4 \_ service \| net \_ string \_ IPV6 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="59d55-134">NET\_STRING\_IPV4\_SERVICE \| NET\_STRING\_IPV6\_SERVICE.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <span data-ttu-id="59d55-135"><dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-135"><dt>**NET\_STRING\_IP\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="59d55-136">\_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。</span><span class="sxs-lookup"><span data-stu-id="59d55-136">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <span data-ttu-id="59d55-137"><dt>**NET \_ STRING \_ IP \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-137"><dt>**NET\_STRING\_IP\_NETWORK**</dt></span></span> </dl>                                    | <span data-ttu-id="59d55-138">NET \_ string \_ IPV4 \_ network \| net \_ string \_ IPV6 \_ 網路。</span><span class="sxs-lookup"><span data-stu-id="59d55-138">NET\_STRING\_IPV4\_NETWORK \| NET\_STRING\_IPV6\_NETWORK.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <span data-ttu-id="59d55-139"><dt>**NET \_ 字串 \_ 任何 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-139"><dt>**NET\_STRING\_ANY\_ADDRESS**</dt></span></span> </dl>                                 | <span data-ttu-id="59d55-140">\_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS 的 NET 字串。</span><span class="sxs-lookup"><span data-stu-id="59d55-140">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <span data-ttu-id="59d55-141"><dt>**.NET \_ 字串 \_ 任何 \_ 位址 \_ 沒有 \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-141"><dt>**NET\_STRING\_ANY\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="59d55-142">\_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。</span><span class="sxs-lookup"><span data-stu-id="59d55-142">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <span data-ttu-id="59d55-143"><dt>**.NET \_ 字串 \_ 任何 \_ 服務**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-143"><dt>**NET\_STRING\_ANY\_SERVICE**</dt></span></span> </dl>                                 | <span data-ttu-id="59d55-144">\_ \_ 名為 \_ SERVICE \| NET \_ STRING \_ IP \_ SERVICE 的 NET 字串。</span><span class="sxs-lookup"><span data-stu-id="59d55-144">NET\_STRING\_NAMED\_SERVICE \| NET\_STRING\_IP\_SERVICE.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <span data-ttu-id="59d55-145"><dt>**.NET \_ 字串 \_ 任何 \_ 服務 \_ 無 \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-145"><dt>**NET\_STRING\_ANY\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="59d55-146">\_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。</span><span class="sxs-lookup"><span data-stu-id="59d55-146">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="59d55-147">備註</span><span class="sxs-lookup"><span data-stu-id="59d55-147">Remarks</span></span>

<span data-ttu-id="59d55-148">這些值定義于 Iphlpapi 中。</span><span class="sxs-lookup"><span data-stu-id="59d55-148">These values are defined in Iphlpapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d55-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="59d55-149">Requirements</span></span>



| <span data-ttu-id="59d55-150">需求</span><span class="sxs-lookup"><span data-stu-id="59d55-150">Requirement</span></span> | <span data-ttu-id="59d55-151">值</span><span class="sxs-lookup"><span data-stu-id="59d55-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59d55-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59d55-152">Minimum supported client</span></span><br/> | <span data-ttu-id="59d55-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59d55-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59d55-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59d55-154">Minimum supported server</span></span><br/> | <span data-ttu-id="59d55-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59d55-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59d55-156">標頭</span><span class="sxs-lookup"><span data-stu-id="59d55-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d55-157"><dt>Iphlpapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="59d55-157"><dt>Iphlpapi.h</dt></span></span> </dl> |



 

 




