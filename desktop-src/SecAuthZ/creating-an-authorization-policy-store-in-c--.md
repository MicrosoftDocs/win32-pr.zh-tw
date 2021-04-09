---
description: 使用授權管理員 API 在 c + + 中建立授權原則存放區的指示。
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: 在 c + + 中建立授權原則存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114137"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>在 c + + 中建立授權原則存放區

在安裝應用程式之前或期間建立授權原則。

當您使用授權管理員 API 建立授權原則時，請遵循下列主題中提供的指示。



| 主題                                                                                                            | 描述                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [在 c + + 中建立授權原則存放區物件](creating-an-authorization-policy-store-object-in-c--.md) | 授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。 這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。              |
| [在 c + + 中建立應用程式物件](creating-an-application-object-in-c--.md)                               | 授權原則存放區包含一或多個應用程式的授權原則資訊。 針對每個使用該原則存放區的應用程式，您必須建立 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，並將它儲存至原則存放區。 |
| [在 c + + 中定義作業](defining-operations-in-c--.md)                                                     | 在授權管理員中，操作是應用程式的低層級函式或方法。                                                                                                                                                               |
| [在 c + + 中將作業分組為工作](grouping-operations-into-tasks-in-c--.md)                               | 在授權管理員中，工作是應用程式使用者需要完成的高層級動作。 工作是由作業所組成，這是應用程式的低層級函式和方法。                                                     |
| [在 c + + 中將工作分組為角色](grouping-tasks-into-roles-in-c--.md)                                         | 在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。                                                                                                                                      |
| [在 c + + 中定義使用者群組](defining-groups-of-users-in-c--.md)                                           | 在授權管理員中， [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。                                                                       |
| [在 c + + 中將使用者新增至應用程式群組](adding-users-to-an-application-group-in-c--.md)                   | 在授權管理員中，應用程式群組是一組使用者和使用者群組。 應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。                                                                          |



 

 

 



