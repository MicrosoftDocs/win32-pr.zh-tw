---
description: 這包含使用 VerifyVersionInfo 函式來判斷應用程式是否正在特定作業系統上執行的範例。
ms.assetid: f39c35ae-9be5-4a03-9079-6fcc63387f6b
title: 驗證系統版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ddb3562230d0708ddc55d0f8214286ea6c3008
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192294"
---
# <a name="verifying-the-system-version"></a><span data-ttu-id="720a7-103">驗證系統版本</span><span class="sxs-lookup"><span data-stu-id="720a7-103">Verifying the System Version</span></span>

<span data-ttu-id="720a7-104">\[ 不建議使用 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 函式來確認目前執行中的作業系統。</span><span class="sxs-lookup"><span data-stu-id="720a7-104">\[ Use of the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to verify the currently running operating system is not recommended.</span></span> <span data-ttu-id="720a7-105">相反地，請使用版本協助程式 [ **api**](version-helper-apis.md)\]</span><span class="sxs-lookup"><span data-stu-id="720a7-105">Instead, use the [**Version Helper APIs**](version-helper-apis.md)\]</span></span>

<span data-ttu-id="720a7-106">這包含使用 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 函式來判斷應用程式是否正在特定作業系統上執行的範例。</span><span class="sxs-lookup"><span data-stu-id="720a7-106">This contains examples that use the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the application is running on a specific operating system.</span></span>

<span data-ttu-id="720a7-107">每個範例中的主要步驟如下所示：</span><span class="sxs-lookup"><span data-stu-id="720a7-107">The main steps in each example are as follows:</span></span>

1.  <span data-ttu-id="720a7-108">在 [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) 結構中設定適當的值。</span><span class="sxs-lookup"><span data-stu-id="720a7-108">Set the appropriate values in the [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) structure.</span></span>
2.  <span data-ttu-id="720a7-109">使用 [**VER \_ set \_ condition**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) 宏設定適當的條件遮罩。</span><span class="sxs-lookup"><span data-stu-id="720a7-109">Set the appropriate condition mask using the [**VER\_SET\_CONDITION**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) macro.</span></span>
3.  <span data-ttu-id="720a7-110">呼叫 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 以執行測試。</span><span class="sxs-lookup"><span data-stu-id="720a7-110">Call [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) to perform the test.</span></span>

## <a name="example-1"></a><span data-ttu-id="720a7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="720a7-111">Example 1</span></span>

<span data-ttu-id="720a7-112">下列範例會判斷應用程式是否在 Windows XP Service Pack 2 (SP2) 或更新版本的 Windows 上執行，例如 Windows Server 2003 或 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="720a7-112">The following example determines whether the application is running on Windows XP with Service Pack 2 (SP2) or a later version of Windows, such as Windows Server 2003 or Windows Vista.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_WinXP_SP2_or_Later () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 1;
   osvi.wServicePackMajor = 2;
   osvi.wServicePackMinor = 0;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR,
      dwlConditionMask);
}

void main()
{
    if(Is_WinXP_SP2_or_Later())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



## <a name="example-2"></a><span data-ttu-id="720a7-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="720a7-113">Example 2</span></span>

<span data-ttu-id="720a7-114">下列程式碼會確認應用程式是在 Windows 2000 伺服器或更新版本的伺服器上執行，例如 Windows Server 2003 或 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="720a7-114">The following code verifies that the application is running on Windows 2000 Server or a later server, such as Windows Server 2003 or Windows Server 2008.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_Win_Server() 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 0;
   osvi.wServicePackMajor = 0;
   osvi.wServicePackMinor = 0;
   osvi.wProductType = VER_NT_SERVER;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, VER_EQUAL );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR |
      VER_PRODUCT_TYPE,
      dwlConditionMask);
}

void main()
{
    if(Is_Win_Server())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



 

 



