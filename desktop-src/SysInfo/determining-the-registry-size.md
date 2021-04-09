---
description: 在 Windows 2000 上，安裝公用程式通常會檢查登錄的目前大小和大小上限，以判斷是否有足夠的可用空間來容納即將新增的新資料。
ms.assetid: 87e7b9de-d571-41e4-817e-29023546e9bd
title: 判斷登錄大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4434b519625cf21c9e0076dc7c21d71e27c01778
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853107"
---
# <a name="determining-the-registry-size"></a><span data-ttu-id="b93b0-103">判斷登錄大小</span><span class="sxs-lookup"><span data-stu-id="b93b0-103">Determining the Registry Size</span></span>

<span data-ttu-id="b93b0-104">在 Windows 2000 上，安裝公用程式通常會檢查登錄的目前大小和大小上限，以判斷是否有足夠的可用空間來容納即將新增的新資料。</span><span class="sxs-lookup"><span data-stu-id="b93b0-104">On Windows 2000, it is common for an installation utility to check the current and maximum size of the registry to determine whether there is enough available space for the new data it will be adding.</span></span> <span data-ttu-id="b93b0-105">這個範例示範如何使用系統物件內的「% Registry 配額使用中」效能計數器，以程式設計方式執行此作業。</span><span class="sxs-lookup"><span data-stu-id="b93b0-105">This sample demonstrates how to do this programmatically using the "% Registry Quota In Use" performance counter within the System object.</span></span>

<span data-ttu-id="b93b0-106">下列範例會使用效能資料協助程式 (PDH) 來取得計數器值;它必須與 Pdh 連結。</span><span class="sxs-lookup"><span data-stu-id="b93b0-106">The following sample uses performance data helper (PDH) to obtain the counter value; it must be linked with Pdh.lib.</span></span> <span data-ttu-id="b93b0-107">PDH 是一組高層級的 Api，用來取得效能資料。</span><span class="sxs-lookup"><span data-stu-id="b93b0-107">PDH is a high-level set of APIs used to obtain performance data.</span></span>

> [!Note]  
> <span data-ttu-id="b93b0-108">不需要在 Windows Server 2003 或 Windows XP 上執行此登錄大小檢查，因為它們沒有登錄配額限制。</span><span class="sxs-lookup"><span data-stu-id="b93b0-108">It is not necessary to implement this registry size-check on Windows Server 2003 or Windows XP because they do not have a registry quota limit.</span></span>

 


```C++
//*******************************************************************
// 
//  Determines the current and maximum registry size.
//
//*******************************************************************

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <pdh.h>

PDH_STATUS GetRegistrySize( LPTSTR szMachineName, 
    LPDWORD lpdwCurrentSize, LPDWORD lpdwMaximumSize );

//*******************************************************************
// 
//  Entry point for the program. This function demonstrates how to
//  use the GetRegistrySize function implemented below.
// 
//  It will use the first argument, if present, as the name of the
//  computer whose registry you wish to determine. If unspecified,
//  it will use the local computer.
//*******************************************************************

int _tmain( int argc, TCHAR *argv[] ) 
{

    LPTSTR      szMachineName  = NULL;
    PDH_STATUS  pdhStatus      = 0;
    DWORD       dwCurrent      = 0;
    DWORD       dwMaximum      = 0;

    // Allow a computer name to be specified on the command line.
    if ( argc > 1 )
        szMachineName = argv[1];

    // Get the registry size.
    pdhStatus=GetRegistrySize(szMachineName, &dwCurrent, &dwMaximum);

    // Print the results.
    if ( pdhStatus == ERROR_SUCCESS ) 
    {
        _tprintf( TEXT("Registry size: %ld bytes\n"), dwCurrent );
        _tprintf( TEXT("Max registry size: %ld bytes\n"), dwMaximum );

    } 
    else 
    {
        // If the operation failed, print the PDH error message.
        LPTSTR szMessage = NULL;

        FormatMessage( FORMAT_MESSAGE_ALLOCATE_BUFFER |
            FORMAT_MESSAGE_FROM_HMODULE,
            GetModuleHandle( TEXT("PDH.DLL") ), pdhStatus,
            MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
            szMessage, 0, NULL );

        _tprintf( TEXT("GetRegistrySize failed:  %s"), szMessage );

        LocalFree( szMessage );
    }

    return 0;
}

//*******************************************************************
// 
//  Retrieves the current and maximum registry size. It gets this
//  information from the raw counter values for the "% Registry Quota 
//  In Use" performance counter within the System object.
// 
//  PARAMETERS:   
//      szMachineName - Null-terminated string that specifies the
//          name of the computer whose registry you wish to query.
//          If this parameter is NULL, the local computer is used.
// 
//      lpdwCurrentSize - Receives the current registry size.
// 
//      lpdwMaximumSize - Receives the maximum registry size.
// 
//  RETURN VALUE: 
//      ERROR_SUCCESS if successful. Otherwise, the function
//      returns a PDH error code. These error codes can be
//      found in PDHMSG.H. A textual error message can be
//      retrieved from PDH.DLL using the FormatMessage function.
// 
//******************************************************************

PDH_STATUS GetRegistrySize( LPTSTR szMachineName, 
    LPDWORD lpdwCurrentSize, LPDWORD lpdwMaximumSize ) 
{
    PDH_STATUS  pdhResult   = 0;
    TCHAR       szCounterPath[1024];
    DWORD       dwPathSize  = 1024;
    PDH_COUNTER_PATH_ELEMENTS pe;
    PDH_RAW_COUNTER pdhRawValues;
    HQUERY      hQuery      = NULL;
    HCOUNTER    hCounter    = NULL;
    DWORD       dwType      = 0;

    // Open PDH query
    pdhResult = PdhOpenQuery( NULL, 0, &hQuery );
    if ( pdhResult != ERROR_SUCCESS )
        return pdhResult;

    __try 
    {
        // Create counter path
        pe.szMachineName     = szMachineName;
        pe.szObjectName      = TEXT("System");
        pe.szInstanceName    = NULL;
        pe.szParentInstance  = NULL;
        pe.dwInstanceIndex   = 1;
        pe.szCounterName     = TEXT("% Registry Quota In Use");

        pdhResult = PdhMakeCounterPath( &pe, szCounterPath, 
            &dwPathSize, 0 );
        if ( pdhResult != ERROR_SUCCESS )
            __leave;

        // Add the counter to the query
        pdhResult=PdhAddCounter(hQuery, szCounterPath, 0, &hCounter);
        if ( pdhResult != ERROR_SUCCESS ) 
            __leave;

        // Run the query to collect the performance data
        pdhResult = PdhCollectQueryData( hQuery );
        if ( pdhResult != ERROR_SUCCESS ) 
            __leave;

        // Retrieve the raw counter data:
        //    The dividend (FirstValue) is the current registry size
        //    The divisor (SecondValue) is the maximum registry size
        ZeroMemory( &pdhRawValues, sizeof(pdhRawValues) );
        pdhResult = PdhGetRawCounterValue( hCounter, &dwType,
            &pdhRawValues );
        if ( pdhResult != ERROR_SUCCESS )
            __leave;

        // Store the sizes in variables.
        if ( lpdwCurrentSize )
            *lpdwCurrentSize = (DWORD) pdhRawValues.FirstValue;
         
        if ( lpdwMaximumSize )
            *lpdwMaximumSize = (DWORD) pdhRawValues.SecondValue;

    } 
    __finally 
    {
        // Close the query
        PdhCloseQuery( hQuery );
    }

    return 0;
}
```



 

 



