---
description: 模擬的 Server-Side 需求
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: 模擬的 Server-Side 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971315"
---
# <a name="server-side-requirements-for-impersonation"></a>模擬的 Server-Side 需求

伺服器會以程式設計的方式執行模擬。 它會使用 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)明確地假設用戶端的安全性認證。 當用戶端授與伺服器足夠的授權單位時，這會產生將用戶端的安全性認證取代為伺服器執行緒權杖的效果，以取代處理常式權杖。

例如，伺服器可以使用用戶端權杖來存取受安全描述項保護的資源。 或者，如果已啟用掩蓋，也可以在用戶端身分識別下進行呼叫。

伺服器可以用程式設計的方式明確設定掩蓋，也可以依賴系統管理設定。 根據預設，COM + 應用程式會設定為使用動態掩蓋。 如需詳細資訊，請參閱「 [掩蔽](cloaking.md)」。

如果伺服器正在代表用戶端執行委派（使用用戶端身分識別透過網路），則伺服器進程身分識別必須在 Active Directory 服務中標示為「受信任的委派」;否則委派會失敗。

當它完成使用用戶端的身分識別時，伺服器可以使用 [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)還原為自己的進程權杖。

如需有關實施模擬和委派的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[模擬的用戶端需求](client-side-requirements-for-impersonation.md)
</dt> <dt>

[隱形](cloaking.md)
</dt> </dl>

 

 
