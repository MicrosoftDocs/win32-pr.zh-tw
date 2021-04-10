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
# <a name="how-to-collect-print-job-information-from-the-user"></a>如何：收集使用者的列印工作資訊

本主題說明如何收集使用者的列印工作資訊。

## <a name="overview"></a>概觀

藉由呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數，從使用者收集列印工作資訊。 此函式會將 [ **列印** ] 通用對話方塊顯示給使用者，並傳回 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 資料結構中的列印工作資訊。

當使用者啟動列印工作時，就會顯示 [ **列印** 一般] 對話方塊。 [ **列印** 通用] 對話方塊是強制回應對話方塊，這表示使用者在一般對話方塊關閉之前，無法與主視窗互動。

## <a name="collecting-print-job-information"></a>收集列印工作資訊

1.  初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構元素。

    在程式可以顯示 [ **列印** 一般] 對話方塊之前，它必須配置並初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構。 然後，它會將此結構傳遞至 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式，此函式會顯示對話方塊，並傳回相同結構中的列印工作資料。 下列程式碼範例會示範範例程式如何執行此步驟。

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

    

2.  顯示 [ **列印** 一般] 對話方塊。

    使用已初始化的 [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構來呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ，以顯示 [**列印** 一般] 對話方塊並收集使用者資料，如下列程式碼範例所示。

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  儲存 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構中的欄位，並啟動列印工作。

    [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構包含的資料會描述使用者在 [列印] 對話方塊中所做的選擇。 **PRINTDLG** 結構的某些成員是全域記憶體物件的控制碼。 [列印範例程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))會將全域記憶體物件的資料複製到程式管理的記憶體區塊，並將其他欄位從 **PRINTDLG** 結構複製到程式所定義之資料結構中的欄位。

    將 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構中的資料儲存在程式的資料結構之後，您可以開啟 [列印進度] 對話方塊。 [列印進度] 對話方塊程式可處理對話方塊訊息，並開始列印處理執行緒。

    下列程式碼範例示範如何將資料從 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構複製到程式的資料結構，以及如何啟動列印工作。

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

    

4.  如果使用者按一下 [**列印** 一般] 對話方塊中的 [**取消**] 按鈕，就不會執行進一步的處理。

 

 
