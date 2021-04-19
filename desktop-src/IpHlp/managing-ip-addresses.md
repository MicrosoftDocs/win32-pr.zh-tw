---
description: IP 協助程式可協助管理與本機電腦上的介面相關聯的 IP 位址。 使用下列段落中所述的功能來管理 IP 位址。
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: 管理 IP 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972024"
---
# <a name="managing-ip-addresses"></a>管理 IP 位址

IP 協助程式可協助管理與本機電腦上的介面相關聯的 IP 位址。 使用下列段落中所述的功能來管理 IP 位址。

[**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable)函式會抓取包含 IP 位址與介面之對應的資料表。 有一個以上的 IP 位址可能與相同的介面相關聯。

使用 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 函式，將 IP 位址新增至特定介面。 若要移除先前使用 **AddIPAddress** 新增的 IP 位址，請使用 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) 函數。

[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式需要本機電腦使用動態主機設定通訊協定 (DHCP) 。 **IpReleaseAddress** 函式會釋放先前從 DHCP 取得的 IP 位址。 **IpRenewAddress** 函式會在特定 IP 位址上更新 DHCP 租用。 DHCP 租用可讓電腦在指定的一段時間內使用 IP 位址。

-   如需涉及 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 的程式碼範例，請參閱 [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)。

-   如需涉及 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 和 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)的程式碼範例，請參閱 [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)。

-   如需涉及 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 的程式碼範例，請參閱 [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)。

 

 



