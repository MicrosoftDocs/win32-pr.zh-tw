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
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980442"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="94e73-105">將使用者新增至腳本中的應用程式群組</span><span class="sxs-lookup"><span data-stu-id="94e73-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="94e73-106">在授權管理員中，應用程式群組是一組使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="94e73-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="94e73-107">應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="94e73-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="94e73-108">應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="94e73-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="94e73-109">**允許應用程式群組的成員執行一或一組任務**</span><span class="sxs-lookup"><span data-stu-id="94e73-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="94e73-110">將該應用程式群組指派給包含這些工作的角色。</span><span class="sxs-lookup"><span data-stu-id="94e73-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="94e73-111">角色會以 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="94e73-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="94e73-112">下列範例示範如何建立應用程式群組、將使用者新增為應用程式群組的成員，以及將應用程式群組指派給現有的角色。</span><span class="sxs-lookup"><span data-stu-id="94e73-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="94e73-113">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含名為 Expense Administrator 的角色。</span><span class="sxs-lookup"><span data-stu-id="94e73-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


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



 

 



