---
description: 使用授權管理員 API 在 c + + 中建立授權原則存放區來定義許可權的指示。
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: 在 c + + 中定義許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008c82e74bcd4b4fec714e43c8beb7d8c7e908baaf569ee260559f64ba5bbc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913771"
---
# <a name="defining-permissions-in-c"></a>在 c + + 中定義許可權

在授權管理員中，您可以藉由建立授權原則存放區來定義哪些使用者可以存取哪些應用程式資源。

如需使用 Acl 定義許可權的相關資訊，請參閱 [在 c + + 中使用 Acl 定義許可權](defining-permissions-with-acls-in-c--.md)。

**若要定義存取權限**

1.  建立用來定義授權原則的存放區：<dl>

[在 c + + 中建立授權原則存放區物件](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  在特定應用程式的授權原則存放區中建立區段：<dl>

[在 c + + 中建立應用程式物件](creating-an-application-object-in-c--.md)  
    </dl>
3.  定義應用程式用來存取和修改資源的作業：<dl>

[在 c + + 中定義作業](defining-operations-in-c--.md)  
    </dl>
4.  將作業分組為使用者想要執行的高階工作：<dl>

[在 c + + 中將作業分組為工作](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  定義包含工作群組的角色：<dl>

[在 c + + 中將工作分組為角色](grouping-tasks-into-roles-in-c--.md)  
    </dl>指派給角色的使用者具有執行指派給該角色之任何工作的許可權。
6.  建立腳本，以便在執行時間存取工作的許可權：<dl>

[在 c + + 中使用商務邏輯來限定存取權](qualifying-access-with-business-logic-in-c--.md)  
    </dl>此為選用步驟。
7.  定義使用者群組：<dl>

[在 c + + 中定義使用者群組](defining-groups-of-users-in-c--.md)  
    </dl>然後可以將這些群組指派給角色，以決定可執行檔工作。
8.  將使用者新增至使用者群組：<dl>

[在 c + + 中將使用者新增至應用程式群組](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



