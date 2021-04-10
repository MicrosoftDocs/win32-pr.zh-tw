---
title: 判斷共用的位置
description: 下列範例示範如何呼叫 WNetGetUniversalName 函式，以判斷重新導向磁片磁碟機上共用的位置。
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933445"
---
# <a name="determining-the-location-of-a-share"></a>判斷共用的位置

下列範例示範如何呼叫 [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) 函式，以判斷重新導向磁片磁碟機上共用的位置。

首先，程式碼範例會呼叫 **WNetGetUniversalName** 函式，並指定 [**通用 \_ 名稱 \_ 資訊**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) 資訊層級，以取得資源 (UNC) 名稱字串的通用命名慣例指標。 然後，此範例會第二次呼叫 **WNetGetUniversalName** ， [**指定 \_ 遠端 \_ 名稱**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) 資訊層級來抓取兩個額外的網路連接資訊字串。 如果呼叫成功，範例會列印共用的位置。

若要測試下列程式碼範例，請執行下列步驟：

1.  將程式碼範例命名為 GetUni .cpp。
2.  將範例新增至名為 GetUni 的主控台應用程式。
3.  將 Shell32 .lib、Mpr 和 NetApi32 程式庫連結至程式庫的編譯器清單。
4.  從命令提示字元，變更為 GetUni 目錄。
5.  編譯 GetUni .cpp。
6.  執行檔案 GetUni.exe 後面接著磁碟機號和冒號，如下所示：

    **GetUni H：\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 