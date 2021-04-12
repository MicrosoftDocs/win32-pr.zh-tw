---
title: 通訊協定識別碼
description: 下列通訊協定識別碼也會列在 Windows SDK 的 Routprot 中，以及平臺軟體發展工具組 (SDK) 的 iprtmib .h。
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ac515eb4b5090c0b4f75fd923d8345538ff5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315946"
---
# <a name="protocol-identifiers"></a>通訊協定識別碼

下列通訊協定識別碼也會列在 Windows SDK 的 Routprot 中，以及平臺軟體發展工具組 (SDK) 的 iprtmib .h。

## <a name="ip-protocols"></a>IP 通訊協定

下列路由通訊協定會與 IP 傳輸相關聯。



| 通訊協定                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 協定 \_ IP \_ OTHER，MIB \_ IPPROTO \_ 其他                        | 未在 RFC 1354 中指定的其他通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ LOCAL，MIB \_ IPPROTO \_ LOCAL                        | 本機介面。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT、MIB \_ IPPROTO \_ NETMGMT                    | 靜態路由。 此值可用來透過網路管理（例如動態主機設定通訊協定） (DCHP) 、簡易網路管理通訊協定 (SNMP) ，或 [**CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry)、 [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)或 [**SetIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry) 函式的呼叫，來識別 IP 路由設定的路由資訊。                                                                                              |
| PROTO \_ IP \_ ICMP、MIB \_ IPPROTO \_ ICMP                          | ICMP 重新導向的結果。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP、MIB \_ IPPROTO \_ EGP                            | 外部閘道協定 (EGP) ，也就是動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP、MIB \_ IPPROTO \_ GGP                            | 閘道對網協定 (GGP) ，也就是動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ HELLO，MIB \_ IPPROTO \_ HELLO                        | Hellospeak 通訊協定，也就是動態路由通訊協定。 這是不在使用中的歷程記錄專案，而且是原始 ARPANET 路由器所使用的早期路由通訊協定，此通訊協定會執行稱為 Fuzzball 路由通訊協定的特殊軟體（有時稱為 Hellospeak），如 RFC 891 和 RFC 1305 中所述。 如需詳細資訊，請參閱 [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) 和 [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305)。 |
| PROTO \_ IP \_ RIP、MIB \_ IPPROTO \_ RIP                            | Berkeley 路由資訊通訊協定 (RIP) 或 RIP （動態路由通訊協定）。                                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ 為 \_ ，MIB \_ IPPROTO \_ \_ 是                      | 中繼系統到中繼系統 (是) 通訊協定，也就是動態路由通訊協定。 Was 是為了在開放式系統互連 (OSI) 通訊協定套件中使用而開發的通訊協定。                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ ES \_ 是，MIB \_ IPPROTO \_ ES \_                      | 終端系統到中繼系統 (ES-) 通訊協定，也就是動態路由通訊協定。 ES 的通訊協定是為了在開放式系統互連 (OSI) 通訊協定套件中使用而開發的。                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ CISCO、MIB \_ IPPROTO \_ CISCO                        | Cisco 內部閘道路由通訊協定 (IGRP) ，也就是動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN、MIB \_ IPPROTO \_ BBN                            | 閃電、Beranek 和 Newman (BBN) 內部閘道通訊協定 (IGP) 使用最短路徑第一個 (SPF) 演算法。 這是早期動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF，MIB \_ IPPROTO \_ OSPF                          | 開放式最短路徑先 (OSPF) 通訊協定，也就是動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP，MIB \_ IPPROTO \_ BGP                            | 邊界閘道協定 (BGP) 是動態路由通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP，MIB \_ IPPROTO \_ BOOTP                        | 啟動程式通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPV6 \_ DHCPRELAY、MIB \_ IPV6PROTO \_ HDCPRELAY            | DHCPv6 轉送通訊協定。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ AUTOSTATIC、MIB \_ IPNT \_ AUTOSTATIC             | 最初由路由通訊協定加入的 Windows 特定專案，但現在是靜態的。                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ 靜態、MIB \_ IPNT \_ 靜態                     | 從路由使用者介面或路由命令新增為靜態路由的 Windows 特定專案。                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ 靜態 \_ 非 \_ DOD，MIB \_ IPNT \_ 靜態 \_ 非 \_ DOD | 從路由使用者介面或路由命令新增為靜態路由的 Windows 特定專案，但這些路由不會造成 (DOD) 的撥號要求。                                                                                                                                                                                                                                                                                                                                                        |



 

具有 PROTO IP 本機通訊協定識別碼的路由 \_ \_ 包括：

-   回送路由
-   子網路由
-   子網介面的所有網路廣播路由
-   所有「1」 s 廣播路線
-   本機多播路由
-   傳送至 PPP 連結的遠端端點

IP 路由器管理員的識別碼為：

IPRTRMGR \_ PID

您可以使用此識別碼，而不是使用 IP 路由器管理員進行 MIB 呼叫的路由通訊協定識別碼。 此識別碼可用於 MIB-II、轉送 MIB 和某些企業特定資訊。 此識別碼也會列在 Iprtrmib 中。

## <a name="ipx-protocols"></a>IPX 通訊協定

下列路由通訊協定與 IPX 傳輸相關聯。



| 通訊協定            | 描述                          |
|---------------------|--------------------------------------|
| IPX \_ 通訊協定 \_ RIP  | 適用于 IPX 的路由資訊通訊協定 |
| IPX \_ 通訊協定 \_ SAP  | 服務公告通訊協定       |
| IPX \_ 通訊協定 \_ NLSP | NetWare 連結服務通訊協定       |



 

IPX 路由器管理員的識別碼為：

IPX \_ 通訊協定 \_ 基底

使用此識別碼，而不使用路由通訊協定識別碼進行與 IPX 路由器管理員的 MIB 通話。

 

 