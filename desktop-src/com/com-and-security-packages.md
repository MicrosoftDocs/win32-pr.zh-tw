---
title: COM 和安全性封裝
description: Windows 支援 NTLMSSP (LAN Manager 安全性支援提供者) 、Kerberos v5 驗證通訊協定，以及安全通道安全性套件，可提供 PCT 1.0、SSL 2.0、SSL 3.0 和 TLS 1.0 通訊協定。
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968213"
---
# <a name="com-and-security-packages"></a>COM 和安全性封裝

Windows 支援 NTLMSSP (LAN Manager 安全性支援提供者) 、Kerberos v5 驗證通訊協定，以及安全通道安全性套件，可提供 PCT 1.0、SSL 2.0、SSL 3.0 和 TLS 1.0 通訊協定。 此外，也支援使用 Snego 來檢查可用的安全性套件，並選取最適當的套件。

下表顯示各種安全性封裝所支援的驗證層級。



| 伺服器/用戶端驗證                                                                                           | 安全性套件支援                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 兩者都不能取得其他的名稱。<br/>                                                                      | 無<br/>                                                  |
| 用戶端可以驗證服務器，但不是反之亦然。<br/>                                                 | Schannel<br/>                                              |
| 用戶端無法探索伺服器，但是伺服器可以取得用戶端的使用者識別碼。<br/>                    | NTLMSSP<br/>                                               |
| 相互驗證：如果授與許可權，用戶端和伺服器都可以知道另一個的名稱。<br/> | NTLMSSP (本機) 、Kerberos v5 通訊協定和 Schannel<br/> |



 

如需這些安全性封裝的詳細資訊，請參閱本節中的下列主題：

-   [NTLMSSP](ntlmssp.md)
-   [Kerberos v5 通訊協定](kerberos-v5-protocol.md)
-   [頻道](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 





