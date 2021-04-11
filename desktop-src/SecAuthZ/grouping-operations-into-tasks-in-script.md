---
description: 在授權管理員中，工作是應用程式使用者需要完成的高層級動作。
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: 將作業分組到腳本中的工作
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851715"
---
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="f8093-103">將作業分組到腳本中的工作</span><span class="sxs-lookup"><span data-stu-id="f8093-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="f8093-104">在授權管理員中，工作是應用程式使用者需要完成的高層級動作。</span><span class="sxs-lookup"><span data-stu-id="f8093-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="f8093-105">工作是由作業所組成，這是應用程式的低層級函式和方法。</span><span class="sxs-lookup"><span data-stu-id="f8093-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="f8093-106">接著，會將工作指派給必須執行該工作的角色。</span><span class="sxs-lookup"><span data-stu-id="f8093-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="f8093-107">工作是以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="f8093-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="f8093-108">如需作業和工作的詳細資訊，請參閱 [作業和](operations-and-tasks.md)工作。</span><span class="sxs-lookup"><span data-stu-id="f8093-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="f8093-109">下列範例顯示如何將作業分組以建立工作。</span><span class="sxs-lookup"><span data-stu-id="f8093-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="f8093-110">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含在 [腳本中定義作業](defining-operations-in-script.md)的主題中定義的作業。</span><span class="sxs-lookup"><span data-stu-id="f8093-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



