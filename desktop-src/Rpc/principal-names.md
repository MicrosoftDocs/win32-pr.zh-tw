---
title: 主體名稱
description: 若要讓用戶端使用伺服器程式建立相互驗證的會話，則必須提供伺服器的預期主體名稱。
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462412"
---
# <a name="principal-names"></a>主體名稱

若要讓用戶端使用伺服器程式建立相互驗證的會話，則必須提供伺服器的預期主體名稱。 某些通訊協定（例如 Kerberos）要求任何已驗證會話的伺服器主體名稱都是正確的。 主體是安全性系統可辨識的實體。 這包括人類使用者和系統服務。 針對指定的安全性支援提供者， (SSP) 的所有主體名稱都採用類似的格式。 SSP 是執行安全性驗證的軟體模組。 如需詳細資訊，請參閱 [SSPI 架構總覽](sspi-architectural-overview.md)。 為了維持一致性，安全性提供者通常會提供類似于使用者的系統服務名稱。 在某些安全性提供者下，系統服務可能沒有主體名稱。

伺服器使用 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式來註冊安全性提供者的主體名稱。 每個安全性提供者都只能使用一個伺服器主體名稱。 如果註冊了多個名稱，則會隨機播放並使用一個名稱。 SSP 規定主體名稱的格式。 例如，系統服務的 Kerberos/Negotiate Ssp 看起來大約像下面這樣：機器 \_ 名稱 $ @childdomain.parentdomain1.parentdomain2.COM 。

產生主體名稱的建議程式是使用已記載的 Api (例如 **DsMakeSpn** 函式) ，而不是從字串將主體名稱 piecing 在一起。 使用記載的 Api 可提高不同部署環境之間的可攜性，並消除錯誤的可能性。

指定不正確的主體名稱，可能會讓用戶端和伺服器無法建立已驗證的會話。 安全通道 SSP 採用兩種形式的主體名稱：

-   第一個 SCHANNEL 主體名稱表單是 [*msstd*](m-glos.md) 格式。 Msstd 表單中的名稱通常會遵循模式 msstd:servername@serverdomain.com 。 這稱為 [電子郵件名稱] 屬性。 如果憑證包含 [電子郵件名稱] 屬性，而且它包含 @ ) 的 @ ( 符號，則主體名稱是 msstd： email name。 否則，它必須包含 [一般名稱] 屬性。 內部反斜線是雙反斜線，就像在字串系結中一樣。
-   第二個 SCHANNEL 主體名稱表單是 [*fullsic*](f-glos.md) 格式。 這是一系列 RFC1779 相容的名稱，以角括弧括住，並以反斜線分隔。 它通常會遵循模式 fullsic： \\ < \\ 授權單位 \\ SubAuthority \\ ... \\ 。Person> 或 fullsic： \\ < \\ 授權單位 \\ SubAuthority \\ ... \\ServerProgram>。

如果名稱與憑證不符， \_ \_ 則會傳回拒絕存取錯誤。 如果名稱格式無效，則 SCHANNEL SSP 會傳回程序代碼錯誤 \_ 不正確 \_ 參數。

若要查詢伺服器的主體名稱，應用程式可以呼叫 [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)。 這會配置以 null 終止的字串來保存主體名稱。 在結束之前，您的應用程式必須叫用 [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) 來釋放此字串所佔用的記憶體。

以這種方式查詢伺服器名稱並不安全，應予以避免。 針對伺服器驗證，用戶端程式應該知道它所連接的伺服器，而且應該從頭建立伺服器主體名稱。

 

 




