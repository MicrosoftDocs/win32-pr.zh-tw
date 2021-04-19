---
description: 本主題稍後的程式碼範例會示範如何將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 如何：將資料直接傳送至 GDI 印表機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983777"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="3e98a-103">如何：將資料直接傳送至 GDI 印表機</span><span class="sxs-lookup"><span data-stu-id="3e98a-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="3e98a-104">本主題稍後的程式碼範例會示範如何將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="3e98a-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="3e98a-105">下列步驟說明如何將資料直接傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="3e98a-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="3e98a-106">接下來的程式碼範例也會說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="3e98a-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="3e98a-107">呼叫 [**OpenPrinter**](openprinter.md) 以取得印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3e98a-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="3e98a-108">使用印表機資料初始化 [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="3e98a-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="3e98a-109">呼叫 [**StartDocPrinter**](startdocprinter.md) 以指出應用程式將會傳送檔資料至印表機。</span><span class="sxs-lookup"><span data-stu-id="3e98a-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="3e98a-110">呼叫 [**StartPagePrinter**](startpageprinter.md) 以指出應用程式將會傳送新頁面至印表機。</span><span class="sxs-lookup"><span data-stu-id="3e98a-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="3e98a-111">呼叫 [**WritePrinter**](writeprinter.md) 以傳送資料。</span><span class="sxs-lookup"><span data-stu-id="3e98a-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="3e98a-112">呼叫 [**EndPagePrinter**](endpageprinter.md) ，表示已傳送目前頁面的所有資料。</span><span class="sxs-lookup"><span data-stu-id="3e98a-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="3e98a-113">呼叫 [**EndDocPrinter**](enddocprinter.md) ，表示已傳送此檔的所有資料。</span><span class="sxs-lookup"><span data-stu-id="3e98a-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="3e98a-114">呼叫 [**ClosePrinter**](closeprinter.md) 來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="3e98a-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="3e98a-115">將印表機控制資料直接傳送至使用以 GDI 為基礎之印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="3e98a-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3e98a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e98a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e98a-117">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-118">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-119">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-122">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3e98a-123">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e98a-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
