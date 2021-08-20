---
title: Proxy 伺服器和 WinRM
description: Windows遠端系統管理 (WinRM) 會使用 HTTP 和 HTTPS 在用戶端與伺服器電腦之間傳送訊息。 一般而言，WinRM 用戶端會將訊息直接傳送至 WinRM 伺服器。 WinRM 用戶端也可以設定為使用 proxy 伺服器。
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663493f9c3e71e44be000f436ad4573f911652a8e142b77ffab41acbff250b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112936"
---
# <a name="proxy-servers-and-winrm"></a>Proxy 伺服器和 WinRM

Windows遠端系統管理 (WinRM) 會使用 HTTP 和 HTTPS 在用戶端與伺服器電腦之間傳送訊息。 一般而言，WinRM 用戶端會將訊息直接傳送至 WinRM 伺服器。 WinRM 用戶端也可以設定為使用 proxy 伺服器。

如需詳細資訊，請參閱下列各節：

-   [設定 WinRM 2.0 的 Proxy 伺服器](#configuring-a-proxy-server-for-winrm-20)
    -   [以 HTTPS 為基礎的 Proxy 連接](#https-based-proxy-connections)
    -   [以 HTTP 為基礎的 Proxy 連接](#http-based-proxy-connections)
-   [設定 WinRM 1.1 及更早版本的 Proxy 伺服器](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>設定 WinRM 2.0 的 Proxy 伺服器

WinRM 2.0 支援廣泛的 proxy 設定。 例如，WinRM 支援 HTTP 和 HTTPS 傳輸的 proxy，以及已驗證和未驗證的 proxy 伺服器。

### <a name="https-based-proxy-connections"></a>HTTPS-Based Proxy 連接

為了獲得更好的安全性和以連線為基礎的親和性，應使用 HTTPS 作為傳輸機制。

如果 proxy 伺服器需要驗證，則 WinRM 用戶端和伺服器必須使用 HTTPS。

> [!Note]  
> Proxy 伺服器的驗證與目的地伺服器的驗證無關。

 

### <a name="http-based-proxy-connections"></a>HTTP-Based Proxy 連接

如果不需要 proxy 伺服器驗證，可以使用 HTTP 或 HTTPs 進行傳輸。 不過，透過 proxy 伺服器從 WinRM 用戶端到 WinRM 伺服器的 HTTP 型連線可能會有問題。

使用以 HTTP 為基礎的連接時可能會發生下列問題：

-   Proxy 伺服器不支援以連線為基礎的驗證，這可能會導致目的地伺服器的驗證失敗，並出現「拒絕存取」錯誤。
-   需要一組以上的認證，才能連接到目的地伺服器和 proxy 伺服器。
-   以 HTTP 為基礎的 proxy 伺服器可能不支援維護相關聯的用戶端和伺服器連接的能力。 如果 proxy 沒有將用戶端高度連結到伺服器並維護 TCP/IP 連接，未經驗證的用戶端可能會取得資料的存取權。 此外，缺乏連接親和性可能會導致伺服器的驗證失敗。

如果必須使用 HTTP 做為傳輸，則 proxy 伺服器應支援下列設定，以達到更好的 WinRM 回應，並防止 WinRM 用戶端的拒絕存取失敗：

-   HTTP/1.1 的支援。 在用戶端與伺服器之間對應連線親和性時，HTTP/1.1 更嚴格。
-   用於協商、Kerberos 和 CredSSP 驗證的連接型驗證。

    要求的驗證需要在用戶端與伺服器之間進行多次來回行程。 驗證 (WinRM) server 將回應傳送給用戶端，而該用戶端不是401回應 (未經授權) ，則會在驗證時完成大部分的驗證。 如果 WinRM 伺服器將回應傳回至不是401回應的用戶端，則 proxy 不應關閉連接。

    在傳送實際的封包資料之前，可以在用戶端與伺服器之間傳送多個要求/回應配對。 WinRM 2.0 使用具有加密的 Negotiate 和 Kerberos 驗證配置，這可能會增加額外的來回行程。 在驗證完成之前，無法將資料傳送至伺服器。

    WinRM 伺服器會傳回200層級的回應，表示驗證已完成。 以 HTTP 為基礎的 proxy 伺服器可能會在收到來自 WinRM 伺服器的200層級回應後，結束以連線為基礎的驗證親和性，並關閉 TCP/IP 連接。 從用戶端到伺服器的最後一次往返不包含原始的要求封包。 如果 proxy 伺服器關閉連線，伺服器將會嘗試重新驗證用戶端，而且用戶端要求可能永遠不會傳送到伺服器。 如果未維護以連線為基礎的親和性，則對目的地伺服器的驗證可能會失敗，並出現「拒絕存取」錯誤。

-   連接持續性。 Proxy 的用戶端 TCP/IP 連接應該會繼續對應到伺服器的相同 TCP/IP 連接。」 維護此連線有助於達成更高層級的效能。 如果未維護連接，則每個要求都必須重新驗證，這可能會影響效能。

### <a name="encryption-and-winrm-20"></a>加密和 WinRM 2。0

WinRM 2.0 支援使用 Negotiate、Kerberos 和 CredSSP 驗證配置透過 HTTP 進行加密。 如果 WinRM 伺服器支援 HTTP，而且是透過 proxy 存取，則 WinRM 伺服器必須強制加密，而不允許未加密的網路流量。

在任何情況下，不應該透過 proxy 伺服器傳送未加密的 HTTP 要求。 當資料必須通過 proxy 伺服器才能傳送到目的地伺服器時，下列安全性問題很重要：

-   惡意的 proxy 伺服器可能會檢查每個要求/回應配對，包括認證。
-   如果在 WinRM 用戶端和 proxy 伺服器之間，以及在 proxy 伺服器與目的地伺服器之間，TCP/IP 連接不是強的，則未經授權的用戶端可以使用從 proxy 伺服器到目的地伺服器的相同驗證連線來連線到目的地伺服器。 目的地伺服器可能會允許未經驗證的用戶端存取資料。 如果強制加密，目的地伺服器會將拒絕存取訊息傳送給未經驗證的用戶端。

使用加密可減輕這些潛在的安全性問題。

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>設定 WinRM 1.1 及更早版本的 Proxy 伺服器

如果需要 proxy 才能連線到 winrm 伺服器，winrm 用戶端會依賴 Windows 的 HTTP 服務 (WinHTTP) proxy 設定。 根據預設，WinHTTP 未設定為使用 proxy 伺服器。 您可以使用 [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) 或 [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) 命令列公用程式來變更 WinHTTP proxy 設定。

**WinRM 1.1 及更早版本：** WinRM 不會使用 Internet Explorer proxy 設定。

 

 