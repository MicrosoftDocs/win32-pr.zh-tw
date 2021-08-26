---
title: " (RPC) 的用戶端模擬"
description: 當伺服器必須將用戶端要求傳遞給其他伺服器進程或作業系統時，模擬在分散式運算環境中很有用。
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022820"
---
# <a name="client-impersonation"></a>用戶端模擬

當伺服器必須將用戶端要求傳遞給其他伺服器進程或作業系統時，模擬在分散式運算環境中很有用。 在此情況下，伺服器會模擬用戶端的安全性內容。 然後，其他伺服器進程可以處理要求，就像原始用戶端所做的一樣。

![當代表用戶端進行後續呼叫時，伺服器會模擬呼叫用戶端](images/impr.png)

例如，用戶端會向伺服器 A 提出要求。如果伺服器 A 必須查詢伺服器 B 才能完成要求，伺服器 A 會模擬用戶端安全性內容，並代表用戶端提出對伺服器 B 的要求。 伺服器 B 會使用原始用戶端的安全性內容，而不是伺服器 A 的安全性識別，以判斷是否要完成工作。

伺服器會呼叫 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) ，以使用用戶端安全性內容來覆寫伺服器執行緒的安全性。 工作完成之後，伺服器會呼叫 [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) 或 [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) 來還原為伺服器執行緒定義的安全性內容。

當系結時，用戶端可以指定安全性的服務品質資訊，以指定伺服器如何模擬用戶端。 例如，其中一個設定可讓用戶端指定不允許伺服器模擬該伺服器。 如需詳細資訊，請參閱 [服務品質](quality-of-service.md)。

在模擬原始用戶端時呼叫其他伺服器的功能稱為「 *委派*」。 使用委派時，模擬用戶端的伺服器可以呼叫另一部伺服器，而且可以使用用戶端的認證進行網路呼叫。 也就是說，從第二部伺服器的角度來看，來自第一部伺服器的要求，與來自用戶端的要求並不區分。 並非所有安全性提供者都支援委派。 Microsoft 只提供一個支援委派的安全性提供者： Kerberos。

委派可能是危險的功能，因為用戶端會在遠端程序呼叫期間提供伺服器的許可權。 這就是為什麼 Kerberos 只在要求相互驗證時才允許使用模擬層級的委派呼叫。 網域系統管理員可以限制對委派模擬等級發出呼叫的電腦，以防止不滿意的用戶端呼叫可能會濫用認證的伺服器。

委派規則有一個例外狀況：使用 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)呼叫。 當這些呼叫進行時，伺服器會取得委派許可權，即使已指定模擬的模擬等級也是如此。 也就是說，伺服器可以代表用戶端呼叫其他伺服器。 這僅適用于一個遠端呼叫。 例如，如果用戶端使用 **ncalrpc** 本機伺服器 lb 來呼叫本機伺服器 lb，就可以模擬和呼叫 REMOTE server RB。 RB 將能夠代表用戶端 A 執行動作，但只能在執行 RB 的遠端電腦上執行。 它無法對遠端電腦 C 進行其他網路呼叫，除非 LB 在呼叫 RB 時指定了委派的模擬層級。

> [!Note]  
> 「模擬 *」一詞* 代表兩個重迭的意義。 模擬的第一個含意是代表用戶端進行的一般處理常式。 第二個意義是稱為模擬的特定模擬等級。 文字的內容通常會說明其意義。

 

 

 