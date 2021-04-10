---
description: 授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。 這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: 在 c + + 中建立授權原則存放區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943711"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="eba01-104">在 c + + 中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="eba01-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="eba01-105">授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eba01-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="eba01-106">這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="eba01-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="eba01-107">當使用授權管理員的應用程式初始化時，它會從存放區載入此資訊。</span><span class="sxs-lookup"><span data-stu-id="eba01-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="eba01-108">授權原則存放區必須位於信任的系統上，因為該系統上的系統管理員具有存放區的高存取權。</span><span class="sxs-lookup"><span data-stu-id="eba01-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="eba01-109">授權管理員支援將授權原則儲存在 Active Directory Directory 服務或 XML 檔案中，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="eba01-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="eba01-110">在授權管理員 API 中，授權原則存放區會以 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="eba01-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="eba01-111">這些範例會示範如何建立 Active Directory 存放區和 XML 存放區的 **AzAuthorizationStore** 物件。</span><span class="sxs-lookup"><span data-stu-id="eba01-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="eba01-112">建立 Active Directory 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="eba01-113">建立 SQL Server 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="eba01-114">建立 XML 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="eba01-115">建立 Active Directory 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="eba01-116">若要使用 Active Directory 來儲存授權原則，網域必須處於 **Windows Server 2003** 網域功能等級。</span><span class="sxs-lookup"><span data-stu-id="eba01-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="eba01-117">在 **非網域命名內容** 中找不到授權原則存放區 (也稱為應用程式磁碟分割) 。</span><span class="sxs-lookup"><span data-stu-id="eba01-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="eba01-118">建議您將存放區放在 **程式資料** 容器中，該容器是專門為授權原則存放區建立的新組織單位。</span><span class="sxs-lookup"><span data-stu-id="eba01-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="eba01-119">此外，也建議將存放區放在與執行使用存放區之應用程式的應用程式伺服器相同的區域網路內。</span><span class="sxs-lookup"><span data-stu-id="eba01-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="eba01-120">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 Active Directory 中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="eba01-121">此範例假設名為 authmanager.com 的網域中有一個名為 Program Data 的現有 Active Directory 組織單位。</span><span class="sxs-lookup"><span data-stu-id="eba01-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="eba01-122">建立 SQL Server 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="eba01-123">授權管理員支援建立以 Microsoft SQL Server 為基礎的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="eba01-124">若要建立以 SQL Server 為基礎的授權存放，請使用開頭為首碼 **MSSQL://** 的 URL。</span><span class="sxs-lookup"><span data-stu-id="eba01-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="eba01-125">URL 必須包含有效的 SQL 連接字串、資料庫名稱，以及授權原則存放區的名稱： **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_。</span><span class="sxs-lookup"><span data-stu-id="eba01-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="eba01-126">如果 SQL Server 實例不包含指定的授權管理員資料庫，授權管理員會以該名稱建立新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="eba01-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="eba01-127">除非您明確設定連接的 SQL 加密，或設定使用網際網路通訊協定安全性 (IPsec) 之網路流量的加密，否則不會加密與 SQL Server 存放區的連接。</span><span class="sxs-lookup"><span data-stu-id="eba01-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="eba01-128">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 SQL Server 資料庫中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a><span data-ttu-id="eba01-129">建立 XML 存放區</span><span class="sxs-lookup"><span data-stu-id="eba01-129">Creating an XML Store</span></span>

<span data-ttu-id="eba01-130">授權管理員支援以 XML 格式建立授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="eba01-131">XML 存放區可以位於執行應用程式的同一部電腦上，也可以從遠端儲存。</span><span class="sxs-lookup"><span data-stu-id="eba01-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="eba01-132">不支援直接編輯 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="eba01-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="eba01-133">使用授權管理員 MMC 嵌入式管理單元或授權管理員 API 來編輯原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="eba01-134">授權管理員不支援委派 XML 原則存放區的管理。</span><span class="sxs-lookup"><span data-stu-id="eba01-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="eba01-135">如需委派的詳細資訊，請參閱 [委派 c + + 中的許可權定義](delegating-the-defining-of-permissions-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="eba01-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="eba01-136">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 XML 檔案中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="eba01-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



