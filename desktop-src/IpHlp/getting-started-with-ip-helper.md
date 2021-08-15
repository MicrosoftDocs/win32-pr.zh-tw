---
description: 以下是使用 IP 協助程式開發介面 (API) 來開始進行程式設計的逐步指南。 它的設計目的是要讓您瞭解基本 IP Helper 函式和資料結構，以及它們如何一起運作。
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: 使用 IP Helper 的開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ca2df12a7d2d2cbd2d0a64f1da07c8aeecd4980fea791bfc19ca018cd87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014156"
---
# <a name="getting-started-with-ip-helper"></a>使用 IP Helper 的開始使用

以下是使用 IP 協助程式開發介面 (API) 來開始進行程式設計的逐步指南。 它的設計目的是要讓您瞭解基本 IP Helper 函式和資料結構，以及它們如何一起運作。

用於說明的應用程式是非常基本的 IP Helper 應用程式。 Microsoft Windows 軟體開發套件 (SDK) 隨附的範例包含更先進的程式碼範例。

大部分 IP 協助程式應用程式的第一個步驟都是相同的。

-   [建立基本 IP 協助程式應用程式](creating-a-basic-ip-helper-application.md)

下列各節說明建立此基本 IP 協助程式應用程式的其餘步驟。

-   [使用 GetNetworkParams 抓取資訊](retrieving-information-using-getnetworkparams.md)
-   [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)
-   [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)
-   [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)
-   [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [使用 GetIpStatistics 抓取資訊](retrieving-information-using-getipstatistics.md)
-   [使用 GetTcpStatistics 抓取資訊](retrieving-information-using-gettcpstatistics.md)

此基本 IP Helper 範例的完整原始程式碼。

-   [完整 IP 協助程式的原始程式碼](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Advanced IP Helper 範例

Microsoft Windows 軟體開發套件 (SDK) 包含數個更先進的 IP 協助程式範例。 根據預設，IP 協助程式範例的原始程式碼是由針對下列目錄中的 Windows 7 發行 Windows SDK 所安裝：

*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ NetDs \\ IPHelp*

以下是在下列目錄中找到的更先進範例：

-   EnableRouter

    此目錄包含的範例會示範如何使用 [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) 和 [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP 協助程式功能，在本機電腦上啟用和停用 IPv4 轉送。

-   iparp

    此目錄包含一個範例程式，示範如何使用 IP 協助程式函式，在本機電腦上顯示和操作 IPv4 ARP 資料表中的專案。

-   ipchange

    此目錄包含一個範例程式，示範如何使用 IP Helper 函式，以程式設計方式變更您電腦上特定網路介面卡的 IP 位址。 此程式也會示範如何取出現有的網路介面卡 IP 設定資訊。

-   IPConfig

    此目錄包含一個範例程式，示範如何以程式設計方式抓取類似 IPCONFIG.EXE 公用程式的 IPv4 設定資訊。 它會示範如何使用 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 和 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 函數。 請注意， **GetAdaptersInfo** 函數只會取出 IPv4 資訊。

-   IPRenew

    此目錄包含一個範例程式，示範如何以程式設計方式釋放和更新透過 DHCP 取得的 IPv4 位址。 此程式也會示範如何取出現有的網路介面卡設定資訊。

-   IPRoute

    此目錄包含一個範例程式，示範如何使用 IP Helper 函式來操作 IPv4 路由表。

-   ipstat

    此目錄包含一個範例程式，示範如何使用 IP Helper 函式來顯示通訊協定的 IPv4 連線。 根據預設，會顯示 IP、ICMP、TCP 和 UDP 的統計資料。

-   Netinfo

    此目錄包含一個範例程式，示範如何使用 Windows Vista 和更新版本引進的新 IP 協助程式 api 來顯示/變更 IPv4 和 IPv6 的位址和介面資訊。

 

 



