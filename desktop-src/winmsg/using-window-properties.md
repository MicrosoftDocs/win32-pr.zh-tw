---
description: 本節說明如何執行與視窗屬性相關聯的下列工作。
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: 使用視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fcb4cb0346554ee2df5c1b2fc92df7675cd61d11799b891156b13f26fb213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028266"
---
# <a name="using-window-properties"></a>使用視窗屬性

本節說明如何執行與視窗屬性相關聯的下列工作。

-   [新增視窗屬性](#adding-a-window-property)
-   [正在抓取視窗屬性](#retrieving-a-window-property)
-   [列出指定視窗的視窗屬性](#listing-window-properties-for-a-given-window)
-   [刪除視窗屬性](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>新增視窗屬性

下列範例會載入圖示，然後載入資料指標，並為緩衝區配置記憶體。 然後，此範例會使用 [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) 函式，將產生的圖示、游標和記憶體控制碼指派為應用程式定義 hwndSubclass 變數所識別之視窗的視窗屬性。 這些屬性是由字串屬性 \_ 圖示、屬性資料 \_ 指標和屬性緩衝區來識別 \_ 。


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>正在抓取視窗屬性

視窗可以建立其視窗屬性資料的控制碼，並將資料用於任何用途。 下列範例會使用 [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) 來取得由屬性 \_ 圖示、屬性資料指標和屬性緩衝區所識別之視窗屬性的控制碼 \_ \_ 。 然後，此範例會在視窗的工作區中顯示新取得的記憶體緩衝區、游標和圖示的內容。


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>列出指定視窗的視窗屬性

在下列範例中， [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 函式會列出應用程式定義的 hwndSubclass 變數所識別之視窗視窗屬性的字串識別碼。 此函式依賴應用程式定義的回呼函式 WinPropProc，在視窗的工作區中顯示字串。


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>刪除視窗屬性

當視窗損毀時，它必須終結它所設定的任何視窗屬性。 下列範例會使用 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 函式和應用程式定義的回呼函式 DelPropProc 來終結與應用程式定義的 hwndSubclass 變數所識別之視窗相關聯的屬性。 也會顯示使用 [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) 函式的回呼函數。


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
