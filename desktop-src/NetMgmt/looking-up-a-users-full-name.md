---
title: 查閱使用者的完整名稱
description: 電腦可以組織成網域，也就是電腦網路的集合。 網域系統管理員會維護集中式使用者和組帳戶資訊。
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976320"
---
# <a name="looking-up-a-users-full-name"></a><span data-ttu-id="b071d-104">查閱使用者的完整名稱</span><span class="sxs-lookup"><span data-stu-id="b071d-104">Looking Up a User's Full Name</span></span>

<span data-ttu-id="b071d-105">電腦可以組織成 *網域*，也就是電腦網路的集合。</span><span class="sxs-lookup"><span data-stu-id="b071d-105">Computers can be organized into a *domain*, which is a collection of computers network.</span></span> <span data-ttu-id="b071d-106">網域系統管理員會維護集中式使用者和組帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="b071d-106">The domain administrator maintains centralized user and group account information.</span></span>

<span data-ttu-id="b071d-107">若要尋找使用者的完整名稱，請指定使用者名稱和功能變數名稱：</span><span class="sxs-lookup"><span data-stu-id="b071d-107">To find the full name of a user, given the user name and domain name:</span></span>

-   <span data-ttu-id="b071d-108">如果使用者名稱和功能變數名稱不是 Unicode 字串，請將其轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="b071d-108">Convert the user name and domain name to Unicode, if they are not already Unicode strings.</span></span>
-   <span data-ttu-id="b071d-109">藉由呼叫 [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)，查詢網域控制站 (DC) 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b071d-109">Look up the computer name of the domain controller (DC) by calling [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span></span>
-   <span data-ttu-id="b071d-110">藉由呼叫 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)來查閱 DC 電腦上的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b071d-110">Look up the user name on the DC computer by calling [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span></span>
-   <span data-ttu-id="b071d-111">將完整使用者名稱轉換成 ANSI，除非程式預期使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b071d-111">Convert the full user name to ANSI, unless the program is expecting to work with Unicode strings.</span></span>

<span data-ttu-id="b071d-112">下列範例程式碼是 (GetFullName) 的函式，此函式會接受前兩個引數中的使用者名稱和功能變數名稱，並在第三個引數中傳回使用者的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b071d-112">The following sample code is a function (GetFullName) that takes a user name and a domain name in the first two arguments and returns the user's full name in the third argument.</span></span>


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



 

 




