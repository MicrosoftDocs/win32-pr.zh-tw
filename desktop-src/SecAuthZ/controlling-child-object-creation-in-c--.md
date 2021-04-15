---
description: 您可以使用容器物件的 DACL 來控制可在容器內建立子物件的人員。
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: 控制在 c + + 中建立子物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512420"
---
# <a name="controlling-child-object-creation-in-c"></a>控制在 c + + 中建立子物件

您可以使用容器物件的 DACL 來控制可在容器內建立子物件的人員。 這一點很重要，因為物件的建立者通常會指派為物件的擁有者，而物件的擁有者可以控制物件的存取權。

不同類型的容器物件具有特定存取權限，可控制建立子物件的能力。 例如，執行緒必須有登錄機碼的金鑰建立子機碼存取權，才能在機 \_ \_ \_ 碼下建立子機碼。 登錄機碼的 DACL 可以包含允許或拒絕此存取權限的 Ace。 同樣地，NTFS 也支援「檔案 \_ 新增檔案 \_ 和檔案 \_ 新增子目錄」存取權限，以控制在 \_ 目錄中建立檔案或目錄的能力。

ADS 右邊的 [建立子系] 存取權限會 \_ \_ 控制在 \_ \_ 目錄服務中建立子物件 (DS) 物件。 不過，DS 物件可以包含不同類型的物件，因此系統支援更細微的控制。 您可以使用 [特定物件的 ace](object-specific-aces.md) 來允許或拒絕建立指定之子物件類型的許可權。 您可以允許使用者建立一種類型的子物件，同時防止使用者建立其他類型的子物件。

下列範例會使用 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) 函式，將特定物件的 ACE 新增至 ACL。 ACE 會授與許可權來建立指定的子物件類型。 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)結構的 **grfAccessPermissions** 成員會設定為 [ADS \_ RIGHT \_ DS 建立子系]， \_ \_ 以指出 ACE 會控制子物件的建立。 [**物件 \_ 和 \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid)結構的 **ObjectsPresent** 成員會設定為目前的 ACE \_ 物件 \_ 類型， \_ 以指出 **ObjectTypeGuid** 成員包含有效的 GUID。 GUID 會識別要控制其建立的子物件類型。

在下列範例中，pOldDACL 必須是現有 [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) 結構的有效指標。 如需有關如何建立物件之 **ACL** 結構的詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](creating-a-security-descriptor-for-a-new-object-in-c--.md)。


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



