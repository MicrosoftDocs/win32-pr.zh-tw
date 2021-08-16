---
description: 應用程式群組是一組使用者和使用者群組。 應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。 應用程式群組是由 IAzApplicationGroup 物件表示。
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: 將使用者新增至腳本中的應用程式群組
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18c990e3140dcfc6a4cbc2d57379431075387f43af8fbb0b22f344ffd0b9a30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784930"
---
# <a name="adding-users-to-an-application-group-in-script"></a>將使用者新增至腳本中的應用程式群組

在授權管理員中，應用程式群組是一組使用者和使用者群組。 應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。 應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。

**允許應用程式群組的成員執行一或一組任務**

-   將該應用程式群組指派給包含這些工作的角色。

    角色會以 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件表示。

下列範例示範如何建立應用程式群組、將使用者新增為應用程式群組的成員，以及將應用程式群組指派給現有的角色。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含名為 Expense Administrator 的角色。


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



