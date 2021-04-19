---
description: 加密套件是一組密碼編譯演算法。
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: TLS/SSL (Schannel SSP) 的加密套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986454"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>TLS/SSL (Schannel SSP) 的加密套件

加密套件是一組密碼編譯演算法。 TLS/SSL 通訊協定的安全通道 SSP 執行會使用加密套件中的演算法來建立金鑰和加密資訊。 加密套件會為下列每個工作指定一種演算法：

-   金鑰交換
-   大量加密
-   訊息驗證

[*金鑰交換演算法*](/windows/desktop/SecGloss/k-gly) 可保護建立共用金鑰所需的資訊。 這些演算法是非對稱的 ([*公開金鑰演算法*](/windows/desktop/SecGloss/p-gly)) ，適用于相對較少量的資料。

大量加密演算法會加密在用戶端與伺服器之間交換的訊息。 這些演算法是 [*對稱*](/windows/desktop/SecGloss/s-gly) 的，且適用于大量的資料。

[訊息驗證](message-authentication-codes-in-schannel.md) 演算法會產生訊息 [*雜湊*](/windows/desktop/SecGloss/h-gly) 和簽章，以確保訊息的 [*完整性*](/windows/desktop/SecGloss/i-gly) 。

開發人員會使用 [**ALG \_ 識別碼**](/windows/desktop/SecCrypto/alg-id) 資料類型來指定這些元素。 如需詳細資訊，請參閱 [指定 Schannel 密碼和加密強度](specifying-schannel-ciphers-and-cipher-strengths.md)。

在舊版的 Windows 中，TLS 加密套件和橢圓形曲線是使用單一字串來設定的：

![顯示密碼套件單一字串的圖表。](images/tls-cipher-suite.png)

不同的 Windows 版本支援不同的 TLS 加密套件和優先權順序。 請參閱對應的 Windows 版本，以取得 Microsoft Schannel 提供者選擇的預設順序。

**Windows Server 2022：** 如需支援的加密套件的相關資訊，請參閱 [Windows Server 2022 中的 TLS 加密套件](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10，版本1903：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1903 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10 版本1809：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1809 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10，版本1803：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1803 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10，版本1709：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1709 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10，版本1703：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1703 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 和 Windows 10 1607 版：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1607 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10，版本1511：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1511 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10，版本1507：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1507 中的 TLS 加密套件](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 和 Windows 8.1：** 如需支援的加密套件的相關資訊，請參閱 [Windows 8.1 中的 TLS 加密套件](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 和 Windows 8：** 如需支援的加密套件的相關資訊，請參閱 [Windows 8 中的 TLS 加密套件](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 和 windows 7：** 如需支援的加密套件的相關資訊，請參閱 [Windows 7 中的 TLS 加密套件](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 和 Windows Vista：** 如需支援的加密套件的相關資訊，請參閱 [Windows Vista 中的 TLS 加密套件](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 和 WINDOWS XP：** 如需支援的加密套件的詳細資訊，請參閱下列主題。

| 主題                                                                         | 描述                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS 加密套件](tls-cipher-suites.md)<br/>                         | 有關 Windows Server 2003 和 Windows XP 中的 TLS 通訊協定所提供之加密套件的資訊。<br/>              |
| [安全通訊端層通訊協定](secure-sockets-layer-protocol.md)<br/> | SSL 2.0 和3.0 的一般資訊，包括 Windows Server 2003 和 Windows XP 中的可用加密套件。<br/> |



 

> [!Note]  
> 在 Windows 10 之前，會使用橢圓曲線附加加密套件字串來決定曲線的優先順序。 Windows 10 支援橢圓曲線優先順序順序設定，因此不需要橢圓曲線尾碼，而是在提供時由新的橢圓曲線優先順序順序覆寫，以允許組織使用群組原則，以相同的加密套件來設定不同版本的 Windows。

 

