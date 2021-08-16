---
description: 儲存在 Active Directory 支援管理委派的授權原則存放區。
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: 委派 c + + 中的許可權定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f79202a3f8ee21934f890d3c5a66a19be4466fa2b1ecdfe31672a4edfc2319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782052"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>委派 c + + 中的許可權定義

儲存在 Active Directory 支援管理委派的授權原則存放區。 系統管理可以委派給存放區、應用程式或範圍層級的使用者和群組。

每個層級都有一份系統管理員和讀者的清單。 存放區、應用程式或範圍的系統管理員可以讀取和修改委派層級的原則存放區。 讀取器可以讀取委派層級的原則存放區，但無法修改存放區。

屬於系統管理員或應用程式讀取者的使用者或群組，也必須新增為包含該應用程式之原則存放區的委派使用者。 同樣地，必須將屬於系統管理員或範圍讀取者的使用者或群組新增為包含該範圍之應用程式的委派使用者。

例如，若要委派範圍的系統管理，請先呼叫 [**IAzAuthorizationStore：： AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) 方法，將使用者或群組新增至包含此範圍之存放區的委派使用者清單中。 然後藉由呼叫 [**IAzApplication：： AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) 方法，將使用者或群組新增至包含範圍的應用程式的委派使用者清單中。 最後，藉由呼叫 [**IAzScope：： AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) 方法，將使用者或群組新增至範圍的系統管理員清單。

以 XML 為基礎的原則存放區不支援任何層級的委派。

如果範圍包含的工作定義包含授權規則或包含授權規則的角色定義，則無法委派儲存在 Active Directory 的授權存放區內的範圍。

下列範例顯示如何委派應用程式的管理。 此範例假設指定的位置有現有的 Active Directory 授權原則存放區，此原則存放區包含名為 Expense 的應用程式，且此應用程式未包含任何含有商務規則腳本的工作。


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



 

 



