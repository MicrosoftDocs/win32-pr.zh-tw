---
description: 授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: 在腳本中建立授權原則存放區物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848356"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a><span data-ttu-id="9b850-103">在腳本中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="9b850-103">Creating an Authorization Policy Store Object in Script</span></span>

<span data-ttu-id="9b850-104">授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b850-104">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="9b850-105">這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="9b850-105">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="9b850-106">當使用授權管理員的應用程式初始化時，它會從存放區載入此資訊。</span><span class="sxs-lookup"><span data-stu-id="9b850-106">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="9b850-107">授權原則存放區必須位於信任的系統上，因為該系統上的系統管理員具有存放區的高存取權。</span><span class="sxs-lookup"><span data-stu-id="9b850-107">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="9b850-108">授權管理員支援將授權原則儲存在 Active Directory Directory 服務或 XML 檔案中，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9b850-108">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="9b850-109">在授權管理員 API 中，授權原則存放區會以 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="9b850-109">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="9b850-110">這些範例會示範如何建立 Active Directory 存放區和 XML 存放區的 **AzAuthorizationStore** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b850-110">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="9b850-111">建立 Active Directory 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-111">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="9b850-112">建立 SQL Server 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-112">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="9b850-113">建立 XML 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-113">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="9b850-114">建立 Active Directory 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-114">Creating an Active Directory Store</span></span>

<span data-ttu-id="9b850-115">若要使用 Active Directory 來儲存授權原則，網域必須處於 **Windows Server 2003** 網域功能等級。</span><span class="sxs-lookup"><span data-stu-id="9b850-115">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="9b850-116">在 **非網域命名內容** 中找不到授權原則存放區 (也稱為應用程式磁碟分割) 。</span><span class="sxs-lookup"><span data-stu-id="9b850-116">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="9b850-117">建議您將存放區放在 **程式資料** 容器中，該容器是專門為授權原則存放區建立的新組織單位。</span><span class="sxs-lookup"><span data-stu-id="9b850-117">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="9b850-118">此外，也建議將存放區放在與執行使用存放區之應用程式的應用程式伺服器相同的區域網路內。</span><span class="sxs-lookup"><span data-stu-id="9b850-118">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="9b850-119">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 Active Directory 中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-119">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="9b850-120">此範例假設名為 authmanager.com 的網域中有一個名為 Program Data 的現有 Active Directory 組織單位。</span><span class="sxs-lookup"><span data-stu-id="9b850-120">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="9b850-121">建立 SQL Server 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-121">Creating a SQL Server Store</span></span>

<span data-ttu-id="9b850-122">授權管理員支援建立以 Microsoft SQL Server 為基礎的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-122">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="9b850-123">若要建立以 SQL Server 為基礎的授權存放，請使用開頭為首碼 **MSSQL://** 的 URL。</span><span class="sxs-lookup"><span data-stu-id="9b850-123">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="9b850-124">URL 必須包含有效的 SQL 連接字串、資料庫名稱，以及授權原則存放區的名稱： **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_。</span><span class="sxs-lookup"><span data-stu-id="9b850-124">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="9b850-125">如果 SQL Server 實例不包含指定的授權管理員資料庫，授權管理員會以該名稱建立新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="9b850-125">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="9b850-126">除非您明確設定連接的 SQL 加密，或設定使用網際網路通訊協定安全性 (IPsec) 之網路流量的加密，否則不會加密與 SQL Server 存放區的連接。</span><span class="sxs-lookup"><span data-stu-id="9b850-126">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="9b850-127">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 SQL Server 資料庫中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-127">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a><span data-ttu-id="9b850-128">建立 XML 存放區</span><span class="sxs-lookup"><span data-stu-id="9b850-128">Creating an XML Store</span></span>

<span data-ttu-id="9b850-129">授權管理員支援以 XML 格式建立授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-129">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="9b850-130">XML 存放區可以位於執行應用程式的同一部電腦上，也可以從遠端儲存。</span><span class="sxs-lookup"><span data-stu-id="9b850-130">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="9b850-131">不支援直接編輯 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="9b850-131">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="9b850-132">使用授權管理員 MMC 嵌入式管理單元或授權管理員 API 來編輯原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-132">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="9b850-133">授權管理員不支援委派 XML 原則存放區的管理。</span><span class="sxs-lookup"><span data-stu-id="9b850-133">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="9b850-134">如需委派的詳細資訊，請參閱 [委派腳本中的許可權定義](delegating-the-defining-of-permissions-in-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9b850-134">For information about delegation, see [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).</span></span>

<span data-ttu-id="9b850-135">下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 XML 檔案中的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="9b850-135">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



