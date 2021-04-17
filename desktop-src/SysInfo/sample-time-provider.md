---
description: 下列範例示範如何建立時間提供者的結構。 在此範例中，DLL 支援兩個硬體時間提供者。
ms.assetid: 6be08c49-be68-4b75-b740-fc1d5a2ff592
title: 範例時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a5f04f7515d73f8851b764ad5758c47848b07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513749"
---
# <a name="sample-time-provider"></a>範例時間提供者

下列範例示範如何建立時間提供者的結構。 在此範例中，DLL 支援兩個硬體時間提供者。

``` syntax
#include <windows.h>
#include "timeprov.h"

// Global variables.
TimeProvSysCallbacks sc;
WCHAR ProviderName1[] = L"MyCompanyMyAppProvider1";
WCHAR ProviderName2[] = L"MyCompanyMyAppProvider2";
const TimeProvHandle htp1 = (TimeProvHandle)1;
const TimeProvHandle htp2 = (TimeProvHandle)2;

// Stores the current set of best samples.
TpcGetSamplesArgs Samples;

// Stores the polling interval the system requires to maintain clock
// stability. The provider need not poll more often.
DWORD dwPollInterval;

HRESULT CALLBACK TimeProvOpen(
   WCHAR *wszName,
   TimeProvSysCallbacks *pSysCallback,
   TimeProvHandle *phTimeProv)
{
   // Spawn a thread to read configuration information from the 
   // registry.
   ;

   // Copy the system callback pointers to a buffer.
   CopyMemory(&sc, (PVOID)pSysCallback, sizeof(TimeProvSysCallbacks));

   // Return the handle to the appropriate time provider.
   if ( lstrcmp(wszName, ProviderName1) == 0 )
      *phTimeProv = htp1;
   else *phTimeProv = htp2;

   return S_OK;
}

HRESULT CALLBACK TimeProvCommand(
   TimeProvHandle hTimeProv,
   TimeProvCmd eCmd,
   PVOID pvArgs)
{
   switch( eCmd )
   {
      case TPC_GetSamples:
      // Return the Samples structure in pvArgs.
         CopyMemory(pvArgs, &Samples, sizeof(TpcGetSamplesArgs));
         break;
      case TPC_PollIntervalChanged:
      // Retrieve the new value.
         sc.pfnGetTimeSysInfo( TSI_PollInterval, &dwPollInterval );
         break;
      case TPC_TimeJumped:
      // Discard samples saved in the Samples structure.
         ZeroMemory(&Samples, sizeof(TpcGetSamplesArgs));
         break;
      case TPC_UpdateConfig:
      // Read the configuration information from the registry.
         break;
   }
   return S_OK;
}

HRESULT CALLBACK TimeProvClose(
   TimeProvHandle hTimeProv)
{
   if( hTimeProv == htp1 )
   {
   // Terminate MyCompanyMyAppProvider1, performing any cleanup.
   ;
   }
   else
   {
   // Terminate MyCompanyMyAppProvider2, performing any cleanup.
   ;
   }

   return S_OK;
}
```

 

 



