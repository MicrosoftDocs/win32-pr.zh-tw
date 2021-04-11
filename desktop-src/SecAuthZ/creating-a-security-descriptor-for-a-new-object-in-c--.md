---
description: 下列範例會使用下列進程，為新的登錄機碼建立安全描述項。 類似的程式碼可以用來建立其他物件類型的安全描述項。
ms.assetid: 866992a7-95c4-4094-87bb-e6d8eeb24317
title: 在 c + + 中建立新物件的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17687b60999bc4e6828c9769eec32ec4ce5afb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848358"
---
# <a name="creating-a-security-descriptor-for-a-new-object-in-c"></a><span data-ttu-id="268af-104">在 c + + 中建立新物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="268af-104">Creating a Security Descriptor for a New Object in C++</span></span>

<span data-ttu-id="268af-105">下列範例會使用下列進程，為新的登錄機碼建立 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 。</span><span class="sxs-lookup"><span data-stu-id="268af-105">The following example creates a [*security descriptor*](/windows/desktop/SecGloss/s-gly) for a new registry key using the following process.</span></span> <span data-ttu-id="268af-106">類似的程式碼可以用來建立其他物件類型的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="268af-106">Similar code can be used to create a security descriptor for other object types.</span></span>

-   <span data-ttu-id="268af-107">此範例會使用兩個 Ace 的資訊來填滿 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="268af-107">The example fills an array of [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structures with the information for two ACEs.</span></span> <span data-ttu-id="268af-108">一個 ACE 允許所有人的讀取存取;另一個 ACE 允許系統管理員的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="268af-108">One ACE allows read access to everyone; the other ACE allows full access to administrators.</span></span>
-   <span data-ttu-id="268af-109">[**明確的 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)陣列會傳遞至 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)函式，以建立安全描述項的 DACL。</span><span class="sxs-lookup"><span data-stu-id="268af-109">The [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) array is passed to the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to create a DACL for the security descriptor.</span></span>
-   <span data-ttu-id="268af-110">配置安全描述項的記憶體之後，此範例會呼叫 [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) 和 [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) 函式，以初始化安全描述項並附加 DACL。</span><span class="sxs-lookup"><span data-stu-id="268af-110">After allocating memory for the security descriptor, the example calls the [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) and [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) functions to initialize the security descriptor and attach the DACL.</span></span>
-   <span data-ttu-id="268af-111">然後，安全描述項會儲存在安全性 \_ 屬性結構中，並傳遞至 [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa) 函式，以將安全描述項附加至新建立的金鑰。</span><span class="sxs-lookup"><span data-stu-id="268af-111">The security descriptor is then stored in a SECURITY\_ATTRIBUTES structure and passed to the [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa) function, which attaches the security descriptor to the newly created key.</span></span>


```C++
#pragma comment(lib, "advapi32.lib")

#include <windows.h>
#include <stdio.h>
#include <aclapi.h>
#include <tchar.h>

void main()
{

    DWORD dwRes, dwDisposition;
    PSID pEveryoneSID = NULL, pAdminSID = NULL;
    PACL pACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea[2];
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    SECURITY_ATTRIBUTES sa;
    LONG lRes;
    HKEY hkSub = NULL;

    // Create a well-known SID for the Everyone group.
    if(!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0, 0, 0, 0, 0, 0, 0,
                     &pEveryoneSID))
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow Everyone read access to the key.
    ZeroMemory(&ea, 2 * sizeof(EXPLICIT_ACCESS));
    ea[0].grfAccessPermissions = KEY_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance= NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName  = (LPTSTR) pEveryoneSID;

    // Create a SID for the BUILTIN\Administrators group.
    if(! AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pAdminSID)) 
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup; 
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow the Administrators group full access to
    // the key.
    ea[1].grfAccessPermissions = KEY_ALL_ACCESS;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance= NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName  = (LPTSTR) pAdminSID;

    // Create a new ACL that contains the new ACEs.
    dwRes = SetEntriesInAcl(2, ea, NULL, &pACL);
    if (ERROR_SUCCESS != dwRes) 
    {
        _tprintf(_T("SetEntriesInAcl Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize a security descriptor.  
    pSD = (PSECURITY_DESCRIPTOR) LocalAlloc(LPTR, 
                             SECURITY_DESCRIPTOR_MIN_LENGTH); 
    if (NULL == pSD) 
    { 
        _tprintf(_T("LocalAlloc Error %u\n"), GetLastError());
        goto Cleanup; 
    } 
 
    if (!InitializeSecurityDescriptor(pSD,
            SECURITY_DESCRIPTOR_REVISION)) 
    {  
        _tprintf(_T("InitializeSecurityDescriptor Error %u\n"),
                                GetLastError());
        goto Cleanup; 
    } 
 
    // Add the ACL to the security descriptor. 
    if (!SetSecurityDescriptorDacl(pSD, 
            TRUE,     // bDaclPresent flag   
            pACL, 
            FALSE))   // not a default DACL 
    {  
        _tprintf(_T("SetSecurityDescriptorDacl Error %u\n"),
                GetLastError());
        goto Cleanup; 
    } 

    // Initialize a security attributes structure.
    sa.nLength = sizeof (SECURITY_ATTRIBUTES);
    sa.lpSecurityDescriptor = pSD;
    sa.bInheritHandle = FALSE;

    // Use the security attributes to set the security descriptor 
    // when you create a key.
    lRes = RegCreateKeyEx(HKEY_CURRENT_USER, _T("mykey"), 0, _T(""), 0, 
            KEY_READ | KEY_WRITE, &sa, &hkSub, &dwDisposition); 
    _tprintf(_T("RegCreateKeyEx result %u\n"), lRes );

Cleanup:

    if (pEveryoneSID) 
        FreeSid(pEveryoneSID);
    if (pAdminSID) 
        FreeSid(pAdminSID);
    if (pACL) 
        LocalFree(pACL);
    if (pSD) 
        LocalFree(pSD);
    if (hkSub) 
        RegCloseKey(hkSub);

    return;

}
```



 

 
