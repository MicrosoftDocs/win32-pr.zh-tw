---
title: 遍歷模組清單
description: 下列範例會取得指定進程的模組清單。
ms.assetid: 8efe1e13-6222-496a-bff3-90f53b03c750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f84907cfeba5a9106616d68a3039dd1555e0f4c238ae111df4c886f7664f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419188"
---
# <a name="traversing-the-module-list"></a>遍歷模組清單

下列範例會取得指定進程的模組清單。 此函式 `ListProcessModules` 會使用 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) 函式來取得與指定進程相關聯之模組的快照，然後使用 [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) 和 [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) 函式逐步解說清單。 的 `dwPID` 參數會 `ListProcessModules` 識別要列舉模組的進程，通常是藉由呼叫 **CreateToolhelp32Snapshot** 來列舉系統上執行的處理常式所取得。 請參閱針對使用此函式的簡單主控台應用程式， [製作快照和查看進程](taking-a-snapshot-and-viewing-processes.md) 。

簡單的錯誤報表函式會 `printError` 顯示任何失敗的原因，這通常是由安全性限制所導致。


```C++
#include <windows.h> 
#include <tlhelp32.h> 
#include <tchar.h> 
 
//  Forward declarations: 
BOOL ListProcessModules( DWORD dwPID ); 
void printError( TCHAR* msg ); 
 
int main( void )
{
  ListProcessModules(GetCurrentProcessId() );
  return 0;
}

BOOL ListProcessModules( DWORD dwPID ) 
{ 
  HANDLE hModuleSnap = INVALID_HANDLE_VALUE; 
  MODULEENTRY32 me32; 
 
//  Take a snapshot of all modules in the specified process. 
  hModuleSnap = CreateToolhelp32Snapshot( TH32CS_SNAPMODULE, dwPID ); 
  if( hModuleSnap == INVALID_HANDLE_VALUE ) 
  { 
    printError( TEXT("CreateToolhelp32Snapshot (of modules)") ); 
    return( FALSE ); 
  } 
 
//  Set the size of the structure before using it. 
  me32.dwSize = sizeof( MODULEENTRY32 ); 
 
//  Retrieve information about the first module, 
//  and exit if unsuccessful 
  if( !Module32First( hModuleSnap, &me32 ) ) 
  { 
    printError( TEXT("Module32First") );  // Show cause of failure 
    CloseHandle( hModuleSnap );     // Must clean up the snapshot object! 
    return( FALSE ); 
  } 
 
//  Now walk the module list of the process, 
//  and display information about each module 
  do 
  { 
    _tprintf( TEXT("\n\n     MODULE NAME:     %s"),             me32.szModule ); 
    _tprintf( TEXT("\n     executable     = %s"),             me32.szExePath ); 
    _tprintf( TEXT("\n     process ID     = 0x%08X"),         me32.th32ProcessID ); 
    _tprintf( TEXT("\n     ref count (g)  =     0x%04X"),     me32.GlblcntUsage ); 
    _tprintf( TEXT("\n     ref count (p)  =     0x%04X"),     me32.ProccntUsage ); 
    _tprintf( TEXT("\n     base address   = 0x%08X"), (DWORD) me32.modBaseAddr ); 
    _tprintf( TEXT("\n     base size      = %d"),             me32.modBaseSize ); 
 
  } while( Module32Next( hModuleSnap, &me32 ) ); 

    _tprintf( TEXT("\n"));
 
//  Do not forget to clean up the snapshot object. 
  CloseHandle( hModuleSnap ); 
  return( TRUE ); 
} 
 
 
void printError( TCHAR* msg )
{
  DWORD eNum;
  TCHAR sysMsg[256];
  TCHAR* p;

  eNum = GetLastError( );
  FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS,
         NULL, eNum,
         MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
         sysMsg, 256, NULL );

  // Trim the end of the line and terminate it with a null
  p = sysMsg;
  while( ( *p > 31 ) || ( *p == 9 ) )
    ++p;
  do { *p-- = 0; } while( ( p >= sysMsg ) &&
                          ( ( *p == '.' ) || ( *p < 33 ) ) );

  // Display the message
  _tprintf( TEXT("\n  WARNING: %s failed with error %d (%s)"), msg, eNum, sysMsg );
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[課程模組](module-walking.md)
</dt> </dl>

 

 




