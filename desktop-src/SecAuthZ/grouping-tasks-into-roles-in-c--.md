---
description: 在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。
ms.assetid: d2671c52-8d34-45e2-9c49-4ed399f3c220
title: 在 c + + 中將工作分組為角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb4952d9ece250ddfacc53d955bce3a107281a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978109"
---
# <a name="grouping-tasks-into-roles-in-c"></a><span data-ttu-id="8ea16-103">在 c + + 中將工作分組為角色</span><span class="sxs-lookup"><span data-stu-id="8ea16-103">Grouping Tasks into Roles in C++</span></span>

<span data-ttu-id="8ea16-104">在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。</span><span class="sxs-lookup"><span data-stu-id="8ea16-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="8ea16-105">工作會群組在一起，並指派給角色定義，而角色定義會以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件表示，並將其 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8ea16-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **TRUE**.</span></span> <span data-ttu-id="8ea16-106">然後可以將角色定義指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件，然後將使用者或使用者群組指派給該物件。</span><span class="sxs-lookup"><span data-stu-id="8ea16-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="8ea16-107">如需工作和角色的詳細資訊，請參閱 [角色](roles.md)。</span><span class="sxs-lookup"><span data-stu-id="8ea16-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="8ea16-108">下列範例顯示如何將工作指派給角色定義、建立角色物件，以及將角色定義指派給 role 物件。</span><span class="sxs-lookup"><span data-stu-id="8ea16-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="8ea16-109">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，且此應用程式包含名為 Submit Expense 和核准 Expense 的工作。</span><span class="sxs-lookup"><span data-stu-id="8ea16-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


```C++
#ifndef _WIN32_WINNT
 #define _WIN32_WINNT 0x0502
#endif 
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzTask* pTaskRoleDef = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR taskNameSubmit = NULL;
    BSTR taskNameApprove = NULL;
    BSTR roleDefName = NULL;
    BSTR roleName = NULL;
    
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the policy store.
    storeName = SysAllocString(L"msxml://c:\\myStore.xml");
    if (!storeName)
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    appName = SysAllocString(L"Expense");
    if (!appName)
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Allocate strings for the task names.
    taskNameSubmit = SysAllocString(L"Submit Expense");
    if (!taskNameSubmit)
        MyHandleError("Could not allocate first task name string.");
    
    taskNameApprove = SysAllocString(L"Approve Expense");
    if (!taskNameApprove)
        MyHandleError("Could not allocate second task name string.");

    //  Create a third task object to act as a role definition.
    roleDefName = SysAllocString(L"Expense Admin");
    if (!roleDefName)
        MyHandleError("Could not allocate role definition name.");
    hr = pApp->CreateTask(roleDefName, myVar, &pTaskRoleDef);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create role definition.");

    //  Set the IsRoleDefinition property of pTaskRoleDef to TRUE.
    hr = pTaskRoleDef->put_IsRoleDefinition(true);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set role definition property.");

    //  Add two tasks to the role definition.
    hr = pTaskRoleDef->AddTask(taskNameSubmit, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add submit task.");
    hr = pTaskRoleDef->AddTask(taskNameApprove, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add approve task.");

    //  Save information to the store.
    hr = pTaskRoleDef->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data to the store.");

    //  Create an IAzRole object.
    roleName = SysAllocString(L"Expense Administrator");
    if (!roleName)
        MyHandleError("Could not allocate role name.");
    hr = pApp->CreateRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create a role object.");

    //  Add the role definition to the role object.
    hr = pRole->AddTask(roleDefName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could add role definition to the role.");

    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pTaskRoleDef->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(taskNameSubmit);
    SysFreeString(taskNameApprove);
    SysFreeString(roleDefName);
    SysFreeString(roleName);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



