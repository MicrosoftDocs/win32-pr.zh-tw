---
title: 關於 NAP
description: 關於 NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671416"
---
# <a name="about-nap"></a>關於 NAP

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

網路存取保護 (NAP) 的設計目的是協助系統管理員維護網路上電腦的健康狀態，進而協助維護網路的整體完整性。 它並非設計用來保護網路免于惡意使用者的攻擊。 例如，如果電腦具有網路存取原則所需的所有軟體和設定，則電腦會被視為狀況良好或符合規範，而且會被授與適當的網路存取權。 NAP 不會防止有合格電腦的授權使用者將惡意程式上傳到網路，或不適當的行為。

為了保護網路的存取，網路基礎結構必須提供下列功能區域：

-   健全狀況驗證：判斷電腦是否符合系統健康需求。
-   網路限制：限制不符合系統健康需求之用戶端的網路或通訊存取權。
-   補救：提供必要的更新，讓電腦能夠更正其不相容的健全狀況狀態。
-   持續合規性：只要使用者的電腦符合健康原則需求，即允許存取網路。

Windows XP （含 Service Pack 3） (SP3) 、Windows Vista 和 Windows Server 2008 提供動態主機設定通訊協定的 NAP 強制方法 (DHCP) 位址設定、遠端存取式虛擬私人網路 (VPN) 連線、IEEE 802.1 X 驗證的有線和無線連線，以及網際網路通訊協定安全性 (IPsec) 為基礎的通訊。 NAP 平臺還支援架構，以供協力廠商軟體廠商或 Microsoft 提供的其他元件支援健康狀態驗證、網路限制、補救和持續合規性。

NAP 平臺包含下列元件：

-   [NAP 用戶端架構](nap-client-architecture.md)
-   [NAP 伺服器端架構](nap-server-side-architecture.md)
-   [NAP 用戶端和伺服器端元件通訊](nap-client-and-server-side-component-communication.md)

NAP 用戶端需要 Windows Vista、Windows XP SP3 或 Windows Server 2008。 DHCP、VPN 和 IPsec 強制的 NAP 健康原則伺服器和 NAP 強制端點需要 Windows Server 2008。

 

 




