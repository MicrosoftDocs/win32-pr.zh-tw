---
description: 只有在進行互動式驗證之後，才可以使用非互動式驗證。 在非互動式驗證期間，使用者不會輸入登入資料，而是會使用先前建立的認證。
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: 非互動式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e259a2b14d48f4d7109966fa01f6fbd6a505a1343e90ea312c557ebfb9c84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786609"
---
# <a name="noninteractive-authentication"></a>非互動式驗證

只有在進行 [互動式驗證](interactive-authentication.md) 之後，才可以使用非互動式驗證。 在非互動式驗證期間，使用者不會輸入 [*登入資料*](../secgloss/l-gly.md)，而是會使用先前建立的 [*認證*](../secgloss/c-gly.md) 。

當應用程式使用 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 和安全性套件來建立安全的網路連線時，就會執行非互動式驗證。 非互動式驗證是一種機制，可讓使用者連接到網路上的多部電腦，而不需要為每部機器重新輸入登入資訊。 例如，如果應用程式需要在遠端電腦上開啟安全資料夾，而且應用程式使用者已經以互動方式登入網域帳戶，則應用程式不會要求使用者重新提供登入資料。 相反地，應用程式可以使用 SSPI 要求非互動式驗證，將先前建立的安全性資訊傳遞到安全性套件。 然後，安全性封裝會使用 LSA 函數來檢查 [*認證*](../secgloss/c-gly.md)。 下圖說明此程式。

![非互動式驗證](images/lsasspi2.png)

在上圖中，用戶端應用程式會起始對 SSPI 的呼叫，要求已驗證的網路連接。 SSPI 會將用戶端的要求傳遞至安全性封裝以進行處理。 安全性套件會藉由呼叫「 [*本地安全機構*](../secgloss/l-gly.md) 」 (LSA) 來驗證使用者，並指定 [*驗證套件*](../secgloss/a-gly.md) 並提供使用者現有的認證。

驗證結果會從 [*驗證套件*](../secgloss/a-gly.md)、透過 LSA 傳送到 [*安全性套件*](../secgloss/s-gly.md)，最後傳遞給 SSPI。 SSPI 會通知用戶端應用程式有關要求的結果。

如需 SSPI 的詳細資訊，請參閱 [安全性支援提供者介面](sspi.md)。

 

 
