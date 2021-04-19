---
description: 本主題說明如何取出印表機裝置內容。
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 如何：取出印表機裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979930"
---
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="138af-103">如何：取出印表機裝置內容</span><span class="sxs-lookup"><span data-stu-id="138af-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="138af-104">本主題說明如何取出印表機裝置內容。</span><span class="sxs-lookup"><span data-stu-id="138af-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="138af-105">您可以直接呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 函式來取出印表機裝置內容，也可以透過 [ **列印** 一般] 對話方塊來傳回。</span><span class="sxs-lookup"><span data-stu-id="138af-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="138af-106">當您顯示 [ **列印** 一般] 對話方塊時，使用者將能夠選取印表機、檔的頁面，以及他們想要列印的檔複本數目。</span><span class="sxs-lookup"><span data-stu-id="138af-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="138af-107">[ **列印** 通用] 對話方塊會在資料結構中傳回這些選項。</span><span class="sxs-lookup"><span data-stu-id="138af-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="138af-108">本主題說明如何使用下列方法來取得印表機裝置內容。</span><span class="sxs-lookup"><span data-stu-id="138af-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="138af-109">呼叫 CreateDC</span><span class="sxs-lookup"><span data-stu-id="138af-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="138af-110">顯示列印通用對話方塊</span><span class="sxs-lookup"><span data-stu-id="138af-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="138af-111">使用 PrintDlgEx 函式</span><span class="sxs-lookup"><span data-stu-id="138af-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="138af-112">使用 PrintDlg 函式</span><span class="sxs-lookup"><span data-stu-id="138af-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="138af-113">呼叫 CreateDC</span><span class="sxs-lookup"><span data-stu-id="138af-113">Call CreateDC</span></span>

<span data-ttu-id="138af-114">如果您知道想要列印的裝置，您可以呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ，並將該資訊直接傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="138af-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="138af-115">**CreateDC** 會傳回一個裝置內容，您可以在其中呈現要列印的內容。</span><span class="sxs-lookup"><span data-stu-id="138af-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="138af-116">抓取裝置內容最簡單的呼叫會顯示在下面的程式碼範例中。</span><span class="sxs-lookup"><span data-stu-id="138af-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="138af-117">此範例中的程式碼會將裝置內容抓取到預設顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="138af-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="138af-118">若要轉譯為特定的印表機，您必須指定 "WINSPOOL.DRV" 作為裝置，並將正確的印表機名稱傳遞至 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)。</span><span class="sxs-lookup"><span data-stu-id="138af-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="138af-119">如果您想要在建立裝置內容時，為設備磁碟機提供裝置特定的初始化資料，您也可以在 **CreateDC** 的呼叫中傳遞 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構。</span><span class="sxs-lookup"><span data-stu-id="138af-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="138af-120">下列範例會顯示 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 的呼叫，其中選取了 "winspool.drv" 驅動程式，並依名稱指定印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="138af-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="138af-121">您可以藉由呼叫 [**>enumprinters**](enumprinters.md)函式，取得要傳遞給 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)的精確印表機名稱字串。</span><span class="sxs-lookup"><span data-stu-id="138af-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="138af-122">下列程式碼範例示範如何呼叫 **>enumprinters** ，以及取得本機和本機連接印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="138af-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="138af-123">因為無法事先知道所需的緩衝區大小，所以會呼叫 **>enumprinters** 兩次。</span><span class="sxs-lookup"><span data-stu-id="138af-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="138af-124">第一個呼叫會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="138af-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="138af-125">這項資訊是用來配置所需大小的緩衝區，而第二次呼叫 **>enumprinters** 則會傳回您想要的資料。</span><span class="sxs-lookup"><span data-stu-id="138af-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="138af-126">顯示列印通用對話方塊</span><span class="sxs-lookup"><span data-stu-id="138af-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="138af-127">您可以選擇兩個 **列印** 通用對話方塊來向使用者顯示;您可以藉由呼叫 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式來顯示的較新對話方塊，以及您可以藉由呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數來顯示的舊版樣式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="138af-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="138af-128">下列各節將說明如何從應用程式呼叫每個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="138af-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="138af-129">使用 PrintDlgEx 函式</span><span class="sxs-lookup"><span data-stu-id="138af-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="138af-130">呼叫 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數，以顯示 **列印** 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="138af-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="138af-131">藉由使用屬性工作表，使用者可以指定列印工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="138af-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="138af-132">例如，使用者可以選取要列印的頁面範圍、份數等等。</span><span class="sxs-lookup"><span data-stu-id="138af-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="138af-133">**PrintDlgEx** 也可以取出所選印表機的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="138af-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="138af-134">您可以使用此控制碼來呈現印表機上的輸出。</span><span class="sxs-lookup"><span data-stu-id="138af-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="138af-135">如需示範如何使用 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 來取出印表機裝置內容的範例程式碼，請參閱 [使用通用對話方塊](../dlgbox/using-common-dialog-boxes.md)中的「使用列印屬性工作表」。</span><span class="sxs-lookup"><span data-stu-id="138af-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="138af-136">使用 PrintDlg 函式</span><span class="sxs-lookup"><span data-stu-id="138af-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="138af-137">如果您的應用程式必須在不支援 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式的系統上執行，例如，在執行 windows 2000 之前的 windows 版本的系統上，或不需要 **PrintDlgEx** 函式所提供的額外功能，請使用 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="138af-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="138af-138">下列步驟說明如何顯示較舊的樣式 **列印** 通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="138af-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="138af-139">初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="138af-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="138af-140">呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ，將 [ **列印** 通用] 對話方塊顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="138af-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="138af-141">如果 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 呼叫傳回 **TRUE**，請鎖定傳回的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構記憶體。</span><span class="sxs-lookup"><span data-stu-id="138af-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="138af-142">如果 **PrintDlg** 呼叫傳回 **FALSE**，則使用者在 [**列印** 一般] 對話方塊中按下 [**取消**] 按鈕，就不會再處理任何專案。</span><span class="sxs-lookup"><span data-stu-id="138af-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="138af-143">配置夠大的本機記憶體緩衝區，以包含 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構的複本。</span><span class="sxs-lookup"><span data-stu-id="138af-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="138af-144">將傳回的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構複製到本機配置的結構。</span><span class="sxs-lookup"><span data-stu-id="138af-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="138af-145">儲存 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構中所傳回的其他資訊，而且您將需要處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="138af-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="138af-146">釋放 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 和它所參考的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="138af-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="138af-147">下列範例程式碼說明如何使用 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式來取得裝置內容和所選印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="138af-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



<span data-ttu-id="138af-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="138af-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
