---
description: 在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: 將工作分組到腳本中的角色
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db0314ad953eecb94f10c995dea28e1dc3d69b586c386a94ae4f1ed45037fdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913582"
---
# <a name="grouping-tasks-into-roles-in-script"></a>將工作分組到腳本中的角色

在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。 工作會群組在一起，並指派給角色定義，而角色定義會以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件表示，並將其 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) 屬性設定為 **True**。 然後可以將角色定義指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件，然後將使用者或使用者群組指派給該物件。 如需工作和角色的詳細資訊，請參閱 [角色](roles.md)。

下列範例顯示如何將工作指派給角色定義、建立角色物件，以及將角色定義指派給 role 物件。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含名為 Submit Expense 和核准 Expense 的工作。


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



