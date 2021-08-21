---
title: 在 Windows XP 中使用 Teredo
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 深入瞭解：在 Windows XP 中使用 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b488a4825fba8371082d3e538b365e8ec666d000b70ee61d34a640c22775ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856955"
---
# <a name="using-teredo-in-windows-xp"></a>在 Windows XP 中使用 Teredo

若要在執行 Windows XP Service pack 1 (SP1) 的電腦上使用 Teredo 用戶端或主機特定轉送，請使用 Advanced 網路套件、Windows XP service pack 2 (sp2) 、Windows server 2003 service pack 1 (SP1) ，或 Windows server 2003 service pack 2 (sp2) ，應用程式開發人員必須執行下列動作：

-   請確定應用程式與 ipv6 相容，方法是使用新的 Windows 通訊端2程式設計項目 (可支援 IPv4 和 IPv6 的函式和結構) 。 如需詳細資訊，請參閱[Windows 通訊端應用程式的 IPv6 指南](../winsock/ipv6-guide-for-windows-sockets-applications-2.md)。
-   藉由將 IPV6 \_ 保護 \_ 層級 Windows 通訊端通訊端選項設定為保護層級不 \_ \_ 受限制的層級，啟用應用程式中的 Teredo 使用。 如需詳細資訊，請參閱 [使用 IPV6 \_ 保護 \_ 層級](/previous-versions/aa916826(v=msdn.10))。 您也可以透過 .NET Framework 類別的[系統 .net](/dotnet/api/system.net.sockets?view=netcore-3.1)來設定此選項。
-   建立 Windows 防火牆的例外狀況，以允許未經要求的連入 Teredo 流量。 使用[Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page)api，針對指派給 Teredo 流量的 UDP 埠建立埠例外狀況。 如需詳細資訊和範例，以詳述 Teredo 的必要安全性和流量考慮，請參閱 [使用 teredo](using-teredo.md)。

為了確保在應用程式執行時可以使用 Teredo，應用程式開發人員應在應用程式的安裝過程中執行下列作業：

-   使用 **netsh interface ipv6 install** 命令安裝 IPv6。 Windows防火牆會以與 IPv4 流量相同的方式，保護使用者的電腦免于未經要求的連入 IPv6 流量。
-   使用 **netsh interface ipv6 set teredo 用戶端** 命令啟用 Teredo。

（選擇性）您可以測試每次應用程式執行時是否安裝 IPv6，並視需要安裝 IPv6 並啟用 Teredo。 您也應該通知使用者正在安裝 IPv6，而且正在啟用 Teredo。

 

 
