---
title: 將磁片磁碟機指派給共用
description: 下列範例示範如何透過呼叫 WNetAddConnection2 函式，將磁碟機號連接到遠端伺服器共用。 此範例會通知使用者呼叫是否成功。
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376001"
---
# <a name="assigning-a-drive-to-a-share"></a>將磁片磁碟機指派給共用

下列範例示範如何透過呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函式，將磁碟機號連接到遠端伺服器共用。 此範例會通知使用者呼叫是否成功。

若要測試下列程式碼範例，請執行下列步驟：

1.  將下列幾行變更為有效的字串：

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  將檔案新增至名為 AddConn2 的主控台應用程式。
3.  連結程式庫 MPR。LIB 至編譯器的程式庫清單。
4.  編譯並執行程式 AddConn2.EXE。


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 