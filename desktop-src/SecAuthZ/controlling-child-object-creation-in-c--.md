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
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="4d576-103">控制在 c + + 中建立子物件</span><span class="sxs-lookup"><span data-stu-id="4d576-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="4d576-104">您可以使用容器物件的 DACL 來控制可在容器內建立子物件的人員。</span><span class="sxs-lookup"><span data-stu-id="4d576-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="4d576-105">這一點很重要，因為物件的建立者通常會指派為物件的擁有者，而物件的擁有者可以控制物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="4d576-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="4d576-106">不同類型的容器物件具有特定存取權限，可控制建立子物件的能力。</span><span class="sxs-lookup"><span data-stu-id="4d576-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="4d576-107">例如，執行緒必須有登錄機碼的金鑰建立子機碼存取權，才能在機 \_ \_ \_ 碼下建立子機碼。</span><span class="sxs-lookup"><span data-stu-id="4d576-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="4d576-108">登錄機碼的 DACL 可以包含允許或拒絕此存取權限的 Ace。</span><span class="sxs-lookup"><span data-stu-id="4d576-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="4d576-109">同樣地，NTFS 也支援「檔案 \_ 新增檔案 \_ 和檔案 \_ 新增子目錄」存取權限，以控制在 \_ 目錄中建立檔案或目錄的能力。</span><span class="sxs-lookup"><span data-stu-id="4d576-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="4d576-110">ADS 右邊的 [建立子系] 存取權限會 \_ \_ 控制在 \_ \_ 目錄服務中建立子物件 (DS) 物件。</span><span class="sxs-lookup"><span data-stu-id="4d576-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="4d576-111">不過，DS 物件可以包含不同類型的物件，因此系統支援更細微的控制。</span><span class="sxs-lookup"><span data-stu-id="4d576-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="4d576-112">您可以使用 [特定物件的 ace](object-specific-aces.md) 來允許或拒絕建立指定之子物件類型的許可權。</span><span class="sxs-lookup"><span data-stu-id="4d576-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="4d576-113">您可以允許使用者建立一種類型的子物件，同時防止使用者建立其他類型的子物件。</span><span class="sxs-lookup"><span data-stu-id="4d576-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="4d576-114">下列範例會使用 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) 函式，將特定物件的 ACE 新增至 ACL。</span><span class="sxs-lookup"><span data-stu-id="4d576-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="4d576-115">ACE 會授與許可權來建立指定的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="4d576-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="4d576-116">[**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)結構的 **grfAccessPermissions** 成員會設定為 [ADS \_ RIGHT \_ DS 建立子系]， \_ \_ 以指出 ACE 會控制子物件的建立。</span><span class="sxs-lookup"><span data-stu-id="4d576-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="4d576-117">[**物件 \_ 和 \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid)結構的 **ObjectsPresent** 成員會設定為目前的 ACE \_ 物件 \_ 類型， \_ 以指出 **ObjectTypeGuid** 成員包含有效的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4d576-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="4d576-118">GUID 會識別要控制其建立的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="4d576-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="4d576-119">在下列範例中，pOldDACL 必須是現有 [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) 結構的有效指標。</span><span class="sxs-lookup"><span data-stu-id="4d576-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="4d576-120">如需有關如何建立物件之 **ACL** 結構的詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](creating-a-security-descriptor-for-a-new-object-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="4d576-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


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



 

 



