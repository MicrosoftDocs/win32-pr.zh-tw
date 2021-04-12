---
description: 若要在 c + + 中建立用戶端內容，應用程式可以使用權杖的控制碼、網域和使用者名稱，或用戶端安全識別碼的字串表示，建立用戶端內容。
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: 使用 c + + 中的授權管理員建立用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79afa31db547b28d129c5b8e90dcf3e4ba1e91c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513585"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a>使用 c + + 中的授權管理員建立用戶端內容

在授權管理員中，應用程式會藉由呼叫 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法（代表用戶端內容），來判斷用戶端是否有權存取作業。

應用程式可以使用權杖的控制碼、網域和使用者名稱，或用戶端的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 的字串表示，來建立用戶端內容。

使用 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication)介面的 [**InitializeClientCoNtextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken)、 [**InitializeClientCoNtextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)和 [**InitializeClientCoNtextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid)方法來建立用戶端內容。

下列範例顯示如何從用戶端權杖建立 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) 物件。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，此存放區包含名為 Expense 的應用程式，而且變數 hToken 包含有效的用戶端權杖。


```C++
#include <windows.h>

void ExpenseCheck(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
 
 //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

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

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
                &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Use the client context as needed.

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
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



 

 
