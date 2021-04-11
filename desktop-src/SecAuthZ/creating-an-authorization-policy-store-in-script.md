---
description: 使用授權管理員 API 在腳本中建立授權原則存放區的指示。
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: 在腳本中建立授權原則存放區
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114540"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>在腳本中建立授權原則存放區

在安裝應用程式之前或期間建立授權原則。

當您使用授權管理員 API 建立授權原則時，請遵循下列主題中提供的指示。



| 主題                                                                                                                  | 描述                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [在腳本中建立授權原則存放區物件](creating-an-authorization-policy-store-object-in-script.md) | 授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。                                                                                                                                       |
| [在腳本中建立應用程式物件](creating-an-application-object-in-script.md)                               | 針對使用授權原則存放區的每個應用程式，您必須建立 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，並將它儲存至原則存放區。                                                                                                |
| [在腳本中定義作業](defining-operations-in-script.md)                                                     | 作業是應用程式的低層級函式或方法。                                                                                                                                                                                              |
| [將作業分組到腳本中的工作](grouping-operations-into-tasks-in-script.md)                               | 工作是應用程式使用者需要完成的高層級動作。 工作是由作業所組成，這是應用程式的低層級函式和方法。                                                                                    |
| [將工作分組到腳本中的角色](grouping-tasks-into-roles-in-script.md)                                         | 角色代表使用者類別以及這些使用者已獲授權執行的工作。                                                                                                                                                                     |
| [在腳本中定義使用者群組](defining-groups-of-users-in-script.md)                                           | [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。 **IAzApplicationGroup** 物件也可以包含其他 **IAzApplicationGroup** 物件做為成員。 |
| [將使用者新增至腳本中的應用程式群組](adding-users-to-an-application-group-in-script.md)                   | 應用程式群組是一組使用者和使用者群組。 應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。 應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。    |



 

 

 



