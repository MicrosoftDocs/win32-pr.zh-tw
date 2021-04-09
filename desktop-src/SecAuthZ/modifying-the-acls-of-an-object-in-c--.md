---
description: 下列範例會將存取控制專案 (ACE) 新增至物件的任意存取控制清單 (DACL) 。
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: 使用 c + + 修改物件的 Acl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945032"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a><span data-ttu-id="a28fb-103">使用 c + + 修改物件的 Acl</span><span class="sxs-lookup"><span data-stu-id="a28fb-103">Modifying the ACLs of an Object in C++</span></span>

<span data-ttu-id="a28fb-104">下列範例會將 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 新增至物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 。</span><span class="sxs-lookup"><span data-stu-id="a28fb-104">The following example adds an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span>

<span data-ttu-id="a28fb-105">*AccessMode* 參數會決定新 ace 的型別，以及新的 ace 如何與指定之信任者的任何現有 ace 合併。</span><span class="sxs-lookup"><span data-stu-id="a28fb-105">The *AccessMode* parameter determines the type of new ACE and how the new ACE is combined with any existing ACEs for the specified trustee.</span></span> <span data-ttu-id="a28fb-106">使用 \_ AccessMode 參數中的授與存取權、設定 \_ 存取、拒絕 \_ 存取或撤銷 \_ 存取旗標。 </span><span class="sxs-lookup"><span data-stu-id="a28fb-106">Use the GRANT\_ACCESS, SET\_ACCESS, DENY\_ACCESS, or REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="a28fb-107">如需這些旗標的詳細資訊，請參閱 [**存取 \_ 模式**](/windows/win32/api/accctrl/ne-accctrl-access_mode)。</span><span class="sxs-lookup"><span data-stu-id="a28fb-107">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="a28fb-108">您可以使用類似的程式碼來處理 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 。</span><span class="sxs-lookup"><span data-stu-id="a28fb-108">Similar code can be used to work with a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="a28fb-109">\_ \_ 在 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)和 [**SETNAMEDSECURITYINFO**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)函式中指定 sacl 安全性資訊，以取得和設定物件的 sacl。</span><span class="sxs-lookup"><span data-stu-id="a28fb-109">Specify SACL\_SECURITY\_INFORMATION in the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) and [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions to get and set the SACL for the object.</span></span> <span data-ttu-id="a28fb-110">使用 \_ \_ AccessMode 參數中的 SET audit SUCCESS、set \_ AUDIT \_ 失敗和 REVOKE \_ 存取旗標。</span><span class="sxs-lookup"><span data-stu-id="a28fb-110">Use the SET\_AUDIT\_SUCCESS, SET\_AUDIT\_FAILURE, and REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="a28fb-111">如需這些旗標的詳細資訊，請參閱 [**存取 \_ 模式**](/windows/win32/api/accctrl/ne-accctrl-access_mode)。</span><span class="sxs-lookup"><span data-stu-id="a28fb-111">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="a28fb-112">使用此程式碼，將 [特定物件的 ACE](object-specific-aces.md) 新增至目錄服務物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="a28fb-112">Use this code to add an [object-specific ACE](object-specific-aces.md) to the DACL of a directory service object.</span></span> <span data-ttu-id="a28fb-113">若要在物件特定的 ACE 中指定 Guid，請將 *TrusteeForm* 參數設定為「信任者」為「物件」、「 \_ 名稱」或「 \_ \_ \_ 信任者」 \_ 是 \_ 物件 \_ 和 sid， \_ 並將 *pszTrustee* 參數設定為 [**物件 \_ 和 \_ 名稱**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) 或 [**物件 \_ 和 \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a28fb-113">To specify the GUIDs in an object-specific ACE, set the *TrusteeForm* parameter to TRUSTEE\_IS\_OBJECTS\_AND\_NAME or TRUSTEE\_IS\_OBJECTS\_AND\_SID and set the *pszTrustee* parameter to be a pointer to an [**OBJECTS\_AND\_NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) or [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure.</span></span>

<span data-ttu-id="a28fb-114">此範例使用 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 函式來取得現有的 DACL。</span><span class="sxs-lookup"><span data-stu-id="a28fb-114">This example uses the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) function to get the existing DACL.</span></span> <span data-ttu-id="a28fb-115">然後，它會以 ACE 的相關資訊來填滿 [**明確的 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構，並使用 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) 函式，將新的 ace 與 DACL 中的任何現有 ace 合併。</span><span class="sxs-lookup"><span data-stu-id="a28fb-115">Then it fills an [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure with information about an ACE and uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to merge the new ACE with any existing ACEs in the DACL.</span></span> <span data-ttu-id="a28fb-116">最後，此範例會呼叫 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數，以將新的 DACL 附加至物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 。</span><span class="sxs-lookup"><span data-stu-id="a28fb-116">Finally, the example calls the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function to attach the new DACL to the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
