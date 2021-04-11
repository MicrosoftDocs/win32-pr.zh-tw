---
title: 在 Windows XP 中使用 Teredo
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 深入瞭解：在 Windows XP 中使用 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027484"
---
# <a name="using-teredo-in-windows-xp"></a>在 Windows XP 中使用 Teredo

若要在執行 Windows XP Service Pack 1 的電腦上使用 Teredo 用戶端或主機特定轉送 (SP1) 搭配 Advanced 網路套件、Windows XP Service pack 2 (SP2) 、Windows Server 2003 （含 Service pack 1） (SP1) 或 Windows Server 2003 Service Pack 2 (SP2) ，應用程式開發人員必須執行下列動作：

-   使用新的 Windows 通訊端2程式設計項目， (可同時支援 IPv4 和 IPv6) 的函式和結構，確保應用程式與 IPv6 相容。 如需詳細資訊，請參閱 [Windows 通訊端應用程式的 IPv6 指南](../winsock/ipv6-guide-for-windows-sockets-applications-2.md)。
-   藉由將 [IPV6 \_ 保護 \_ 等級 Windows 通訊端通訊端] 選項設定為保護層級不 \_ \_ 受限制的層級，啟用在應用程式中使用 Teredo。 如需詳細資訊，請參閱 [使用 IPV6 \_ 保護 \_ 層級](/previous-versions/aa916826(v=msdn.10))。 您也可以透過 .NET Framework 類別的 [系統 .net](/dotnet/api/system.net.sockets?view=netcore-3.1) 來設定此選項。
-   建立 Windows 防火牆的例外狀況，以允許未經要求的連入 Teredo 流量。 您可以使用 [Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page) api，針對指派給 Teredo 流量的 UDP 埠建立埠例外狀況。 如需詳細資訊和範例，以詳述 Teredo 的必要安全性和流量考慮，請參閱 [使用 teredo](using-teredo.md)。

為了確保在應用程式執行時可以使用 Teredo，應用程式開發人員應在應用程式的安裝過程中執行下列作業：

-   使用 **netsh interface ipv6 install** 命令安裝 IPv6。 Windows 防火牆會以與 IPv4 流量相同的方式，保護使用者的電腦免于未經要求的連入 IPv6 流量。
-   使用 **netsh interface ipv6 set teredo 用戶端** 命令啟用 Teredo。

（選擇性）您可以測試每次應用程式執行時是否安裝 IPv6，並視需要安裝 IPv6 並啟用 Teredo。 您也應該通知使用者正在安裝 IPv6，而且正在啟用 Teredo。

 

 
