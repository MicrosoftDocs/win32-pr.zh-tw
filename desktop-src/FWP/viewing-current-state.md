---
title: 正在查看目前的狀態
description: 下列範例程式碼示範如何尋找可能影響伺服器應用程式的所有篩選準則。
ms.assetid: fd6ca153-cd9a-4def-b017-9eff298b3343
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc509198670f50d001c114d88b944cbbcf065ba9b2e73e53ac05652025271ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638998"
---
# <a name="viewing-current-state"></a>正在查看目前的狀態

下列範例程式碼示範如何尋找可能會影響伺服器應用程式的所有篩選準則。

> [!Note]  
> 篩選準則與下層 **IsPortAllowed** API 所支援的條件相同。

 


```C++
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment (lib, "fwpuclnt.lib")

#define EXIT_ON_ERROR(fnName) \
   if (result != ERROR_SUCCESS) \
   { \
      printf(#fnName " = 0x%08X\n", result); \
      goto CLEANUP; \
   }

DWORD InitFilterConditions(
         __in_opt PCWSTR appPath,
         __in_opt const SOCKADDR* localAddr,
         __in_opt UINT8 ipProtocol,
         __in UINT32 numCondsIn,
         __out_ecount_part(numCondsIn, *numCondsOut)
            FWPM_FILTER_CONDITION0* conds,
         __out UINT32* numCondsOut,
         __deref_out FWP_BYTE_BLOB** appId
         )
{
    return 0;
}

DWORD FindMatchingFilters(
         __in HANDLE engine,
         __in const GUID* layerKey,
         __in_opt PCWSTR appPath,
         __in_opt const SOCKADDR* localAddr,
         __in_opt UINT8 ipProtocol,
         __deref_out_ecount(*numFilters) FWPM_FILTER0*** filters,
         __out UINT32* numFilters
         )
{
   DWORD result = ERROR_SUCCESS;
   FWPM_FILTER_CONDITION0 conds[4];
   UINT32 numConds;
   FWP_BYTE_BLOB* appBlob = NULL;
   FWPM_FILTER_ENUM_TEMPLATE0 enumTempl;
   HANDLE enumHandle = NULL;

   result = InitFilterConditions(
               appPath,
               &localAddr,
               ipProtocol,
               ARRAYSIZE(conds),
               conds,
               &numConds,
               &appBlob
               );
   EXIT_ON_ERROR(InitFilterConditions);

   memset(&enumTempl, 0, sizeof(enumTempl));
   enumTempl.layerKey = *layerKey;
   enumTempl.numFilterConditions = numConds;
   if (numConds > 0)
   {
      enumTempl.filterCondition = conds;
   }
   // We want to see all filters regardless of action.
   enumTempl.actionMask = 0xFFFFFFFF;

   result = FwpmFilterCreateEnumHandle0(
               engine,
               &enumTempl,
               &enumHandle
               );
   EXIT_ON_ERROR(FwpmFilterCreateEnumHandle0);

   result = FwpmFilterEnum0(
               engine,
               enumHandle,
               INFINITE,
               filters,
               numFilters
               );
   EXIT_ON_ERROR(FwpmFilterEnum0);

CLEANUP:
   FwpmFilterDestroyEnumHandle0(engine, enumHandle);
   FwpmFreeMemory0((void**)&appBlob);
   return result;
}

DWORD wmain(int argc,
            wchar_t* argv[])
{
   UNREFERENCED_PARAMETER(argc);
   UNREFERENCED_PARAMETER(argv);
   
   // Open a session to the filter engine
   HANDLE engineHandle = 0;

   // Use dynamic sessions for efficiency and safety:
   //  - All objects associated with the dynamic session are deleted with one call.
   //  - Filtering policy objects are deleted even when the application crashes. 
   FWPM_SESSION0 session;
   memset(&session, 0, sizeof(session));
   session.flags = FWPM_SESSION_FLAG_DYNAMIC;

   UINT32 numFilters = 0;
   FWPM_FILTER0** filters = 0;
   DWORD result = FwpmEngineOpen0(NULL, RPC_C_AUTHN_WINNT, NULL, &session, &engineHandle);
   EXIT_ON_ERROR(FwpmEngineOpen0);

   result = FindMatchingFilters(
         engineHandle,
         &FWPM_LAYER_ALE_AUTH_LISTEN_V4,
         0,
         0,
         0,
         &filters,
         &numFilters
         );

CLEANUP:  
   if (result != ERROR_SUCCESS)
   {
       printf("Error: %x\n", result);
   }
   else
   {
       for (int i = 0; i < numFilters; i++)
       {
              printf("\n%d. %ws", i + 1, (filters[i])->displayData.name);
       }
       printf("\nSuccess: %d filters", numFilters);
   }

 FwpmFreeMemory0((void**)filters);

 return result;
}
```



 

 




