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
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320551"
---
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="6d1ba-105">在腳本中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="6d1ba-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="6d1ba-106">在授權管理員中， [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件代表一組使用者。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="6d1ba-107">然後，您可以將角色共同指派給這個使用者群組。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="6d1ba-108">**IAzApplicationGroup** 物件也可以包含其他 **IAzApplicationGroup** 物件做為成員。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="6d1ba-109">如需應用程式群組的詳細資訊，請參閱 [使用者和群組](users-and-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="6d1ba-110">群組可以由成員和非成員的明確清單定義，或透過 [*輕量型目錄存取協定*](/windows/desktop/SecGloss/l-gly) (LDAP) 查詢來定義。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="6d1ba-111">下列範例示範如何建立每種類型的應用程式群組：</span><span class="sxs-lookup"><span data-stu-id="6d1ba-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="6d1ba-112">建立基本群組</span><span class="sxs-lookup"><span data-stu-id="6d1ba-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="6d1ba-113">建立 LDAP 查詢群組</span><span class="sxs-lookup"><span data-stu-id="6d1ba-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="6d1ba-114">建立基本群組</span><span class="sxs-lookup"><span data-stu-id="6d1ba-114">Creating a Basic Group</span></span>

<span data-ttu-id="6d1ba-115">基本應用程式群組是由代表該群組之 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件 [](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members)的成員 [**和非成員屬性**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers)所定義。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="6d1ba-116">[ **成員** ] 屬性中所列的使用者和群組會包含在應用程式群組中，而 [非 **成員** ] 屬性中所列的使用者和群組則會從應用程式群組中排除。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="6d1ba-117">在非成員屬性中 **列出的取代** 會列在 [ **成員** ] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="6d1ba-118">下列範例示範如何建立基本的應用程式群組，並將所有本機使用者新增為該群組的成員。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="6d1ba-119">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="6d1ba-120">建立 LDAP 查詢群組</span><span class="sxs-lookup"><span data-stu-id="6d1ba-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="6d1ba-121">LDAP 查詢群組具有其 [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) 屬性值中包含的查詢所定義的成員資格。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="6d1ba-122">下列範例顯示如何建立 LDAP 查詢應用程式群組，並將所有使用者新增為該群組的成員。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="6d1ba-123">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。</span><span class="sxs-lookup"><span data-stu-id="6d1ba-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



 

 
