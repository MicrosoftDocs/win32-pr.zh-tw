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
# <a name="how-to-send-data-directly-to-an-xps-printer"></a><span data-ttu-id="b8a76-103">如何：將資料直接傳送到 XPS 印表機</span><span class="sxs-lookup"><span data-stu-id="b8a76-103">How To: Send Data Directly to an XPS Printer</span></span>

<span data-ttu-id="b8a76-104">本主題說明如何將印表機控制資料直接傳送至使用 XPSDrv 印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="b8a76-104">This topic describes how to send printer control data directly to printers that use XPSDrv printer drivers.</span></span>

<span data-ttu-id="b8a76-105">下列步驟說明如何將資料直接傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="b8a76-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="b8a76-106">接下來的程式碼範例也會說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="b8a76-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="b8a76-107">呼叫 [**OpenPrinter**](openprinter.md) 以取得印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8a76-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="b8a76-108">使用印表機資料初始化 [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="b8a76-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="b8a76-109">呼叫 [**StartDocPrinter**](startdocprinter.md) 以指出應用程式將會傳送檔資料至印表機。</span><span class="sxs-lookup"><span data-stu-id="b8a76-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="b8a76-110">呼叫 [**WritePrinter**](writeprinter.md) 以傳送資料。</span><span class="sxs-lookup"><span data-stu-id="b8a76-110">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
5.  <span data-ttu-id="b8a76-111">呼叫 [**EndDocPrinter**](enddocprinter.md) ，表示已傳送此檔的所有資料。</span><span class="sxs-lookup"><span data-stu-id="b8a76-111">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
6.  <span data-ttu-id="b8a76-112">呼叫 [**ClosePrinter**](closeprinter.md) 來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="b8a76-112">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="b8a76-113">將印表機控制資料直接傳送至使用 XPSDrv 印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="b8a76-113">Send printer control data directly to printers that use XPSDrv printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b8a76-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8a76-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8a76-115">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-115">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-116">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-116">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-117">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-117">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-118">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-118">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-119">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-119">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-120">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-120">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b8a76-121">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="b8a76-121">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
