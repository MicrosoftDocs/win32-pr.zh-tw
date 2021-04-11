---
description: 顯示如何正確建立 DACL。
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: 建立 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852103"
---
# <a name="creating-a-dacl"></a><span data-ttu-id="3e876-103">建立 DACL</span><span class="sxs-lookup"><span data-stu-id="3e876-103">Creating a DACL</span></span>

<span data-ttu-id="3e876-104"> (DACL) 建立適當的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 是應用程式開發的必要且很重要的一部分。</span><span class="sxs-lookup"><span data-stu-id="3e876-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="3e876-105">因為 **Null** dacl 允許所有類型的存取權給所有使用者，所以請勿使用 **Null** 的 dacl。</span><span class="sxs-lookup"><span data-stu-id="3e876-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="3e876-106">下列範例顯示如何正確地建立 DACL。</span><span class="sxs-lookup"><span data-stu-id="3e876-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="3e876-107">此範例包含一個函式 CreateMyDACL，此函式會使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 在 DACL 中定義授與和拒絕的存取控制。</span><span class="sxs-lookup"><span data-stu-id="3e876-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="3e876-108">若要為您的應用程式物件提供不同的存取權，請視需要修改 CreateMyDACL 函數。</span><span class="sxs-lookup"><span data-stu-id="3e876-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="3e876-109">在範例中︰</span><span class="sxs-lookup"><span data-stu-id="3e876-109">In the example:</span></span>

1.  <span data-ttu-id="3e876-110">Main 函式會將 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構的位址傳遞給 CreateMyDACL 函數。</span><span class="sxs-lookup"><span data-stu-id="3e876-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="3e876-111">CreateMyDACL 函式會使用 SDDL 字串來：</span><span class="sxs-lookup"><span data-stu-id="3e876-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="3e876-112">拒絕存取來賓和匿名登入使用者。</span><span class="sxs-lookup"><span data-stu-id="3e876-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="3e876-113">允許讀取/寫入/執行已驗證使用者的存取權。</span><span class="sxs-lookup"><span data-stu-id="3e876-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="3e876-114">允許系統管理員進行完全控制。</span><span class="sxs-lookup"><span data-stu-id="3e876-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="3e876-115">如需有關 SDDL 字串格式的詳細資訊，請參閱 [安全描述項字串格式](/windows/desktop/SecAuthZ/security-descriptor-string-format)。</span><span class="sxs-lookup"><span data-stu-id="3e876-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="3e876-116">CreateMyDACL 函式會呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數，將 SDDL 字串轉換成 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="3e876-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="3e876-117">安全性 [**\_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構的 **lpSecurityDescriptor** 成員會指向安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3e876-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="3e876-118">CreateMyDACL 會將 **ConvertStringSecurityDescriptorToSecurityDescriptor** 的傳回值傳送至 main 函數。</span><span class="sxs-lookup"><span data-stu-id="3e876-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="3e876-119">Main 函數會使用更新的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構來指定 [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) 函式所建立之新資料夾的 DACL。</span><span class="sxs-lookup"><span data-stu-id="3e876-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="3e876-120">當 main 函式使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構完成時，main 函式會藉由呼叫 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)函數來釋出為 **lpSecurityDescriptor** 成員配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3e876-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="3e876-121">若要成功編譯 SDDL 函數（例如 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)），您必須將 \_ WIN32 \_ WINNT 常數定義為0x0500 或更高。</span><span class="sxs-lookup"><span data-stu-id="3e876-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
