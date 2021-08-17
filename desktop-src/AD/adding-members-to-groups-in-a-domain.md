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
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024755"
---
# <a name="adding-members-to-groups-in-a-domain"></a>將成員新增至網域中的群組

群組可以包含任何數目的使用者、連絡人或其他群組作為成員。 下列清單列出控制群組成員資格的群組物件屬性。



| 屬性                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**成員**](/windows/desktop/ADSchema/a-member)<br/>     | [**Member**](/windows/desktop/ADSchema/a-member)屬性包含屬於群組成員之物件的辨別名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | [**MemberOf**](/windows/desktop/ADSchema/a-memberof)屬性包含群組的辨別名稱，其中包含群組作為直接成員。 **MemberOf** 屬性不包含任何繼承的群組成員資格資料。 例如，如果 GroupA 是 GroupB 的成員，而 GroupB 是 GroupC 的成員，GroupA 的 **memberOf** 屬性將會包含 GroupB，但不包含 GroupC。<br/> Active Directory 伺服器會維護此屬性。 將辨別名稱新增至另一個群組的 [**成員**](/windows/desktop/ADSchema/a-member) 屬性時，該其他群組的辨別名稱就會加入此群組的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性中。<br/> |



 

下列每個方法都可以用來將成員加入至群組。 您可以使用成員的辨別名稱或成員物件的系結，然後將成員物件新增至群組物件，來加入成員。

若要將屬於下層網域的成員新增至上層網域中的群組，請使用 SID 字串的可系結形式作為分辨名稱。 如需詳細資訊和示範如何將 **objectSid** 轉換為可系結字串的程式碼範例，請參閱範例程式碼中的 **GetLDAPSidBindStringFromVariantSID** 範例函式，將 [objectSid 轉換成](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)可系結的字串。

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>使用 IADsGroup 將成員新增至群組
</dt> <dd>

[**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)介面可以用來將成員加入至群組，方法是使用 [**IADsGroup. add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add)方法。 系結至並取得群組物件的 **IADsGroup** 介面。 然後， **IADsGroup** 就可以用來將成員加入至群組。

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>使用 IDirectoryObject 將成員新增至群組
</dt> <dd>

[**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)介面可以用來將成員加入至群組，方法是使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes)方法來修改群組的 [**成員**](/windows/desktop/ADSchema/a-member)屬性。 系結至並取得群組物件的 **IDirectoryObject** 介面。 然後使用 **IDirectoryObject：： SetObjectAttributes** 方法來修改 **成員** 屬性。

> [!Note]  
> 由於 [**成員**](/windows/desktop/ADSchema/a-member) 屬性有多個值，因此請確定您使用 **ADS \_ ATTR \_ 附加** 控制項程式碼，將辨別名稱加入至 **成員** 屬性。 使用 **ADS \_ ATTR \_ UPDATE** control 程式碼將會覆寫現有的 **成員** 值。

 

建立群組時， [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)介面也可以用來將成員加入至群組，方法是在 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)方法的 *pAttributeEntries* 參數中指定成員。

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>使用 System. DirectoryServices 將成員新增至群組
</dt> <dd>

您可以使用 [DirectoryServices](/dotnet/api/system.directoryservices)命名空間，將成員新增至群組，方法是在群組物件的 **成員** 屬性上使用 **PropertyValueCollection. add** 方法。 如需詳細資訊，請參閱 [設定目錄物件的屬性](/previous-versions/ms180860(v=vs.90))。

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>使用 LDAP API 將成員新增至群組
</dt> <dd>

您可以使用 [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)API，將成員新增至群組，方法是使用其中一個 [**ldap \_ 修改 \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s)函式。 如需詳細資訊，請參閱 [修改目錄專案](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)。

</dd> </dl>

 

