---
description: 下列範例會讀取寫入效能資料至記錄檔範例中記錄檔的資料。
ms.assetid: acec1506-473a-43c9-9b57-ad8c00e8f250
title: 從記錄檔讀取效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d2d04e16e815811fd9917fa28e6fb7b1f4d2358c72a075b1ae0216c8bc4a89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793577"
---
# <a name="reading-performance-data-from-a-log-file"></a>從記錄檔讀取效能資料

下列範例會讀取寫入 [效能資料至記錄](writing-performance-data-to-a-log-file.md) 檔範例中記錄檔的資料。 它會使用 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) 函數來從記錄檔中取出資料，並使用 [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) 函數來格式化要顯示的資料。


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must contain a valid log file name.\n");
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HCOUNTER hCounter = NULL;
    PDH_STATUS status = ERROR_SUCCESS;
    DWORD dwFormat = PDH_FMT_DOUBLE; 
    PDH_FMT_COUNTERVALUE ItemBuffer;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Opens the log file to write performance data
    status = PdhOpenQuery(argv[1], 0, &hQuery);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", status);
        goto cleanup;
    }
   
    // Add the same counter used when writing the log file.
    status = PdhAddCounter(hQuery, COUNTER_PATH, 0, &hCounter);
   
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", status);
        goto cleanup;
    }

    // Read a performance data record.
    status = PdhCollectQueryData(hQuery);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhCollectQueryData failed with 0x%x\n", status);
        goto cleanup;
    }

    while (ERROR_SUCCESS == status) 
    { 
        // Read the next record
        status = PdhCollectQueryData(hQuery);

        if (ERROR_SUCCESS == status)
        {
            // Format the performance data record.
            status = PdhGetFormattedCounterValue(hCounter,
                dwFormat,
                (LPDWORD)NULL,
                &ItemBuffer);

            if (ERROR_SUCCESS != status)
            {
                wprintf(L"PdhGetFormattedCounterValue failed with 0x%x.\n", status);
                goto cleanup;
            }

            wprintf(L"Formatted counter value = %.20g\n", ItemBuffer.doubleValue);
        }
        else
        {
            if (PDH_NO_MORE_DATA != status)
            {
                wprintf(L"PdhCollectQueryData failed with 0x%x\n", status);
            }
        }
    }

cleanup:

    // Close the query.
    if (hQuery)
        PdhCloseQuery(hQuery);
}
```



 

 



