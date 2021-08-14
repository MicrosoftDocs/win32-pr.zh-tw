---
description: 一組密碼編譯演算法。 安全通道通訊協定會使用加密套件中的演算法來建立金鑰和加密資訊。
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Windows Vista 中的 TLS 加密套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918651"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Windows Vista 中的 TLS 加密套件

加密套件是一組密碼編譯演算法。 安全通道通訊協定會使用加密套件中的演算法來建立金鑰和加密資訊。 加密套件會為下列每個工作指定一種演算法：

-   金鑰交換
-   大量加密
-   訊息驗證

[*金鑰交換演算法*](../secgloss/k-gly.md) 可保護建立共用金鑰所需的資訊。 這些演算法是非對稱的 ([*公開金鑰演算法*](../secgloss/p-gly.md)) ，適用于相對較少量的資料。

大量加密演算法會加密在用戶端與伺服器之間交換的訊息。 這些演算法是 [*對稱*](../secgloss/s-gly.md) 的，且適用于大量的資料。

[訊息驗證](message-authentication-codes-in-schannel.md) 演算法會產生訊息 [*雜湊*](../secgloss/h-gly.md) 和簽章，以確保訊息的 [*完整性*](../secgloss/i-gly.md) 。

開發人員會使用 [**ALG \_ 識別碼**](../seccrypto/alg-id.md) 資料類型來指定這些元素。 如需詳細資訊，請參閱 [指定 Schannel 密碼和加密強度](specifying-schannel-ciphers-and-cipher-strengths.md)。

Schannel 支援下列加密套件。 套件會以 Microsoft Schannel 提供者選擇的預設順序列出。

> [!IMPORTANT]
> HTTP/2 web 服務因非 HTTP/2 相容的加密套件而失敗。 若要確保您的 web 服務可與 HTTP/2 用戶端和瀏覽器搭配運作，請參閱 [如何部署自訂的加密套件順序](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)。

 



| 加密套件                                                 | 已啟用 FIPS 模式 | Exchange              | 加密      | 雜湊            | 通訊協定                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS RSA<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS RSA<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ RC4 \_ 128 SHA 的 \_ TLS RSA<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS RSA<br/>               | Yes<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe RSA<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS DHE DSS<br/>           | Yes<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS DHE DSS<br/>           | Yes<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS DHE DSS<br/>          | Yes<br/>    | DH<br/>         | 3DES<br/> | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ RC4 \_ 128 MD5 的 \_ TLS RSA<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ \_ 使用 MD5 的 SSL CK RC4 128 \_<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| \_ \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL CK DES 192 EDE3 CBC<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| \_ \_ 使用 \_ Null MD5 的 \_ TLS RSA<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ Null SHA 的 \_ TLS RSA<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |



 

Schannel 支援下列加密套件;不過，它們預設不存在。 您必須視需要新增它們。 如需如何將加密套件新增至 Schannel 提供者的詳細資訊，請參閱排列 [Schannel 加密套件的優先順序](prioritizing-schannel-cipher-suites.md)。

-   \_ \_ \_ 使用 \_ RC4 \_ 40 \_ MD5 的 TLS RSA 匯出
-   \_ \_ \_ 使用 \_ RC4 \_ 56 \_ SHA 的 TLS RSA EXPORT1024
-   \_ \_ \_ 使用 \_ DES \_ CBC \_ SHA 的 TLS RSA EXPORT1024
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL CK DES 64 CBC
-   \_ \_ 使用 \_ DES \_ CBC SHA 的 \_ TLS RSA
-   \_ \_ 使用 \_ Null MD5 的 \_ TLS RSA
-   \_ \_ 使用 \_ Null SHA 的 \_ TLS RSA
-   \_ \_ \_ \_ 具有 \_ DES \_ CBC \_ SHA 的 TLS DHE DSS EXPORT1024
-   \_ \_ \_ 具有 \_ DES \_ CBC \_ SHA 的 TLS DHE DSS

**Windows Server 2003 和 Windows XP：** 如需支援的加密套件的詳細資訊，請參閱下列主題。

| 主題                                                                         | 描述                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS 加密套件](tls-cipher-suites.md)<br/>                         | Windows Server 2003 和 Windows XP 中的 TLS 通訊協定可用之加密套件的相關資訊。<br/>              |
| [安全通訊端層通訊協定](secure-sockets-layer-protocol.md)<br/> | SSL 2.0 和3.0 的一般資訊，包括 Windows Server 2003 和 Windows XP 中的可用加密套件。<br/> |



 

 

 
