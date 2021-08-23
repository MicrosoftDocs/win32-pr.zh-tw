---
description: 在授權管理員中，IAzApplicationGroup 物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: 在 c + + 中定義使用者群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde349dcf5a877490d85917247cf7fba3480143d87d92afb1b8eb2017030e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914034"
---
# <a name="defining-groups-of-users-in-c"></a>在 c + + 中定義使用者群組

在授權管理員中， [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件也可以包含其他 **IAzApplicationGroup** 物件做為成員。 如需應用程式群組的詳細資訊，請參閱 [使用者和群組](users-and-groups.md)。

您可以透過明確的成員和非成員清單來定義群組，也可以透過 [*輕量型目錄存取協定*](/windows/desktop/SecGloss/l-gly) (LDAP) 查詢來定義群組。 下列範例示範如何建立每種類型的應用程式群組：

-   [建立基本群組](#creating-a-basic-group)
-   [建立 LDAP 查詢群組](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>建立基本群組

基本應用程式群組是由代表該群組之 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件 [](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members)的成員 [**和非成員屬性**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers)所定義。 [ **成員** ] 屬性中所列的使用者和群組會包含在應用程式群組中，而 [非 **成員** ] 屬性中所列的使用者和群組則會從應用程式群組中排除。 在非成員屬性中 **列出的取代** 會列在 [ **成員** ] 屬性中。

下列範例示範如何建立基本的應用程式群組，並將所有本機使用者新增為該群組的成員。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

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

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
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



## <a name="creating-an-ldap-query-group"></a>建立 LDAP 查詢群組

LDAP 查詢群組具有其 [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) 屬性值中包含的查詢所定義的成員資格。

下列範例顯示如何建立 LDAP 查詢應用程式群組，並將所有使用者新增為該群組的成員。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
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



 

 
