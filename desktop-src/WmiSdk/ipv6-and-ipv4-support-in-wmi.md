---
description: WMI IP 路由提供者和網路類別可提供 IPv4 位址的資料。 從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: WMI 中的 IPv6 和 IPv4 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984991"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>WMI 中的 IPv6 和 IPv4 支援

WMI [IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) 和網路類別可提供 IPv4 位址的資料。 從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。

## <a name="wmi-ip-data"></a>WMI IP 資料

下列類別僅提供 IPv4 資料：

-   [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

下列類別會為 IPv4 和 IPv6 提供資料。

-   [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    **IpAddess** 屬性包含 ipv6 網路中電腦的 ipv6 位址。

-   [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) 可以傳回 IPv4 或 IPv6 位址的資料。

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>對 WMI 的 IPv4 和 IPv6 連線

連接至遠端電腦上的 WMI 命名空間時，目的電腦必須執行與連接電腦相同的 IP 軟體。 例如，執行 IPv4 的電腦無法連線到執行 IPv6 的電腦，即使在呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)、 [**wbemscripting.swbemlocator ConnectServer**](swbemlocator-connectserver.md)或使用「標記」連接的情況下，使用電腦名稱稱嘗試連接也是一樣 `winmgmts` 。 相反的情況也是如此：只執行 IPv6 的電腦無法連線到只執行 IPv4 的電腦。

如果目的電腦同時執行 IPv4 和 IPv6，則可以從執行任一 IP 軟體的電腦進行連線。 您可以在與 WMI 命名空間的連線中，提供 IPv4 或 IPv6 格式的電腦名稱稱或 IP 位址。

同時執行 IPv4 和 IPv6 並連接到只執行 IPv4 或僅 IPv6 的目的電腦的電腦，必須為目的電腦 IP 軟體提供適當的格式的 IP 位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> </dl>

 

 
