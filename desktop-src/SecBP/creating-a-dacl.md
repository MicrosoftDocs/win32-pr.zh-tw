---
description: 顯示如何正確建立 DACL。
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: 建立 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516048"
---
# <a name="creating-a-dacl"></a>建立 DACL

 (DACL) 建立適當的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 是應用程式開發的必要且很重要的一部分。 因為 **Null** dacl 允許所有類型的存取權給所有使用者，所以請勿使用 **Null** 的 dacl。

下列範例顯示如何正確地建立 DACL。 此範例包含一個函式 CreateMyDACL，此函式會使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 在 DACL 中定義授與和拒絕的存取控制。 若要為您的應用程式物件提供不同的存取權，請視需要修改 CreateMyDACL 函數。

在範例中︰

1.  Main 函式會將 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構的位址傳遞給 CreateMyDACL 函數。
2.  CreateMyDACL 函式會使用 SDDL 字串來：
    -   拒絕存取來賓和匿名登入使用者。
    -   允許讀取/寫入/執行已驗證使用者的存取權。
    -   允許系統管理員進行完全控制。

    如需有關 SDDL 字串格式的詳細資訊，請參閱 [安全描述項字串格式](/windows/desktop/SecAuthZ/security-descriptor-string-format)。
3.  CreateMyDACL 函式會呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數，將 SDDL 字串轉換成 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。 安全性 [**\_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構的 **lpSecurityDescriptor** 成員會指向安全描述項。 CreateMyDACL 會將 **ConvertStringSecurityDescriptorToSecurityDescriptor** 的傳回值傳送至 main 函數。
4.  Main 函數會使用更新的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構來指定 [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) 函式所建立之新資料夾的 DACL。
5.  當 main 函式使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構完成時，main 函式會藉由呼叫 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)函數來釋出為 **lpSecurityDescriptor** 成員配置的記憶體。

> [!Note]  
> 若要成功編譯 SDDL 函數（例如 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)），您必須將 \_ WIN32 \_ WINNT 常數定義為0x0500 或更高。

 


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



 

 
