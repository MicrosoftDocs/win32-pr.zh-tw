---
description: 瞭解 Windows 10 v1903、v1909 和 v2004 中的 TLS 加密套件。 加密套件只能針對支援的 TLS 版本進行協商。
title: Windows 10 v1903、v1909 和 v2004 中的 TLS 加密套件
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 8bfea2623a7935ec64c4cc1ef1e04271d4227b3c
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262340"
---
# <a name="tls-cipher-suites-in-windows-10-v1903-v1909-and-v2004"></a>Windows 10 v1903、v1909 和 v2004 中的 TLS 加密套件

加密套件只能針對支援的 TLS 版本進行協商。 在 TLS 信號交換中，一律偏好最高支援的 TLS 版本。

加密套件的可用性應以下列兩種方式之一來控制：

-   設定優先順序清單時，會覆寫預設優先權順序。 不在優先順序清單中的加密套件將不會使用。
-   當應用程式傳遞 .SCH \_ 使用強式加密時允許 \_ \_ ： Microsoft 安全通道提供者會在應用程式使用 .sch 時，篩選出已知的弱式加密套件（ \_ 使用強式 \_ \_ 加密旗標）。 RC4、DES、匯出和 null 加密套件會被篩選掉。

> [!IMPORTANT]
> HTTP/2 web 服務因非 HTTP/2 相容的加密套件而失敗。 若要確保您的 web 服務可與 HTTP/2 用戶端和瀏覽器搭配運作，請參閱 [如何部署自訂的加密套件順序](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)。

 

FIPS 合規性已變得更複雜，因為在此資料表的舊版中，讓 FIPS 模式啟用的資料行誤導。 例如，使用 NIST 橢圓曲線時，加密套件（例如 TLS \_ >ecdhe \_ RSA \_ 與 \_ AES \_ 128 \_ CBC \_ SHA256）只是 FIPS 投訴。 To find out which combinations of elliptic curves and cipher suites will be enabled in FIPS mode, see section 3.3.1 of [Guidelines for the Selection, Configuration, and Use of TLS Implementations]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r2.pdf).

針對 Windows 10、1903、1909和2004版，預設會啟用下列加密套件，並依預設使用 Microsoft Schannel 提供者：



| 加密套件字串                                                                                 | .SCH 允許 \_ 使用 \_ 強式 \_ 加密 | TLS/SSL 通訊協定版本                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS >ecdhe ECDSA<br/>                                           | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS >ecdhe ECDSA<br/>                                           | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS >ecdhe RSA<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS >ecdhe RSA<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS DHE RSA<br/>                                               | 否<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS DHE RSA<br/>                                               | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 的 TLS >ecdhe ECDSA<br/>                                           | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS >ecdhe ECDSA<br/>                                           | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 的 TLS >ecdhe RSA<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS >ecdhe RSA<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS >ecdhe ECDSA<br/>                                              | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS >ecdhe ECDSA<br/>                                              | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS >ecdhe RSA<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS >ecdhe RSA<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS RSA<br/>                                                    | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS RSA<br/>                                                    | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA256 的 TLS RSA<br/>                                                    | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS RSA<br/>                                                    | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS RSA<br/>                                                       | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS RSA<br/>                                                       | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS RSA<br/>                                                      | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ 使用 \_ Null SHA256 的 \_ TLS RSA <br/> 只有在應用程式明確要求時才會使用。<br/> | 否<br/>                       | TLS 1.2<br/>                            |
| \_ \_ 使用 \_ Null SHA 的 \_ TLS RSA <br/> 只有在應用程式明確要求時才會使用。<br/>    | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |



 

Microsoft Schannel 提供者支援下列加密套件，但預設不會啟用：



| 加密套件字串                                                                               | .SCH 允許 \_ 使用 \_ 強式 \_ 加密 | TLS/SSL 通訊協定版本                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS DHE RSA<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS DHE RSA<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA256 的 TLS DHE DSS<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS DHE DSS<br/>                                             | 是<br/>                      | TLS 1.2<br/>                            |
| \_ \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1。0<br/>          |
| \_ \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                               | 是<br/>                      | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ RC4 \_ 128 SHA 的 \_ TLS RSA<br/>                                                          | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ RC4 \_ 128 MD5 的 \_ TLS RSA<br/>                                                          | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ DES \_ CBC SHA 的 \_ TLS RSA<br/>                                                          | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 具有 \_ DES \_ CBC \_ SHA 的 TLS DHE DSS<br/>                                                     | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ （ \_ DES \_ CBC \_ SHA）沒有 tls 1.2、tls 1.1、tls 1.0、SSL 3。0<br/>   | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ 使用 \_ Null MD5 的 \_ TLS RSA <br/> 只有在應用程式明確要求時才會使用。 <br/> | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ RC4 \_ 56 \_ SHA 的 TLS RSA EXPORT1024<br/>                                               | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ RC4 \_ 40 \_ MD5 的 TLS RSA 匯出<br/>                                                   | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |
| \_ \_ \_ 使用 \_ DES \_ CBC \_ SHA 的 TLS RSA EXPORT1024<br/>                                              | 否<br/>                       | TLS 1.2、TLS 1.1、TLS 1.0、SSL 3。0<br/> |



 

使用 Microsoft Schannel 提供者時，預設會啟用下列 PSK 加密套件，並依此優先順序排列：



| 加密套件字串                              | .SCH 允許 \_ 使用 \_ 強式 \_ 加密 | TLS/SSL 通訊協定版本 |
|--------------------------------------------------|-------------------------------------|---------------------------|
| \_ \_ 使用 \_ AES \_ 256 \_ GCM \_ SHA384 的 TLS PSK<br/> | 是<br/>                      | TLS 1.2<br/>        |
| \_ \_ 使用 \_ AES \_ 128 \_ GCM \_ SHA256 的 TLS PSK<br/> | 是<br/>                      | TLS 1.2<br/>        |
| \_ \_ 使用 \_ AES \_ 256 \_ CBC \_ SHA384 的 TLS PSK<br/> | 是<br/>                      | TLS 1.2<br/>        |
| \_ \_ 使用 \_ AES \_ 128 \_ CBC \_ SHA256 的 TLS PSK<br/> | 是<br/>                      | TLS 1.2<br/>        |
| \_ \_ 具有 Null 的 TLS PSK \_ \_ SHA384<br/>          | 否<br/>                       | TLS 1.2<br/>        |
| \_ \_ 具有 \_ Null SHA256 的 \_ TLS PSK<br/>          | 否<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> 預設不會啟用 PSK 加密套件。 應用程式只需要使用 .SCH \_ USE PRESHAREDKEY 要求 PSK \_ \_ 。 如需 Schannel 旗標的詳細資訊，請參閱 [**schannel \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred)認證。

 

若要新增加密套件，請部署群組原則或使用 TLS Cmdlet：

-   若要使用 [群組原則]，請在 [電腦設定] 下設定 SSL 密碼套件順序 > 系統管理範本 > 網路 > SSL 設定] 設定，以及您想要啟用之所有加密套件的優先順序清單。
-   若要使用 PowerShell，請參閱 [TLS Cmdlet](/powershell/module/tls/?view=win10-ps)。

> [!Note]  
> 在 Windows 10 之前，會使用橢圓曲線附加加密套件字串來決定曲線的優先順序。 Windows 10 支援橢圓曲線優先順序順序設定，因此不需要橢圓曲線尾碼，而是在提供時由新的橢圓曲線優先順序順序覆寫，以允許組織使用群組原則，以相同的加密套件來設定不同版本的 Windows。
