---
description: 在用戶端/伺服器應用程式協定中，伺服器系結至通訊埠，例如通訊端或 RPC 介面。
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: 使用驗證建立安全連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985064"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>使用驗證建立安全連線

在用戶端/伺服器 [*應用程式協定*](/windows/desktop/SecGloss/a-gly)中，伺服器系結至通訊埠，例如通訊端或 RPC 介面。 然後伺服器會等候用戶端連接並要求服務。 在相互驗證的情況下，連接設定的安全性角色是雙折迭的角色：

-   伺服器的用戶端驗證。
-   用戶端的伺服器驗證。

傳輸應用程式的用戶端和伺服器元件會使用 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 來建立安全的連接來傳輸訊息。 建立安全連線的第一個步驟是建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly);亦即，包含與連線相關之安全性資料的不透明資料結構，例如 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) 和會話的持續時間。

安全性內容基本上是從與用戶端相關聯之安全性封裝的訊息，與與伺服器相關聯的安全性封裝。 因此，建立安全性內容通常會要求用戶端和伺服器對其各自的安全性套件進行呼叫。 如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。

用來建立安全驗證連線的通訊協定，需要在用戶端與伺服器之間交換一或多個「安全性權杖」。 這些權杖會以不透明訊息的形式連同任何其他 [*應用程式通訊協定*](/windows/desktop/SecGloss/a-gly)特定資訊的形式傳送。 以不透明的訊息而言，用戶端會從安全性封裝函式接收權杖，其無法解讀或變更，而是以訊息的形式轉送至伺服器。 此權杖對伺服器也是不透明的，不能解讀或變更權杖。 伺服器會將不透明的權杖轉送到其安全性封裝以進行解讀。 封裝接著會通知伺服器用戶端驗證，或驗證失敗。

用戶端會在訊息中接收伺服器的權杖、從接收的訊息抓取權杖，並在對其安全性封裝的呼叫中使用該權杖。 然後，用戶端會再次呼叫安全性封裝，指出是否已建立安全連線，或是在安全連線準備就緒之前，是否需要進一步的交換。 理論上，所需的安全性權杖交換數量沒有限制。 在實務上，只需要有限的交換數目。 NTLM 驗證是以挑戰/回應配置為基礎，而且會使用三個腿來驗證服務器的用戶端。 [*Kerberos*](/windows/desktop/SecGloss/k-gly) 5.0 版通訊協定可能需要額外的訊息交換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端內容初始化](client-context-initialization.md)
</dt> <dt>

[伺服器內容初始化](server-context-initialization.md)
</dt> </dl>

 

 
