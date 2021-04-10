---
description: 如同所有進程，受保護的伺服器具有主要存取權杖，可描述其安全性內容。
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: 用戶端安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943559"
---
# <a name="the-client-security-context"></a>用戶端安全性內容

如同所有 [*進程*](/windows/desktop/SecGloss/p-gly)，受保護的伺服器具有 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly) ，可描述其 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。 當用戶端連接到受保護的伺服器時，伺服器可能會想要使用用戶端的安全性內容來執行動作，而不是使用伺服器的安全性內容。 例如，當動態資料交換中的用戶端 (DDE) 對話從 DDE 伺服器要求資訊時，伺服器必須確認用戶端是否允許存取訊號。

有兩種方式可讓伺服器在用戶端的安全性內容中採取行動：

-   伺服器進程的執行緒可以模擬用戶端。 在此情況下，伺服器的執行緒具有模擬 [*存取權杖*](/windows/desktop/SecGloss/a-gly) ，可識別用戶端、用戶端群組和用戶端的 [*許可權*](/windows/desktop/SecGloss/p-gly)。 如需詳細資訊，請參閱 [用戶端](client-impersonation.md)模擬。
-   伺服器可以取得用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly) ，並將用戶端記錄到伺服器的電腦上。 這會建立新的登入 [*會話*](/windows/desktop/SecGloss/s-gly) ，並產生用戶端的主要存取權杖。 然後伺服器可以使用用戶端的存取權杖來模擬用戶端，或啟動在用戶端的安全性內容中執行的新進程。 如需詳細資訊，請參閱 [用戶端登入會話](client-logon-sessions.md)。

在大部分的情況下，模擬用戶端就已足夠。 模擬可讓伺服器檢查用戶端對安全物件的存取權、檢查用戶端的許可權，以及產生可識別用戶端的審核記錄專案。 一般來說，只有當伺服器需要使用用戶端的安全性內容來存取網路資源時，才需要啟動用戶端登入會話。

 

 
