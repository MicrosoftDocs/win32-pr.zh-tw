---
description: 下列範例會在設定計時器時，將非同步程序呼叫與可等候計時器產生關聯 (的) 函式（也稱為完成常式）。
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: 使用可等候計時器搭配非同步程序呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991867"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>使用可等候計時器搭配非同步程序呼叫

下列範例會在設定計時器時，將 [非同步程序呼叫](asynchronous-procedure-calls.md) 與 [可等候計時器](waitable-timer-objects.md) 產生關聯 (的) 函式（也稱為完成常式）。 完成常式的位址是 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 函數的第四個參數。 第五個參數是 void 指標，可讓您用來將引數傳遞至完成常式。

完成常式將由呼叫 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)的相同執行緒執行。 此執行緒必須處於可提供警示狀態，才能執行完成常式。 它會藉由呼叫 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) 函式來完成這項工作，這是可提供警示函數。

每個執行緒都有一個 APC 佇列。 如果在呼叫其中一個可提供警示函數時，執行緒的 APC 佇列中有一個專案，執行緒就不會進入睡眠狀態。 相反地，專案會從 APC 佇列中移除，並呼叫完成常式。

如果 APC 佇列中沒有任何專案，則會暫止執行緒，直到滿足等候為止。 您可以藉由將專案新增至 APC 佇列、等待時間，或將控制碼變成發出信號來滿足等候。 如果由 APC 佇列中的專案來滿足等候，則會喚醒執行緒，並呼叫完成常式。 在此情況下，函式的傳回值是 **等候 \_ IO \_ 完成**。

執行完成常式之後，系統會檢查要處理的 APC 佇列中是否有另一個專案。 只有在處理所有 APC 專案之後，可提供警示函式才會傳回。 因此，如果將專案新增至 APC 佇列的速度比處理的速度快，則可能會永遠不會傳回對可提供警示函數的呼叫。 如果時間比執行完成常式所需的時間還短，則可等候計時器特別可能發生這種情況。

當您使用具有 APC 的可等候計時器時，設定計時器的執行緒不應等候計時器的控制碼。 如此一來，當計時器變成發出信號，而不是將專案新增至 APC 佇列的結果時，就會導致執行緒喚醒。 如此一來，執行緒就不再處於可提供警示狀態，而且不會呼叫完成常式。 在下列程式碼中，當計時器設定為已發出信號的狀態之後，當專案加入執行緒的 APC 佇列時，對 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) 的呼叫會 awakens 執行緒。


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用可等候計時器物件](using-waitable-timer-objects.md)
</dt> </dl>

 

 
