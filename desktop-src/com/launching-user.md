---
title: 正在啟動使用者
description: 正在啟動使用者
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e04163d5229942abff55339d53ba37ec0f8bdc6e9ac60b0893f1d243b22643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736534"
---
# <a name="launching-user"></a>正在啟動使用者

這是應用程式識別碼的預設設定。 當針對應用程式的身分識別選擇啟動使用者時，每個用戶端帳戶都會取得伺服器的新實例，且每部伺服器都會取得自己的 [視窗工作站](/windows/desktop/winstation/window-stations)。 由於個別的伺服器實例，啟動使用者是最高層級的安全性保護身分識別設定。 不過，資源耗用量有有限的限制。 此外，用戶端將看不到伺服器所顯示的任何 GUI。

如果應用程式具有啟動使用者的身分識別，則會以模擬權杖執行。 如需模擬和存取權杖的詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式識別碼](application-identity.md)
</dt> <dt>

[互動式使用者](interactive-user.md)
</dt> <dt>

[服務身分識別](service-identity.md)
</dt> <dt>

[指定的使用者](specified-user.md)
</dt> </dl>

 

 