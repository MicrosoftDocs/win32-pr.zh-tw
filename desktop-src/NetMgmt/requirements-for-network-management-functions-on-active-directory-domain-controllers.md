---
title: Active Directory 網網域控制站上網路管理功能的需求
description: 如果您在執行 Active Directory 的網域控制站上，呼叫本主題所列的其中一個網路管理功能，則會根據物件的存取控制清單 (ACL) 來允許或拒絕存取安全物件。
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842407"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Active Directory 網網域控制站上網路管理功能的需求

如果您在執行 Active Directory 的網域控制站上，呼叫本主題所列的其中一個網路管理功能，則會根據物件的[存取控制清單](/windows/desktop/SecAuthZ/access-control-lists) (ACL) 來允許或拒絕存取[安全物件](/windows/desktop/SecAuthZ/securable-objects)。  (Acl 是在目錄中指定。 ) 

不同的存取需求適用于資訊查詢和資訊更新。

## <a name="queries"></a>查詢

針對查詢，預設 ACL 允許所有已驗證的使用者和「[Windows 2000 相容存取權](/windows/desktop/SecAuthZ/allowing-anonymous-access)」群組的成員，來讀取和列舉資訊。 以下列出的函式會受到影響：

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)、 [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)、 [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)、 [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)、 [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (層級1和2僅) 
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (層級2和502僅) 
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)、 [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)、 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)、 [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)、 [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)、 [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

匿名存取群組資訊需要將匿名的使用者明確新增至「Windows 2000 相容存取」群組。 這是因為匿名權杖不包含 Everyone 群組 SID。

**Windows 2000：** 依預設，「Windows 2000 相容存取」群組會將每個人都包含為成員。 如此一來，如果系統允許匿名存取，就可以匿名存取 (匿名登入) 資訊。 系統管理員隨時都可以從「Windows 2000 相容存取權」群組移除所有人。 將群組中的每個人從群組中移除，會限制只有驗證的使用者才能存取訊號。 如需匿名存取的詳細資訊，請參閱 [安全性識別](/windows/desktop/SecAuthZ/security-identifiers) 元和 [已知的 sid](/windows/desktop/SecAuthZ/well-known-sids)。

您可以藉由將登錄中的下列機碼設定為值1，來覆寫系統預設值：

**HKEY \_LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa** \\ **EveryoneIncludesAnonymous** = 1

如需在呼叫這兩個函式時，匿名存取群組資訊的詳細資訊，請參閱 [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) 和 [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) 。

## <a name="updates"></a>更新

針對更新，預設 ACL 只允許網域系統管理員和帳戶操作員寫入資訊。 其中一個例外狀況是使用者可以變更自己的密碼，並設定 usri 的 \* \_ usr \_ 批註欄位。 另一個例外狀況是帳戶操作員無法修改管理帳戶。 以下列出的函式會受到影響：

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)、 [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers)、 [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)、 [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers)、 [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)、 [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)、 [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword)、 [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)、 [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset)、 [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)、 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

一般而言，呼叫端必須擁有整個物件的寫入存取權， [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset)、 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)、 [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) 和 [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) 的呼叫才會成功。 若要進行更精細的存取控制，您應該考慮使用 ADSI。 如需 ADSI 的詳細資訊，請參閱 [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)。

如需控制安全物件之存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)、 [許可權](/windows/desktop/SecAuthZ/privileges)和 [安全物件](/windows/desktop/SecAuthZ/securable-objects)。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

 

 