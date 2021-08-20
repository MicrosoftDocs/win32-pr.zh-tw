---
description: 本主題稍後的程式碼範例會示範如何將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 如何：將資料直接傳送至 GDI 印表機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d89dd847a71bbf90c04b8a585ca51ac7f68482cf579c22fac270d869ab9b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056228"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>如何：將資料直接傳送至 GDI 印表機

本主題稍後的程式碼範例會示範如何將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。

下列步驟說明如何將資料直接傳送至印表機。 接下來的程式碼範例也會說明這些步驟。

1.  呼叫 [**OpenPrinter**](openprinter.md) 以取得印表機的控制碼。
2.  使用印表機資料初始化 [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) 結構。
3.  呼叫 [**StartDocPrinter**](startdocprinter.md) 以指出應用程式將會傳送檔資料至印表機。
4.  呼叫 [**StartPagePrinter**](startpageprinter.md) 以指出應用程式將會傳送新頁面至印表機。
5.  呼叫 [**WritePrinter**](writeprinter.md) 以傳送資料。
6.  呼叫 [**EndPagePrinter**](endpageprinter.md) ，表示已傳送目前頁面的所有資料。
7.  呼叫 [**EndDocPrinter**](enddocprinter.md) ，表示已傳送此檔的所有資料。
8.  呼叫 [**ClosePrinter**](closeprinter.md) 來釋放資源。

將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
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

 

 
