---
description: 儲存在 Active Directory 支援管理委派的授權原則存放區。
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: 委派 c + + 中的許可權定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980439"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="e8f5e-103">委派 c + + 中的許可權定義</span><span class="sxs-lookup"><span data-stu-id="e8f5e-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="e8f5e-104">儲存在 Active Directory 支援管理委派的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="e8f5e-105">系統管理可以委派給存放區、應用程式或範圍層級的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="e8f5e-106">每個層級都有一份系統管理員和讀者的清單。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="e8f5e-107">存放區、應用程式或範圍的系統管理員可以讀取和修改委派層級的原則存放區。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="e8f5e-108">讀取器可以讀取委派層級的原則存放區，但無法修改存放區。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="e8f5e-109">屬於系統管理員或應用程式讀取者的使用者或群組，也必須新增為包含該應用程式之原則存放區的委派使用者。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="e8f5e-110">同樣地，必須將屬於系統管理員或範圍讀取者的使用者或群組新增為包含該範圍之應用程式的委派使用者。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="e8f5e-111">例如，若要委派範圍的系統管理，請先呼叫 [**IAzAuthorizationStore：： AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) 方法，將使用者或群組新增至包含此範圍之存放區的委派使用者清單中。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="e8f5e-112">然後藉由呼叫 [**IAzApplication：： AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) 方法，將使用者或群組新增至包含範圍的應用程式的委派使用者清單中。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="e8f5e-113">最後，藉由呼叫 [**IAzScope：： AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) 方法，將使用者或群組新增至範圍的系統管理員清單。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="e8f5e-114">以 XML 為基礎的原則存放區不支援任何層級的委派。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="e8f5e-115">如果範圍包含的工作定義包含授權規則或包含授權規則的角色定義，則無法委派儲存在 Active Directory 的授權存放區內的範圍。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="e8f5e-116">下列範例顯示如何委派應用程式的管理。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="e8f5e-117">此範例假設指定的位置有現有的 Active Directory 授權原則存放區，此原則存放區包含名為 Expense 的應用程式，且此應用程式未包含任何含有商務規則腳本的工作。</span><span class="sxs-lookup"><span data-stu-id="e8f5e-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
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
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
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



 

 



