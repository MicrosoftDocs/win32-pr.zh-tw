---
title: 將成員新增至網域中的群組
description: 本主題說明如何將成員新增至網域中的群組。
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- 將成員新增至網域 AD 中的群組
- 群組 AD，將成員新增至網域中的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462941"
---
# <a name="adding-members-to-groups-in-a-domain"></a><span data-ttu-id="f5577-105">將成員新增至網域中的群組</span><span class="sxs-lookup"><span data-stu-id="f5577-105">Adding Members to Groups in a Domain</span></span>

<span data-ttu-id="f5577-106">群組可以包含任何數目的使用者、連絡人或其他群組作為成員。</span><span class="sxs-lookup"><span data-stu-id="f5577-106">A group can contain any number of users, contacts, or other groups as members.</span></span> <span data-ttu-id="f5577-107">下列清單列出控制群組成員資格的群組物件屬性。</span><span class="sxs-lookup"><span data-stu-id="f5577-107">The following list lists the attributes of the group object that control group membership.</span></span>



| <span data-ttu-id="f5577-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f5577-108">Attribute</span></span>                                      | <span data-ttu-id="f5577-109">描述</span><span class="sxs-lookup"><span data-stu-id="f5577-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5577-110">**成員**</span><span class="sxs-lookup"><span data-stu-id="f5577-110">**member**</span></span>](/windows/desktop/ADSchema/a-member)<br/>     | <span data-ttu-id="f5577-111">[**Member**](/windows/desktop/ADSchema/a-member)屬性包含屬於群組成員之物件的辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="f5577-111">The [**member**](/windows/desktop/ADSchema/a-member) attribute contains the distinguished names for the objects that are members of the group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="f5577-112">**memberOf**</span><span class="sxs-lookup"><span data-stu-id="f5577-112">**memberOf**</span></span>](/windows/desktop/ADSchema/a-memberof)<br/> | <span data-ttu-id="f5577-113">[**MemberOf**](/windows/desktop/ADSchema/a-memberof)屬性包含群組的辨別名稱，其中包含群組作為直接成員。</span><span class="sxs-lookup"><span data-stu-id="f5577-113">The [**memberOf**](/windows/desktop/ADSchema/a-memberof) attribute contains the distinguished names of groups that contain the group as a direct member.</span></span> <span data-ttu-id="f5577-114">**MemberOf** 屬性不包含任何繼承的群組成員資格資料。</span><span class="sxs-lookup"><span data-stu-id="f5577-114">The **memberOf** attribute does not contain any inherited group membership data.</span></span> <span data-ttu-id="f5577-115">例如，如果 GroupA 是 GroupB 的成員，而 GroupB 是 GroupC 的成員，GroupA 的 **memberOf** 屬性將會包含 GroupB，但不包含 GroupC。</span><span class="sxs-lookup"><span data-stu-id="f5577-115">For example, if GroupA is a member of GroupB and GroupB is a member of GroupC, the **memberOf** attribute for GroupA will contain GroupB, but not GroupC.</span></span><br/> <span data-ttu-id="f5577-116">Active Directory 伺服器會維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="f5577-116">The Active Directory server maintains this property.</span></span> <span data-ttu-id="f5577-117">將辨別名稱新增至另一個群組的 [**成員**](/windows/desktop/ADSchema/a-member) 屬性時，該其他群組的辨別名稱就會加入此群組的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="f5577-117">When a distinguished name is added to the [**member**](/windows/desktop/ADSchema/a-member) property of another group, that other group's distinguished name is added to this group's [**memberOf**](/windows/desktop/ADSchema/a-memberof) property.</span></span><br/> |



 

<span data-ttu-id="f5577-118">下列每個方法都可以用來將成員加入至群組。</span><span class="sxs-lookup"><span data-stu-id="f5577-118">Each of the following methods can be used to add a member to a group.</span></span> <span data-ttu-id="f5577-119">您可以使用成員的辨別名稱或成員物件的系結，然後將成員物件新增至群組物件，來加入成員。</span><span class="sxs-lookup"><span data-stu-id="f5577-119">You can add a member by using the distinguished name of the member or binding to the member object and then adding the member object to the group object.</span></span>

<span data-ttu-id="f5577-120">若要將屬於下層網域的成員新增至上層網域中的群組，請使用 SID 字串的可系結形式作為分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f5577-120">To add a member that belongs to a downlevel domain to a group in an uplevel domain, use the bindable form of the SID string for the distinguished name.</span></span> <span data-ttu-id="f5577-121">如需詳細資訊和示範如何將 **objectSid** 轉換為可系結字串的程式碼範例，請參閱範例程式碼中的 **GetLDAPSidBindStringFromVariantSID** 範例函式，將 [objectSid 轉換成](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)可系結的字串。</span><span class="sxs-lookup"><span data-stu-id="f5577-121">For more information and a code example that shows how to convert an **objectSid** into a bindable string, see the **GetLDAPSidBindStringFromVariantSID** example function in [Example Code for Converting an objectSid into a Bindable String](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).</span></span>

<dl> <dt>

<span data-ttu-id="f5577-122"><span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>使用 IADsGroup 將成員新增至群組</span><span class="sxs-lookup"><span data-stu-id="f5577-122"><span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Adding Members to a Group by Using IADsGroup</span></span>
</dt> <dd>

<span data-ttu-id="f5577-123">[**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)介面可以用來將成員加入至群組，方法是使用 [**IADsGroup. add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add)方法。</span><span class="sxs-lookup"><span data-stu-id="f5577-123">The [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface can be used to add members to a group by using the [**IADsGroup.Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="f5577-124">系結至並取得群組物件的 **IADsGroup** 介面。</span><span class="sxs-lookup"><span data-stu-id="f5577-124">Bind to and obtain the **IADsGroup** interface for the group object.</span></span> <span data-ttu-id="f5577-125">然後， **IADsGroup** 就可以用來將成員加入至群組。</span><span class="sxs-lookup"><span data-stu-id="f5577-125">Then the **IADsGroup.Add** method can be used to add members to the group.</span></span>

</dd> <dt>

<span data-ttu-id="f5577-126"><span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>使用 IDirectoryObject 將成員新增至群組</span><span class="sxs-lookup"><span data-stu-id="f5577-126"><span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Adding Members to a Group by Using IDirectoryObject</span></span>
</dt> <dd>

<span data-ttu-id="f5577-127">[**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)介面可以用來將成員加入至群組，方法是使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes)方法來修改群組的 [**成員**](/windows/desktop/ADSchema/a-member)屬性。</span><span class="sxs-lookup"><span data-stu-id="f5577-127">The [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface can be used to add members to a group by using the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method to modify the [**member**](/windows/desktop/ADSchema/a-member) attribute for the group.</span></span> <span data-ttu-id="f5577-128">系結至並取得群組物件的 **IDirectoryObject** 介面。</span><span class="sxs-lookup"><span data-stu-id="f5577-128">Bind to and obtain the **IDirectoryObject** interface for the group object.</span></span> <span data-ttu-id="f5577-129">然後使用 **IDirectoryObject：： SetObjectAttributes** 方法來修改 **成員** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5577-129">Then use the **IDirectoryObject::SetObjectAttributes** method to modify the **member** attribute.</span></span>

> [!Note]  
> <span data-ttu-id="f5577-130">由於 [**成員**](/windows/desktop/ADSchema/a-member) 屬性有多個值，因此請確定您使用 **ADS \_ ATTR \_ 附加** 控制項程式碼，將辨別名稱加入至 **成員** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5577-130">Because the [**member**](/windows/desktop/ADSchema/a-member) attribute has multiple values, ensure that you use the **ADS\_ATTR\_APPEND** control code to add a distinguished name to the **member** attribute.</span></span> <span data-ttu-id="f5577-131">使用 **ADS \_ ATTR \_ UPDATE** control 程式碼將會覆寫現有的 **成員** 值。</span><span class="sxs-lookup"><span data-stu-id="f5577-131">Using the **ADS\_ATTR\_UPDATE** control code will cause the existing **member** values to be overwritten.</span></span>

 

<span data-ttu-id="f5577-132">建立群組時， [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)介面也可以用來將成員加入至群組，方法是在 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)方法的 *pAttributeEntries* 參數中指定成員。</span><span class="sxs-lookup"><span data-stu-id="f5577-132">The [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface can also be used to add members to a group when the group is created by specifying the members in the *pAttributeEntries* parameter of the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

</dd> <dt>

<span data-ttu-id="f5577-133"><span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>使用 System. DirectoryServices 將成員新增至群組</span><span class="sxs-lookup"><span data-stu-id="f5577-133"><span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Adding Members to a Group by Using System.DirectoryServices</span></span>
</dt> <dd>

<span data-ttu-id="f5577-134">您可以使用 [DirectoryServices](/dotnet/api/system.directoryservices)命名空間，將成員新增至群組，方法是在群組物件的 **成員** 屬性上使用 **PropertyValueCollection. add** 方法。</span><span class="sxs-lookup"><span data-stu-id="f5577-134">You can use the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace to add members to a group by using the **PropertyValueCollection.Add** method on the **member** property of the group object.</span></span> <span data-ttu-id="f5577-135">如需詳細資訊，請參閱 [設定目錄物件的屬性](/previous-versions/ms180860(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="f5577-135">For more information, see [Setting Properties on Directory Objects](/previous-versions/ms180860(v=vs.90)).</span></span>

</dd> <dt>

<span data-ttu-id="f5577-136"><span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>使用 LDAP API 將成員新增至群組</span><span class="sxs-lookup"><span data-stu-id="f5577-136"><span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Adding Members to a Group by Using the LDAP API</span></span>
</dt> <dd>

<span data-ttu-id="f5577-137">您可以使用 [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)API，將成員新增至群組，方法是使用其中一個 [**ldap \_ 修改 \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s)函式。</span><span class="sxs-lookup"><span data-stu-id="f5577-137">You can use the [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API to add members to a group by using one of the [**ldap\_modify\***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) functions.</span></span> <span data-ttu-id="f5577-138">如需詳細資訊，請參閱 [修改目錄專案](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)。</span><span class="sxs-lookup"><span data-stu-id="f5577-138">For more information, see [Modifying a Directory Entry](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).</span></span>

</dd> </dl>

 

