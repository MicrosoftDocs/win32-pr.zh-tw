---
description: 授權管理員提供彈性的架構，將角色型存取控制整合到應用程式。 它讓使用這些應用程式的系統管理員，透過指派與工作功能相關的使用者角色來提供存取。
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: 授權管理員模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784191"
---
# <a name="authorization-manager-model"></a>授權管理員模型

授權管理員提供彈性的架構，將角色型存取控制整合到應用程式。 它讓使用這些應用程式的系統管理員，透過指派與工作功能相關的使用者角色來提供存取。

授權管理員應用程式會使用授權存放區的形式存放授權原則，授權存放區會儲存在 Active Directory 或 XML 檔案中，並且在執行階段套用授權原則。

然後，應用程式會呼叫執行時間存取檢查方法，以針對授權存放中的原則資訊檢查存取權。

授權原則包含下列部分：

-   [原則存放區、應用程式和範圍](policy-stores--applications--and-scopes.md)
-   [使用者和群組](users-and-groups.md)
-   [作業和工作](operations-and-tasks.md)
-   [角色](roles.md)
-   [商務規則](business-rules.md)
-   [集合](collections.md)

 

 



