---
description: 加密套件只能針對支援的 TLS 版本進行協商。
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: Windows 8 中的 TLS 加密套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8613c018857525f7877e883f21b1eea7bd53e55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851332"
---
# <a name="tls-cipher-suites-in-windows-8"></a>Windows 8 中的 TLS 加密套件

加密套件只能針對支援的 TLS 版本進行協商。 在 TLS 信號交換中，一律偏好最高支援的 TLS 版本。 例如， \_ \_ \_ \_ \_ 只有在用戶端和伺服器都不支援 TLS 1.2、1.1 & 1.0 或 SSL 3.0 （因為只有 SSL 2.0 支援）時，才能使用 ssl CK RC4 128 （具有 MD5）。

加密套件的可用性應以下列兩種方式之一來控制：

-   設定優先順序清單時，會覆寫預設優先權順序。 不在優先順序清單中的加密套件將不會使用。
-   當應用程式傳遞 .SCH \_ 使用 \_ 強式加密時允許 \_ ： Microsoft 安全通道提供者會在應用程式使用 .sch 時，篩選出已知的弱式加密套件（ \_ 使用強式 \_ \_ 加密旗標）。 在 Windows 8 中，RC4 加密套件會被篩選掉。

> [!IMPORTANT]
> HTTP/2 web 服務因非 HTTP/2 相容的加密套件而失敗。 若要確保您的 web 服務可與 HTTP/2 用戶端和瀏覽器搭配運作，請參閱 [如何部署自訂的加密套件順序](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)。

 

FIPS 合規性已變得更複雜，因為在此資料表的舊版中，讓 FIPS 模式啟用的資料行誤導。 例如，使用 NIST 橢圓曲線時，加密套件（例如 TLS \_ >ecdhe \_ RSA \_ 與 \_ AES \_ 128 \_ CBC \_ SHA256）只是 FIPS 投訴。 To find out which combinations of elliptic curves and cipher suites will be enabled in FIPS mode, see section 3.3.1 of [Guidelines for the Selection, Configuration, and Use of TLS Implementations]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

更新優先順序的3042058更新會由 Windows Update 更新 windows 7、Windows 8 和 Windows Server 2012。 如需詳細資訊，請參閱 [Microsoft 資訊安全諮詢 3042058](/security-updates/SecurityAdvisories/2015/3042058) 。 依預設，Microsoft Schannel 提供者預設會啟用下列加密套件，並依此優先順序排列：



| 加密套件字串                                                                                            | .SCH 允許 \_ 使用 \_ 強式 \_ 加密 | TLS/SSL 通訊協定版本                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256 的 TLS >ecdhe RSA<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384 的 TLS >ecdhe RSA<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256 的 TLS >ecdhe RSA<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384 的 TLS >ecdhe RSA<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe RSA<br/>                                                     | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe RSA<br/>                                                     | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe RSA<br/>                                                     | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe RSA<br/>                                                     | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS DHE RSA<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS DHE RSA<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS RSA<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS RSA<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA256 的 TLS RSA<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS RSA<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS RSA<br/>                                                                  | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS RSA<br/>                                                                  | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384 的 TLS >ecdhe ECDSA<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe ECDSA<br/>                                                   | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe ECDSA<br/>                                                   | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P256 的 TLS >ecdhe ECDSA<br/>                                                   | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P384 的 TLS >ecdhe ECDSA<br/>                                                   | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA256 的 TLS DHE DSS<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS DHE DSS<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                             | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                             | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS RSA<br/>                                                                 | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                            | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ RC4 \_ 128 SHA 的 \_ TLS RSA<br/>                                                                       | No<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ RC4 \_ 128 MD5 的 \_ TLS RSA<br/>                                                                       | No<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ Null SHA256 的 \_ TLS RSA <br/> 只有在應用程式明確要求時才會使用。<br/>            | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ Null SHA 的 \_ TLS RSA <br/> 只有在應用程式明確要求時才會使用。<br/>               | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ \_ 使用 MD5 的 SSL CK RC4 128 \_ <br/> 只有在應用程式明確要求時才會使用。<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| \_ \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL CK DES 192 EDE3 CBC <br/> 只有在應用程式明確要求時才會使用。<br/> | Yes<br/>                      | SSL 2.0<br/>                            |



 

Microsoft Schannel 提供者支援下列加密套件，但預設不會啟用：



| 加密套件字串                                             | .SCH 允許 \_ 使用 \_ 強式 \_ 加密 | TLS/SSL 通訊協定版本                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521 的 TLS >ecdhe RSA<br/>   | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521 的 TLS >ecdhe RSA<br/>   | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe RSA<br/>      | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe RSA<br/>      | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521 的 TLS >ecdhe ECDSA<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe ECDSA<br/>    | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA \_ P521 的 TLS >ecdhe ECDSA<br/>    | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ DES \_ CBC SHA 的 \_ TLS RSA<br/>                        | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ RC4 \_ 56 \_ SHA 的 TLS RSA EXPORT1024<br/>             | No<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ DES \_ CBC \_ SHA 的 TLS RSA EXPORT1024<br/>            | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ RC4 \_ 40 \_ MD5 的 TLS RSA 匯出<br/>                 | No<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ Null MD5 的 \_ TLS RSA<br/>                            | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 具有 \_ DES \_ CBC \_ SHA 的 TLS DHE DSS<br/>                   | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ \_ 具有 \_ DES \_ CBC \_ SHA 的 TLS DHE DSS EXPORT1024<br/>       | Yes<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL CK DES 64 CBC<br/>                     | Yes<br/>                      | SSL 2.0<br/>                            |
| \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL CK RC4 128 EXPORT40<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

若要新增加密套件，請使用群組原則設定 [電腦設定] 底下的 SSL 加密套件順序 > 系統管理範本 > 網路 > SSL 設定]，為您要啟用的所有加密套件設定優先順序清單。

 

 
