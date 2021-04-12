---
title: 互動式使用者
description: 互動式使用者是目前登入執行 COM 伺服器之電腦的使用者。
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316519"
---
# <a name="interactive-user"></a>互動式使用者

*互動式使用者* 是目前登入執行 COM 伺服器之電腦的使用者。 如果身分識別設定為互動式使用者，則如果伺服器將其 class factory 註冊為多用途，則所有用戶端都會使用相同的伺服器實例。 如果沒有登入的使用者，伺服器將不會執行。 如果伺服器有圖形化使用者介面 (GUI) 用戶端必須看到，您應該將互動式使用者用於伺服器的身分識別。 不過，選擇此身分識別會帶來一些安全性風險，因為伺服器會在登入使用者的身分識別下執行，而沒有登入使用者的知識或同意。 此外，服務應用程式無法顯示使用者介面。 如需詳細資訊，請參閱 [互動式服務](/windows/desktop/Services/interactive-services)。

如果將 COM 伺服器設定為以互動式使用者的身分執行，則在終端機服務環境中，伺服器將會在符合用戶端使用者身分識別的互動式會話中啟動。 不過，用戶端應用程式可以在不符合用戶端身分識別的會話中，使用會話的標記來參考伺服器所提供的物件。 當使用此項時，用戶端應用程式可以指定任何會話，在這種情況下，伺服器將會以擁有會話的使用者身分執行，而不是啟動的使用者。 此案例中的預設存取權限不允許啟動使用者呼叫伺服器上的方法。 不過，仍會有下列安全性風險：

-   如果 COM 伺服器公開不是由 COM 控制的介面，例如 TCP 埠、具名管道、LPC 埠、共用記憶體區段等等，則啟動使用者可以使用這些介面來影響伺服器。 設定為以互動式使用者的身份執行的 COM 物件應盡可能減少此受攻擊面。
-   COM 物件可自由設定自己的存取權限。 如果物件在其 AppID 註冊中或藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定存取權限，以允許啟動使用者存取，則使用者可以啟動伺服器以另一位使用者的身份執行，然後存取該物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式識別碼](application-identity.md)
</dt> <dt>

[正在啟動使用者](launching-user.md)
</dt> <dt>

[服務身分識別](service-identity.md)
</dt> <dt>

[指定的使用者](specified-user.md)
</dt> </dl>

 

 