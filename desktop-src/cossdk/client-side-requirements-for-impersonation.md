---
description: 模擬的 Client-Side 需求
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: 模擬的 Client-Side 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317940"
---
# <a name="client-side-requirements-for-impersonation"></a>模擬的 Client-Side 需求

您可以針對用戶端上的模擬指定下列兩個設定：

-   模擬層級，指出用戶端要讓伺服器使用其身分識別的意願。
-   Active Directory 服務中的設定，可將用戶端帳戶標示為「帳戶是機密的，無法委派」，這將會停用委派。

您可以透過各種方式來設定模擬層級。 如果用戶端沒有指出模擬等級，COM 將會使用整個電腦的預設值。 您可以使用 [元件服務] 系統管理工具或 Dcomcnfg.exe 來設定整個電腦的預設值。 用戶端也可以使用 Dcomcnfg.exe 來表示系統管理慣用的模擬等級。

用戶端可以透過程式設計的方式，使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)（相當於 [**IClientSecurity：： SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket)）來表示模擬層級，您可以視需要經常呼叫此層級，或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)，每個進程都可以呼叫一次。

如果用戶端指出委派層級模擬（可授與伺服器的最大授權），則用戶端應該在 Active Directory 服務中正確設定的身分識別下執行，以啟用其身分識別的委派。

如需有關模擬層級和委派運作需求的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。

當然，COM + 應用程式一律可以做為用戶端。 當 COM + 應用程式呼叫另一個應用程式或資源時，它會表示模擬層級。 針對 COM + 伺服器應用程式，您可以設定模擬層級的系統管理員。 COM + 程式庫應用程式無法設定自己的模擬層級;它們會改用主機進程的。 若要瞭解如何設定 COM + 應用程式的模擬，請參閱 [設定模擬等級](setting-an-impersonation-level.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[隱形](cloaking.md)
</dt> <dt>

[模擬的伺服器端需求](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
