---
title: 強制使用者變更登入密碼
description: 這個程式碼範例會示範如何強制使用者使用 NetUserGetInfo 和 NetUserSetInfo 函數和使用者 \_ 資訊3結構，在下一次登入時變更登入密碼 \_ 。
ms.assetid: 828f5d72-3e19-4b65-a1db-ac702fd4cfde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3d0910f77c2553a55a53f1393aae5c9535982
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840203"
---
# <a name="forcing-a-user-to-change-the-logon-password"></a><span data-ttu-id="bbe19-103">強制使用者變更登入密碼</span><span class="sxs-lookup"><span data-stu-id="bbe19-103">Forcing a User to Change the Logon Password</span></span>

<span data-ttu-id="bbe19-104">這個程式碼範例會示範如何強制使用者使用 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) 和 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數和 [**使用者 \_ 資訊 \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) 結構，在下一次登入時變更登入密碼。</span><span class="sxs-lookup"><span data-stu-id="bbe19-104">This code sample demonstrates how to force a user to change the logon password on the next logon using the [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions and the [**USER\_INFO\_3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) structure.</span></span> <span data-ttu-id="bbe19-105">請注意，從 Windows XP 開始，建議您改用 [**USER \_ INFO \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) 結構。</span><span class="sxs-lookup"><span data-stu-id="bbe19-105">Note that starting with Windows XP, it is recommended that you use the [**USER\_INFO\_4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) structure instead.</span></span>

<span data-ttu-id="bbe19-106">使用下列程式碼片段，將 **使用者 \_ 資訊 \_ 3** 結構的 **usri3 \_ 密碼 \_ 過期** 成員設定為非零值：</span><span class="sxs-lookup"><span data-stu-id="bbe19-106">Set the **usri3\_password\_expired** member of the **USER\_INFO\_3** structure to a nonzero value using the following code fragment:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

#define USERNAME L"your_user_name"
#define SERVER L"\\\\server"

void main( void )
{
    PUSER_INFO_3 pUsr = NULL;
    NET_API_STATUS netRet = 0;
    DWORD dwParmError = 0;
 //
 // First, retrieve the user information at level 3. This is 
 // necessary to prevent resetting other user information when 
 // the NetUserSetInfo call is made.
 //
   netRet = NetUserGetInfo( SERVER, USERNAME, 3, (LPBYTE *)&pUsr);

   if( netRet == NERR_Success )
   {
     //
     // The function was successful; set the usri3_password_expired value to 
     // a nonzero value. Call the NetUserSetInfo function.
     //
        pUsr->usri3_password_expired = TRUE;
        netRet = NetUserSetInfo( SERVER, USERNAME, 3, (LPBYTE)pUsr, &dwParmError);
    //
    // A zero return indicates success. 
    // If the return value is ERROR_INVALID_PARAMETER, 
    //  the dwParmError parameter will contain a value indicating the 
    //  invalid parameter within the user_info_3 structure. These values 
    //  are defined in the lmaccess.h file.
    //
        if( netRet == NERR_Success )
            printf("User %S will need to change password at next logon", USERNAME);
        else printf("Error %d occurred. Parm Error %d returned.\n", netRet, dwParmError);
    //
    // Must free the buffer returned by NetUserGetInfo.
    //
        NetApiBufferFree( pUsr);
    }
    else printf("NetUserGetInfo failed: %d\n", netRet);
}
```



 

 




