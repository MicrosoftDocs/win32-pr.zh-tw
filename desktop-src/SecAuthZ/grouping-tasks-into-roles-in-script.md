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
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945034"
---
# <a name="grouping-tasks-into-roles-in-script"></a><span data-ttu-id="7ee8a-103">將工作分組到腳本中的角色</span><span class="sxs-lookup"><span data-stu-id="7ee8a-103">Grouping Tasks into Roles in Script</span></span>

<span data-ttu-id="7ee8a-104">在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="7ee8a-105">工作會群組在一起，並指派給角色定義，而角色定義會以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件表示，並將其 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) 屬性設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **True**.</span></span> <span data-ttu-id="7ee8a-106">然後可以將角色定義指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件，然後將使用者或使用者群組指派給該物件。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="7ee8a-107">如需工作和角色的詳細資訊，請參閱 [角色](roles.md)。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="7ee8a-108">下列範例顯示如何將工作指派給角色定義、建立角色物件，以及將角色定義指派給 role 物件。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="7ee8a-109">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含名為 Submit Expense 和核准 Expense 的工作。</span><span class="sxs-lookup"><span data-stu-id="7ee8a-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


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



 

 



