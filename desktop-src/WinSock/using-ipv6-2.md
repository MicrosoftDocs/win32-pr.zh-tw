---
description: 在 Windows XP 上，提供了新的命令列工具來設定和管理 IPv4。 此工具會使用 &\# 0034; netsh interface ip&\# 0034; 命令來設定和管理 IPv4。
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: 使用 IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975275"
---
# <a name="using-ipv6"></a>使用 IPv6

在 Windows XP 上，提供了新的命令列工具來設定和管理 IPv4。 此工具會使用「netsh interface ip」命令來設定和管理 IPv4。

在 Windows XP Service Pack 1 (SP1) 和更新版本中，這個新的命令列工具已增強，可支援 IPv6 的設定和管理。 此增強工具是「netsh interface ipv6」命令。 使用 Netsh.exe 命令所做的設定變更是永久性的，而且在重新開機電腦或 IPv6 通訊協定時不會遺失。

下列命令可在 Windows XP SP1 和更新版本上使用，以在本機電腦上查詢和設定 IPv6：

-   [Netsh.exe](netsh-exe.md)

在 Windows XP Service Pack 1 (SP1) 之前，IPv6 設定和管理使用了數個較舊的命令列工具來設定和管理 IPv6。 使用這些較舊的工具，IPv6 變更不是永久性的，而且會在電腦或 IPv6 通訊協定重新開機時遺失。

Windows XP 上提供下列舊版命令

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Windows 2000 的 IPv6 技術預覽也提供這些舊版工具。

使用這些舊版工具的設定變更，可以藉由將它們作為命令列放在命令腳本檔中， ( .cmd) 在重新開機電腦或 IPv6 通訊協定之後執行。 若要在重新開機後自動復原設定變更，可以在電腦啟動時使用 Windows 排程工作來執行 .cmd 檔。

Windows Server 2003 和更新版本上不提供這些舊版工具。 您可以從 Windows Server 2003 和更新版本的命令列，提供「netsh interface ipv6」工具來設定和管理 IPv6。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網際網路通訊協定第6版 (IPv6) ](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[適用于 Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[適用于 Windows 2000 的 IPv6 技術預覽](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



