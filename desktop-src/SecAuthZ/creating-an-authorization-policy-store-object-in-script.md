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
# <a name="creating-an-authorization-policy-store-object-in-script"></a>在腳本中建立授權原則存放區物件

授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。 這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。 當使用授權管理員的應用程式初始化時，它會從存放區載入此資訊。 授權原則存放區必須位於信任的系統上，因為該系統上的系統管理員具有存放區的高存取權。

授權管理員支援將授權原則儲存在 Active Directory Directory 服務或 XML 檔案中，如下列範例所示。 在授權管理員 API 中，授權原則存放區會以 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件表示。 這些範例會示範如何建立 Active Directory 存放區和 XML 存放區的 **AzAuthorizationStore** 物件。

-   [建立 Active Directory 存放區](#creating-an-active-directory-store)
-   [建立 SQL Server 存放區](#creating-a-sql-server-store)
-   [建立 XML 存放區](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>建立 Active Directory 存放區

若要使用 Active Directory 來儲存授權原則，網域必須處於 **Windows Server 2003** 網域功能等級。 在 **非網域命名內容** 中找不到授權原則存放區 (也稱為應用程式磁碟分割) 。 建議您將存放區放在 **程式資料** 容器中，該容器是專門為授權原則存放區建立的新組織單位。 此外，也建議將存放區放在與執行使用存放區之應用程式的應用程式伺服器相同的區域網路內。

下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 Active Directory 中的授權原則存放區。 此範例假設名為 authmanager.com 的網域中有一個名為 Program Data 的現有 Active Directory 組織單位。


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



## <a name="creating-a-sql-server-store"></a>建立 SQL Server 存放區

授權管理員支援建立以 Microsoft SQL Server 為基礎的授權原則存放區。 若要建立以 SQL Server 為基礎的授權存放，請使用開頭為首碼 **MSSQL://** 的 URL。 URL 必須包含有效的 SQL 連接字串、資料庫名稱，以及授權原則存放區的名稱： **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_。

如果 SQL Server 實例不包含指定的授權管理員資料庫，授權管理員會以該名稱建立新的資料庫。

> [!Note]  
> 除非您明確設定連接的 SQL 加密，或設定使用網際網路通訊協定安全性 (IPsec) 之網路流量的加密，否則不會加密與 SQL Server 存放區的連接。

 

下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 SQL Server 資料庫中的授權原則存放區。


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



## <a name="creating-an-xml-store"></a>建立 XML 存放區

授權管理員支援以 XML 格式建立授權原則存放區。 XML 存放區可以位於執行應用程式的同一部電腦上，也可以從遠端儲存。 不支援直接編輯 XML 檔案。 使用授權管理員 MMC 嵌入式管理單元或授權管理員 API 來編輯原則存放區。

授權管理員不支援委派 XML 原則存放區的管理。 如需委派的詳細資訊，請參閱 [委派腳本中的許可權定義](delegating-the-defining-of-permissions-in-script.md)。

下列範例示範如何建立 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件，該物件代表 XML 檔案中的授權原則存放區。


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



