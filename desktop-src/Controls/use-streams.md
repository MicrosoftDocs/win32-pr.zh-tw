---
title: 如何使用資料流程
description: 您可以使用資料流程將資料傳入或傳出 rich edit 控制項。 資料流是由 EDITSTREAM 結構所定義，其中指定緩衝區和應用程式定義的回呼函式。
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae620d123ad983cd150bf78d27d99de137ec61eea8c5a32c9fcc9698cb262a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828620"
---
# <a name="how-to-use-streams"></a>如何使用資料流程

您可以使用資料流程將資料傳入或傳出 rich edit 控制項。 資料流程是由 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) 結構所定義，它會指定緩衝區和應用程式定義的回呼函數。

若要將資料讀入 rich edit 控制項 (也就是在資料) 中串流，請使用 [**EM \_ STREAMIN**](em-streamin.md) 訊息。 控制項會不斷地呼叫應用程式的回呼函式，每次都會將部分資料傳送到緩衝區。

若要儲存 rich edit 控制項的內容 (也就是串流出資料) ，您可以使用 [**EM \_ STREAMOUT**](em-streamout.md) 訊息。 控制項會重複寫入緩衝區，然後呼叫應用程式的回呼函數。 回呼函式會在每次呼叫時儲存緩衝區的內容。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-stream"></a>使用資料流程

下列程式碼範例會示範如何將 .rtf 檔案讀取至 rich edit 控制項。 檔案控制代碼會透過 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **dwCookie** 成員傳遞至回呼函數。


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




