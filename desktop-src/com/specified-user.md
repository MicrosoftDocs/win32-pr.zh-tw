---
title: 指定的使用者
description: 指定的使用者
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966790"
---
# <a name="specified-user"></a>指定的使用者

指定特定使用者 (以及使用者的密碼) 是 COM 伺服器慣用的身分識別。 偏好使用此身分識別的原因是，不需要在執行伺服器的電腦上記錄任何人來執行伺服器，且如果伺服器將其 class factory 註冊為多用途，則每個用戶端都會與伺服器的相同實例進行交談。 如果伺服器有 GUI，您就不應該選擇此身分識別;如果您這麼做，使用者將看不到使用者介面。

這種類型的伺服器具有主要權杖，而且可以存取具有啟動使用者身分識別的伺服器可能無法存取的遠端資源。 如需模擬和存取權杖的詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。

以固定用戶帳戶的身分執行比互動式使用者身分識別更安全，因為只有具有特定使用者密碼的人員才能將此身分識別指派給應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式識別碼](application-identity.md)
</dt> <dt>

[互動式使用者](interactive-user.md)
</dt> <dt>

[正在啟動使用者](launching-user.md)
</dt> <dt>

[服務身分識別](service-identity.md)
</dt> </dl>

 

 




