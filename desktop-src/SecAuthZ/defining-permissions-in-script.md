---
description: 藉由建立授權原則存放區，以使用授權管理員 API 在腳本中定義許可權的指示。
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: 在腳本中定義許可權
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 772c55f453a68e3bf1a4933abc4beb7cf3d65380b3bcf5d2e2c4af2832173b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782099"
---
# <a name="defining-permissions-in-script"></a>在腳本中定義許可權

在授權管理員中，您可以藉由建立授權原則存放區來定義哪些使用者可以存取哪些應用程式資源。

**若要定義存取權限**

1.  建立用來定義授權原則的存放區：<dl>

[在腳本中建立授權原則存放區](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  在特定應用程式的授權原則存放區中建立區段：<dl>

[在腳本中建立應用程式物件](creating-an-application-object-in-script.md)  
    </dl>
3.  定義應用程式用來存取和修改資源的作業：<dl>

[在腳本中定義作業](defining-operations-in-script.md)  
    </dl>
4.  將作業分組為使用者想要執行的高階工作：<dl>

[將作業分組到腳本中的工作](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  定義包含工作群組的角色：<dl>

[將工作分組到腳本中的角色](grouping-tasks-into-roles-in-script.md)  
    </dl>指派給角色的使用者具有執行指派給該角色之任何工作的許可權。
6.  建立腳本，以便在執行時間存取工作的許可權：<dl>

[使用腳本中的商務邏輯來限定存取權](qualifying-access-with-business-logic-in-script.md)  
    </dl>此為選用步驟。
7.  定義使用者群組：<dl>

[在腳本中定義使用者群組](defining-groups-of-users-in-script.md)  
    </dl>然後可以將這些群組指派給角色，以決定可執行檔工作。
8.  將使用者新增至使用者群組：<dl>

[將使用者新增至腳本中的應用程式群組](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



