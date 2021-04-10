---
description: 本主題說明如何收集使用者的列印工作資訊。
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: 如何：收集使用者的列印工作資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026734"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="1de2e-103">如何：收集使用者的列印工作資訊</span><span class="sxs-lookup"><span data-stu-id="1de2e-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="1de2e-104">本主題說明如何收集使用者的列印工作資訊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="1de2e-105">概觀</span><span class="sxs-lookup"><span data-stu-id="1de2e-105">Overview</span></span>

<span data-ttu-id="1de2e-106">藉由呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數，從使用者收集列印工作資訊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="1de2e-107">此函式會將 [ **列印** ] 通用對話方塊顯示給使用者，並傳回 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 資料結構中的列印工作資訊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="1de2e-108">當使用者啟動列印工作時，就會顯示 [ **列印** 一般] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="1de2e-109">[ **列印** 通用] 對話方塊是強制回應對話方塊，這表示使用者在一般對話方塊關閉之前，無法與主視窗互動。</span><span class="sxs-lookup"><span data-stu-id="1de2e-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="1de2e-110">收集列印工作資訊</span><span class="sxs-lookup"><span data-stu-id="1de2e-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="1de2e-111">初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構元素。</span><span class="sxs-lookup"><span data-stu-id="1de2e-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="1de2e-112">在程式可以顯示 [ **列印** 一般] 對話方塊之前，它必須配置並初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構。</span><span class="sxs-lookup"><span data-stu-id="1de2e-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="1de2e-113">然後，它會將此結構傳遞至 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式，此函式會顯示對話方塊，並傳回相同結構中的列印工作資料。</span><span class="sxs-lookup"><span data-stu-id="1de2e-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="1de2e-114">下列程式碼範例會示範範例程式如何執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="1de2e-114">The following code example shows how the sample program performs this step.</span></span>

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  <span data-ttu-id="1de2e-115">顯示 [ **列印** 一般] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="1de2e-116">使用已初始化的 [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構來呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ，以顯示 [**列印** 一般] 對話方塊並收集使用者資料，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="1de2e-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="1de2e-117">儲存 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構中的欄位，並啟動列印工作。</span><span class="sxs-lookup"><span data-stu-id="1de2e-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="1de2e-118">[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構包含的資料會描述使用者在 [列印] 對話方塊中所做的選擇。</span><span class="sxs-lookup"><span data-stu-id="1de2e-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="1de2e-119">**PRINTDLG** 結構的某些成員是全域記憶體物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1de2e-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="1de2e-120">[列印範例程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))會將全域記憶體物件的資料複製到程式管理的記憶體區塊，並將其他欄位從 **PRINTDLG** 結構複製到程式所定義之資料結構中的欄位。</span><span class="sxs-lookup"><span data-stu-id="1de2e-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="1de2e-121">將 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構中的資料儲存在程式的資料結構之後，您可以開啟 [列印進度] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1de2e-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="1de2e-122">[列印進度] 對話方塊程式可處理對話方塊訊息，並開始列印處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="1de2e-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="1de2e-123">下列程式碼範例示範如何將資料從 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構複製到程式的資料結構，以及如何啟動列印工作。</span><span class="sxs-lookup"><span data-stu-id="1de2e-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  <span data-ttu-id="1de2e-124">如果使用者按一下 [**列印** 一般] 對話方塊中的 [**取消**] 按鈕，就不會執行進一步的處理。</span><span class="sxs-lookup"><span data-stu-id="1de2e-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
