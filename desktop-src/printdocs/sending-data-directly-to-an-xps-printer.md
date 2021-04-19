---
description: 本主題說明如何將印表機控制資料直接傳送至使用 XPSDrv 印表機驅動程式的印表機。
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 如何：將資料直接傳送到 XPS 印表機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997122"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>如何：將資料直接傳送到 XPS 印表機

本主題說明如何將印表機控制資料直接傳送至使用 XPSDrv 印表機驅動程式的印表機。

下列步驟說明如何將資料直接傳送至印表機。 接下來的程式碼範例也會說明這些步驟。

1.  呼叫 [**OpenPrinter**](openprinter.md) 以取得印表機的控制碼。
2.  使用印表機資料初始化 [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) 結構。
3.  呼叫 [**StartDocPrinter**](startdocprinter.md) 以指出應用程式將會傳送檔資料至印表機。
4.  呼叫 [**WritePrinter**](writeprinter.md) 以傳送資料。
5.  呼叫 [**EndDocPrinter**](enddocprinter.md) ，表示已傳送此檔的所有資料。
6.  呼叫 [**ClosePrinter**](closeprinter.md) 來釋放資源。

將印表機控制資料直接傳送至使用 XPSDrv 印表機驅動程式的印表機。


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }

    return bStatus;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 
