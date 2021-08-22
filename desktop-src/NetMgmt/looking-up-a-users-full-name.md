---
title: 查閱使用者的完整名稱
description: 電腦可以組織成網域，也就是電腦網路的集合。 網域系統管理員會維護集中式使用者和組帳戶資訊。
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdff00483b38ef12355af4dcda4a48d60bf849a8fd5d6829640ae8907e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012516"
---
# <a name="looking-up-a-users-full-name"></a>查閱使用者的完整名稱

電腦可以組織成 *網域*，也就是電腦網路的集合。 網域系統管理員會維護集中式使用者和組帳戶資訊。

若要尋找使用者的完整名稱，請指定使用者名稱和功能變數名稱：

-   如果使用者名稱和功能變數名稱不是 Unicode 字串，請將其轉換成 Unicode。
-   藉由呼叫 [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)，查詢網域控制站 (DC) 的電腦名稱稱。
-   藉由呼叫 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)來查閱 DC 電腦上的使用者名稱。
-   將完整使用者名稱轉換成 ANSI，除非程式預期使用 Unicode 字串。

下列範例程式碼是 (GetFullName) 的函式，此函式會接受前兩個引數中的使用者名稱和功能變數名稱，並在第三個引數中傳回使用者的完整名稱。


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




