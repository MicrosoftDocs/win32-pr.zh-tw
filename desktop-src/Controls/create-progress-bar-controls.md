---
title: 如何使用進度列控制項
description: 本主題說明如何使用進度列來指出冗長檔案剖析作業的進度。
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826418"
---
# <a name="how-to-use-progress-bar-controls"></a>如何使用進度列控制項

本主題說明如何使用進度列來指出冗長檔案剖析作業的進度。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-progress-bar-control"></a>建立進度列控制項

下列程式碼範例會建立一個進度列，並將它置於父視窗工作區的底部。 進度列的高度是以捲軸中使用之箭號點陣圖的高度為基礎。 範圍是根據檔案的大小除以2048，這是從檔案讀取的每個資料「區塊」的大小。 此範例也會設定遞增，並將進度列的目前位置前移到剖析每個區塊之後的遞增。


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>備註

您必須確定正確使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函式，以確保應用程式的安全性。 例如，在範例程式碼中，您應該檢查以確定實際上會 `ReadFile` 讀取所有要求的資料。

另請注意， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)的第四個參數（ (LPSECURITY \_ 屬性) **Null**）會設定預設的安全性值。 如果您需要特定的安全性設定，您必須在結構的成員中設定適當的值。 呼叫 **sizeof** 來設定 **LPSECURITY \_ 屬性** 結構的正確大小。

如需詳細資訊，請參閱[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用進度列控制項](using-progress-bar-controls.md)
</dt> <dt>

[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)
</dt> </dl>

 

 