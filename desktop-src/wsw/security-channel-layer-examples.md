---
title: 安全性通道層範例
description: 下列範例說明通道層的安全性。
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- 安全性範例
- 安全性範例，安裝程式
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d130bc7e0e4250107c6e331a43f7d5a13786929c37bd998177ee587c2f29049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192769"
---
# <a name="security-channel-layer-examples"></a>安全性通道層範例

下列範例說明[通道層](channel-layer-overview.md)中的安全性

透過 TCP 的 Windows 傳輸安全性：用戶端： [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md)。

透過具名管道 Windows 傳輸安全性：用戶端： [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)。

SSL 傳輸安全性：用戶端： [HttpClientWithSslExample](httpclientwithsslexample.md)，伺服器： [HttpServerWithSslExample](httpserverwithsslexample.md)。

透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)，伺服器： [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)。

透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md)，伺服器： [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md)。

透過 SSL 混合模式安全性的使用者名稱： [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md)。 透過 SSL 混合模式安全性發出的權杖： [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md)。 透過 SSL 混合模式安全性的 X509 憑證： [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md)。

## <a name="one-time-setup-for-security-samples"></a>安全性範例的 One-Time 設定

若要執行 WWSAPI 安全性範例，您必須設定 SSL 的用戶端和伺服器憑證，以及用於 HTTP 標頭驗證的本機使用者帳戶。 開始之前，您需要下列工具：

-   Windows 7 SDK 提供 MakeCert.exe (。 ) 
-   從 Windows Server 2003 開始，Windows sdk 中提供 CertUtil.exe 或 CertMgr.exe (CertUtil.exe。 CertMgr.exe 可在 Windows 7 SDK 中取得。 您只需要其中一個工具。 ) 
-   HttpCfg.exe： (只有在使用 Windows 2003 或 Windows XP 時，才需要這麼做。 這項工具可在 Windows XP SP2 支援工具中取得，也隨附于 Windows Server 2003 資源套件工具 CD。 ) 

如果您藉由安裝 Windows 7 SDK 來取得 WWSAPI 的範例，您可以在% ProgramFiles% \\ Microsoft sdk Windows v2.0 bin 下找到 MakeCert.exe 和 CertMgr.exe \\ \\ \\ 。

如果您使用 Windows Vista 和更新版本) ，請從命令提示字元執行下列五步驟安裝 (提高許可權：

1.  產生自我簽署憑證做為憑證授權單位單位 (CA) 或簽發者： **MakeCert.exe-Ss Root-Sr LocalMachine-n "CN = 假-Test-CA"-cy issuer-r-sk "CAKeyContainer"**
2.  使用先前的憑證作為簽發者來產生伺服器憑證： **MakeCert.exe-Ss my-Sr LocalMachine-n "CN = localhost"-天空 exchange-** -----ServerKeyContainer
3.  藉由執行下列其中一個命令，並搜尋名為 localhost 的憑證（具有簽發者虛設-Test-CA），以找出伺服器憑證的40字元 SHA-1 雜湊)  (的指紋：
    -   **CertUtil.exe-儲存我的 localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  使用 HTTP.SYS 註冊伺服器憑證的指紋，但不含空格：
    -   在 Windows Vista 和更新版本上 ("appid" 選項是任意的 GUID) ： **Netsh.exe HTTP add sslcert ipport = 0.0.0.0： 8443 appid = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint>
    -   在 Windows XP 或2003上： **HttpCfg.exe 設定 ssl-i 0.0.0.0： 8443-h <40CharacterThumbprint>**
5.  建立本機使用者： **Net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/add**

若要清除憑證、SSL 憑證系結和在先前步驟中建立的使用者帳戶，請執行下列命令。 請注意，如果有多個相同名稱的憑證，CertMgr.exe 將需要您的輸入，才能將其刪除。

-   **CertMgr.exe-del-c-n 假-測試-CA-s-r LocalMachine Root**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe HTTP delete sslcert ipport = 0.0.0.0： 8443 (或 HttpCfg.exe delete ssl-i 0.0.0.0： 8443)**
-   **Net user "TestUserForBasicAuth"/delete**

請確定只有一個名為假-Test-CA 的根憑證。 如果您不確定，您可以使用上述的 [清除] 命令，一律安全地嘗試清除這些憑證 (並且在開始進行五個步驟的設定之前，先忽略錯誤) 。

 

 




