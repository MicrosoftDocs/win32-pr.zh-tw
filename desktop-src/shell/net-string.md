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
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111218"
---
# <a name="net_string"></a>NET \_ 字串

代表網路位址類型。 使用一或多個 (作為下列常數的位元組合) ，以建立與宏 [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)搭配使用的網路位址遮罩。



| 常數                                                                                                                                                                                                                   | 描述                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ 位址**</dt> </dl>                              | 字串會使用常值位址 (埠或不允許的首碼) 來識別 IPv4 主機/路由器。<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ 服務**</dt> </dl>                              | 字串會使用常值位址 (埠來識別 IPv4 服務;) 不允許前置詞。<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ 網路**</dt> </dl>                              | 字串會識別所需的 IPv4 網路 (首碼;) 不允許埠。<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**.NET \_ 字串 \_ IPV6 \_ 位址**</dt> </dl>                              | 字串會使用常值位址 (埠或不允許的首碼來識別 IPv6 主機/路由器;允許範圍識別碼。 ) <br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**淨 \_ 字串 \_ IPV6 \_ 位址 \_ 沒有 \_ 範圍**</dt> </dl> | 字串會使用常值位址識別 IPv6 主機/路由器，其中介面內容已已知 (埠或首碼不允許;不允許) 範圍識別碼。<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**.NET \_ 字串 \_ IPV6 \_ 服務**</dt> </dl>                              | 字串會使用常值位址 (埠來識別 IPv6 服務;不允許前置詞;允許) 範圍識別碼。<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt> </dl> | 字串會使用常值位址來識別已已知介面內容 (埠所需的 IPv6 服務;不允許前置詞;不允許) 範圍識別碼。<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ 網路**</dt> </dl>                              | 字串會識別 IPv6 網路， (需要的首碼;) 不允許埠或範圍識別碼。<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**\_ \_ 名稱為 \_ ADDRESS 的 NET 字串**</dt> </dl>                           | 字串會使用 DNS (埠或前置詞或範圍識別碼) 不允許的網際網路主機識別。<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**\_ \_ 名為 \_ SERVICE 的 NET 字串**</dt> </dl>                           | 字串會使用需要的 DNS (埠來識別網際網路服務;) 不允許前置詞或範圍識別碼。<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**NET \_ STRING \_ IP \_ 位址**</dt> </dl>                                    | NET \_ string \_ IPV4 \_ address \| net \_ string \_ IPV6 \_ 位址。<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**淨 \_ 字串 \_ IP \_ 位址 \_ 沒有 \_ 範圍**</dt> </dl>       | NET \_ string \_ IPV4 \_ address \| net \_ string \_ IPV6 \_ address \_ NO \_ SCOPE。 <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ STRING \_ IP \_ 服務**</dt> </dl>                                    | NET \_ string \_ IPV4 \_ service \| net \_ string \_ IPV6 \_ 服務。<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>       | \_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**NET \_ STRING \_ IP \_ 網路**</dt> </dl>                                    | NET \_ string \_ IPV4 \_ network \| net \_ string \_ IPV6 \_ 網路。<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ 字串 \_ 任何 \_ 位址**</dt> </dl>                                 | \_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS 的 NET 字串。<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**.NET \_ 字串 \_ 任何 \_ 位址 \_ 沒有 \_ 範圍**</dt> </dl>    | \_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**.NET \_ 字串 \_ 任何 \_ 服務**</dt> </dl>                                 | \_ \_ 名為 \_ SERVICE \| NET \_ STRING \_ IP \_ SERVICE 的 NET 字串。<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**.NET \_ 字串 \_ 任何 \_ 服務 \_ 無 \_ 範圍**</dt> </dl>    | \_ \_ 名稱為 \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE 的 NET 字串。<br/>                                                                                                 |



## <a name="remarks"></a>備註

這些值定義于 Iphlpapi 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Iphlpapi。h</dt> </dl> |



 

 




