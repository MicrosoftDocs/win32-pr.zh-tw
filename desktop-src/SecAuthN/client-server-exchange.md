---
description: 用戶端/伺服器 Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: 用戶端/伺服器 Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2401d3cf2bb59586e608bc7566c13009869d2874a1532b659f70c6c4e09e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141171"
---
# <a name="clientserver-exchange"></a>用戶端/伺服器 Exchange

當使用者對伺服器有票證之後，工作站用戶端就可以與該伺服器建立安全的通訊會話。

**若要建立與伺服器的安全通訊會話**

1.  用戶端會將 KRB AP 要求類型的訊息傳送給伺服器， \_ \_ (Kerberos 應用程式要求) 。 此訊息包含驗證器訊息，此訊息會使用 [*金鑰發佈中心*](/windows/desktop/SecGloss/k-gly) (KDC) 針對伺服器的會話、與伺服器會話的票證，以及指出用戶端是否要求相互驗證的旗標所傳送的金鑰進行加密。 設定要求相互驗證的旗標是設定 [*Kerberos*](/windows/desktop/SecGloss/k-gly)的其中一個選項。 系統永遠不會詢問使用者是否應該使用相互驗證。
2.  伺服器會接收 KRB \_ 的 AP 要求 \_ 、解密票證，以及將使用者的授權資料和 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)解壓縮。
3.  伺服器會使用票證中的工作階段金鑰，將使用者的驗證器訊息解密，並評估內的時間戳記。
4.  如果驗證器訊息有效，伺服器會檢查用戶端要求中的相互驗證旗標。
5.  如果設定了相互驗證旗標，伺服器會使用工作階段金鑰來加密使用者驗證器訊息中的時間，並將結果傳回 KRB AP 代表類型的訊息， \_ \_ (Kerberos 應用程式回復) 。
6.  當用戶端收到 KRB \_ AP \_ REP 時，它會使用與伺服器共用的工作階段金鑰將伺服器的驗證器訊息解密，並將服務傳回的時間與原始驗證器訊息中的時間進行比較。 如果兩者相符，用戶端就可以確保服務是正版的，且連接會繼續進行。

 

 
