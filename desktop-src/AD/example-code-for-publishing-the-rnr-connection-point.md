---
title: 發行 RnR 連接點的範例程式碼
description: Winsock 服務會使用下列程式碼範例來註冊服務的 RnR 連接點。
ms.assetid: dd2c7ac9-76fc-4366-8654-8048e6793a16
ms.tgt_platform: multiple
keywords:
- 用於發佈 RnR 連接點 AD 的範例程式碼
- Windows 通訊端註冊和解析 AD、範例程式碼、發佈 RnR 連接點
- 發行 RnR 連接點廣告，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8f5337f80f9d05bcd1e9b25a963dadba4da21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183012"
---
# <a name="example-code-for-publishing-the-rnr-connection-point"></a>發行 RnR 連接點的範例程式碼

Winsock 服務會使用下列程式碼範例來註冊服務的 RnR 連接點。


```C++
#include <winsock2.h>
#include <stdio.h>

/***************************************************************************

    serverRegister()

    Registers the RnR connection point for the specified service. WSAStartup 
    must be called before calling this function.

***************************************************************************/

INT serverRegister(SOCKADDR * sa, 
                   GUID *pServiceID, 
                   LPTSTR pszServiceInstanceName, 
                   LPTSTR pszServiceInstanceComment)
{
    DWORD ret;
    WSAVERSION Version;
    WSAQUERYSET QuerySet;
    CSADDR_INFO CSAddrInfo[1];
    SOCKADDR sa_local;

    memset(&QuerySet, 0, sizeof(QuerySet));
    memset(&CSAddrInfo, 0, sizeof(CSAddrInfo));
    memset(&sa_local, 0, sizeof(SOCKADDR));
    sa_local.sa_family = AF_INET;

    // Build the CSAddrInfo structure to contain address
    // data that clients use to establish a connection.
    //
    // Be aware that LocalAddr is set to zero because dynamically
    // assigned port numbers are used.
    //
    CSAddrInfo[0].LocalAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].LocalAddr.lpSockaddr = &sa_local;
    CSAddrInfo[0].RemoteAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].RemoteAddr.lpSockaddr = sa;
    CSAddrInfo[0].iSocketType = SOCK_STREAM;
    CSAddrInfo[0].iProtocol = PF_INET;

    QuerySet.dwSize = sizeof(WSAQUERYSET);
    QuerySet.lpServiceClassId = pServiceID;
    QuerySet.lpszServiceInstanceName = pszServiceInstanceName;
    QuerySet.lpszComment = pszServiceInstanceComment;
    QuerySet.lpVersion = &Version;
    QuerySet.lpVersion->dwVersion = 2;
    QuerySet.lpVersion->ecHow = COMP_NOTLESS;
    QuerySet.dwNameSpace = NS_NTDS;
    QuerySet.dwNumberOfCsAddrs = 1;
    QuerySet.lpcsaBuffer = CSAddrInfo;

    ret = WSASetService( &QuerySet,
                         RNRSERVICE_REGISTER,
                         SERVICE_MULTIPLE);

    return(ret);
}
```



 

 




