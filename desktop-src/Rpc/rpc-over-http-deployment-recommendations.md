---
title: RPC over HTTP 部署建議
description: 本節說明使用 RPC over HTTP 時，達到最高安全性和效能的最佳作法和建議的部署設定。
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8871686d1fc8b87bcd6fb7ac4314b1977252f23a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021905"
---
# <a name="rpc-over-http-deployment-recommendations"></a>RPC over HTTP 部署建議

本節說明使用 RPC over HTTP 時，達到最高安全性和效能的最佳作法和建議的部署設定。 此處所找到的各種設定適用于以各種大小、預算和安全性需求為基礎的不同組織。 每個設定也會提供部署考慮，以協助判斷哪一個適用于特定案例。

如需有關高容量 RPC over HTTP 案例的詳細資訊，請參閱 [MICROSOFT RPC 負載平衡](rpc-load-balancing.md)。

下列建議適用于所有設定：

-   使用支援 RPC over HTTP v2 的 Windows 版本。
-   將 IIS 放在執行 RPC Proxy 的電腦上（IIS 6.0 模式）。
-   不允許匿名存取 RPC Proxy 虛擬目錄。
-   絕不啟用 AllowAnonymous 登錄機碼。
-   讓 RPC over HTTP 用戶端使用 **CertificateSubjectField** (如需詳細) 資訊，請參閱 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) ，以確認您所連線的 rpc proxy 是您預期的 rpc proxy。
-   將 **ValidPorts** 登錄機碼設定為僅包含 RPC over HTTP 用戶端將連接的電腦。
-   請勿在 **ValidPorts** 索引鍵中使用萬用字元;這麼做可以節省時間，但完全未預期的電腦也可以容納萬用字元。
-   在 RPC over HTTP 用戶端上使用 SSL。 如果遵循這些章節中所述的指導方針，RPC over HTTP 用戶端將無法在不使用 SSL 的情況下連線。
-   除了使用 SSL 之外，請將 RPC over HTTP 用戶端設定為使用 RPC 加密。 如果 RPC over HTTP 用戶端無法連線到 KDC，則只能使用 Negotiate 和 NTLM。
-   將用戶端電腦設定為使用 NTLMv2。 將 **LMCompatibilityLevel** 登錄機碼設定為2或更高。 如需 **LMCompatibilityLevel** 索引鍵的詳細資訊，請參閱 **msdn.microsoft.com** 。
-   使用上面所述的設定，執行 RPC Proxy 電腦的 web 伺服陣列。
-   在網際網路與 RPC Proxy 之間部署防火牆。
-   為了達到最佳效能，請設定 IIS 以傳送簡短的回應給非成功的錯誤碼。 因為 IIS 回應的取用者是自動化程式，所以不需要將使用者易記的說明傳送給用戶端;RPC over HTTP 用戶端只會略過它們。

從安全性、效能及管理性的觀點來看，RPC Proxy 的基本目標如下：

-   提供 RPC over HTTP 流量進入伺服器網路的單一進入點。 針對 RPC over HTTP 流量進入伺服器網路的單一進入點，有兩個主要優點。 首先，由於 RPC Proxy 是面對網際網路，因此大部分的組織會將這類電腦隔離在稱為不受信任的周邊網路的特殊網路中，這與一般的組織網路不同。 不受信任的周邊網路中的伺服器非常小心地管理、設定和監視，以便能夠承受來自網際網路的攻擊。 不受信任的周邊網路中的電腦越少，設定、管理、監視及保護它們的安全性就越容易。 第二，由於已安裝 RPC Proxy 的單一 Web 伺服陣列可以服務位於公司網路上的任何 RPC over HTTP 伺服器，因此將 RPC Proxy 與 RPC over HTTP 伺服器分開，並讓 RPC Proxy 位於不受信任的周邊網路中是很合理的。 如果 RPC Proxy 與 RPC over HTTP 伺服器位於同一部電腦上，則會強制組織將所有的後端伺服器放入不受信任的周邊網路中，這樣會讓不受信任的周邊網路保持在安全的情況下變得更困難。 將 RPC Proxy 的角色與 RPC over HTTP 伺服器分開，可協助組織讓不受信任的周邊網路中的電腦數目保持可管理，因此更安全。
-   作為伺服器網路的安全保險絲。 RPC Proxy 是設計為伺服器網路的消耗保險絲-如果 RPC Proxy 發生問題，它就會消失，並藉此保護真正的 RPC over HTTP 伺服器。 如果截至目前為止已遵循本節所述的最佳做法，則除了 SSL 之外，RPC over HTTP 流量還會使用 RPC 加密來加密。 RPC 加密本身是在用戶端與伺服器之間，而不是在用戶端和 proxy 之間。 這表示 proxy 不了解，也無法將它所接收的 RPC 流量解密。 它只會瞭解用戶端處理連接建立、流量控制和其他通道詳細資料時，傳送給它的一些控制順序。 它無法存取 RPC over HTTP 用戶端傳送至伺服器的資料。 此外，RPC over HTTP 用戶端必須獨立地對 RPC Proxy 和 RPC over HTTP 伺服器進行驗證。 這可提供深層防禦。 如果 RPC Proxy 電腦因為某些設定錯誤或某種安全性缺口而遭到入侵，通過它的資料仍會受到保護，而不會受到篡改。 攻擊者若要獲得 RPC Proxy 的控制權，最多可以中斷流量，但無法讀取或篡改。 這就是 RPC Proxy 的熔斷器角色進入 play 的地方，它是消耗，而不會危及 RPC over HTTP 流量的安全性。
-   在 Web 伺服陣列中執行 RPC Proxy 的多部電腦之間散發一些存取檢查和解密工作。 藉由在 Web 伺服陣列中運作良好，RPC Proxy 可讓組織卸載 SSL 解密和一些存取檢查，因此可在後端伺服器上釋出更多容量以進行處理。 使用 RPC Proxy 電腦的 Web 伺服陣列，也可讓組織增加其前端伺服器上的容量，藉此提高其承受阻絕服務 (DoS) 攻擊的能力。

在截至目前為止所設定的指導方針中，組織仍有選擇。 每個組織都有使用者的不便、安全性和成本之間的選擇與折衷：

-   **使用基本驗證或 Windows 整合式驗證來驗證 RPC Proxy？** RPC over HTTP 目前僅支援 NTLM-它不支援 Kerberos。 此外，如果 RPC over HTTP 用戶端與在 HTTP 標頭中插入 *via* PRAGMA 的 rpc proxy 之間有 HTTP proxy 或防火牆，則 NTLM 驗證將無法運作。 如果不是這種情況，組織可以選擇基本和 NTLM 驗證。 基本驗證的優點是它的速度更快且更簡單，因此降低了拒絕服務攻擊的機會。 但是 NTLM 更為安全。 視組織的優先順序而定，它可以選擇 [基本]、[NTLM]，或允許其使用者在兩者之間進行選擇。 如果只選擇一個，最好從 RPC Proxy 虛擬目錄關閉另一個，以降低攻擊的風險。
-   **RPC Proxy 和 RPC over HTTP 伺服器使用同一組認證，或針對每個憑證使用不同的認證？** 這項決策的取捨是在使用者的便利性與安全性之間。 少數使用者喜歡輸入多個認證。 但是，如果不受信任的周邊網路發生安全性缺口，則 RPC Proxy 和 RPC over HTTP 伺服器擁有個別的認證集，會提供額外的保護。 請注意，如果使用個別的認證，而且其中一組認證是使用者的網域認證，建議您對 RPC over HTTP 伺服器使用使用者的網域認證，而不是使用 RPC Proxy。

 

 




