---
description: IAzApplicationGroup 物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。 IAzApplicationGroup 物件也可以包含其他 IAzApplicationGroup 物件做為成員。
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: 在腳本中定義使用者群組
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6198d31a53dbd7d30100a8df56536cf0336c9c1e7ca5b78ad4e9e73e40da13cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913984"
---
# <a name="defining-groups-of-users-in-script"></a>在腳本中定義使用者群組

在授權管理員中， [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件代表一組使用者。 然後，您可以將角色共同指派給這個使用者群組。 **IAzApplicationGroup** 物件也可以包含其他 **IAzApplicationGroup** 物件做為成員。 如需應用程式群組的詳細資訊，請參閱 [使用者和群組](users-and-groups.md)。

群組可以由成員和非成員的明確清單定義，或透過 [*輕量型目錄存取協定*](/windows/desktop/SecGloss/l-gly) (LDAP) 查詢來定義。 下列範例示範如何建立每種類型的應用程式群組：

-   [建立基本群組](#creating-a-basic-group)
-   [建立 LDAP 查詢群組](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>建立基本群組

基本應用程式群組是由代表該群組之 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件 [](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members)的成員 [**和非成員屬性**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers)所定義。 [ **成員** ] 屬性中所列的使用者和群組會包含在應用程式群組中，而 [非 **成員** ] 屬性中所列的使用者和群組則會從應用程式群組中排除。 在非成員屬性中 **列出的取代** 會列在 [ **成員** ] 屬性中。

下列範例示範如何建立基本的應用程式群組，並將所有本機使用者新增為該群組的成員。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。


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
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>建立 LDAP 查詢群組

LDAP 查詢群組具有其 [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) 屬性值中包含的查詢所定義的成員資格。

下列範例顯示如何建立 LDAP 查詢應用程式群組，並將所有使用者新增為該群組的成員。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。


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
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
