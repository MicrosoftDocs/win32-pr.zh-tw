---
description: 本節說明如何執行與視窗屬性相關聯的下列工作。
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: 使用視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988814"
---
# <a name="using-window-properties"></a><span data-ttu-id="41d29-103">使用視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-103">Using Window Properties</span></span>

<span data-ttu-id="41d29-104">本節說明如何執行與視窗屬性相關聯的下列工作。</span><span class="sxs-lookup"><span data-stu-id="41d29-104">This section explains how to perform the following tasks associated with window properties.</span></span>

-   [<span data-ttu-id="41d29-105">新增視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-105">Adding a Window Property</span></span>](#adding-a-window-property)
-   [<span data-ttu-id="41d29-106">正在抓取視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-106">Retrieving a Window Property</span></span>](#retrieving-a-window-property)
-   [<span data-ttu-id="41d29-107">列出指定視窗的視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-107">Listing Window Properties for a Given Window</span></span>](#listing-window-properties-for-a-given-window)
-   [<span data-ttu-id="41d29-108">刪除視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-108">Deleting a Window Property</span></span>](#deleting-a-window-property)

## <a name="adding-a-window-property"></a><span data-ttu-id="41d29-109">新增視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-109">Adding a Window Property</span></span>

<span data-ttu-id="41d29-110">下列範例會載入圖示，然後載入資料指標，並為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="41d29-110">The following example loads an icon and then a cursor and allocates memory for a buffer.</span></span> <span data-ttu-id="41d29-111">然後，此範例會使用 [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) 函式，將產生的圖示、游標和記憶體控制碼指派為應用程式定義 hwndSubclass 變數所識別之視窗的視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="41d29-111">The example then uses the [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) function to assign the resulting icon, cursor, and memory handles as window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="41d29-112">這些屬性是由字串屬性 \_ 圖示、屬性資料 \_ 指標和屬性緩衝區來識別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="41d29-112">The properties are identified by the strings PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span>


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



## <a name="retrieving-a-window-property"></a><span data-ttu-id="41d29-113">正在抓取視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-113">Retrieving a Window Property</span></span>

<span data-ttu-id="41d29-114">視窗可以建立其視窗屬性資料的控制碼，並將資料用於任何用途。</span><span class="sxs-lookup"><span data-stu-id="41d29-114">A window can create handles to its window property data and use the data for any purpose.</span></span> <span data-ttu-id="41d29-115">下列範例會使用 [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) 來取得由屬性 \_ 圖示、屬性資料指標和屬性緩衝區所識別之視窗屬性的控制碼 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="41d29-115">The following example uses [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) to obtain handles to the window properties identified by PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span> <span data-ttu-id="41d29-116">然後，此範例會在視窗的工作區中顯示新取得的記憶體緩衝區、游標和圖示的內容。</span><span class="sxs-lookup"><span data-stu-id="41d29-116">The example then displays the contents of the newly obtained memory buffer, cursor, and icon in the window's client area.</span></span>


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



## <a name="listing-window-properties-for-a-given-window"></a><span data-ttu-id="41d29-117">列出指定視窗的視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-117">Listing Window Properties for a Given Window</span></span>

<span data-ttu-id="41d29-118">在下列範例中， [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 函式會列出應用程式定義的 hwndSubclass 變數所識別之視窗視窗屬性的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="41d29-118">In the following example, the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function lists the string identifiers of the window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="41d29-119">此函式依賴應用程式定義的回呼函式 WinPropProc，在視窗的工作區中顯示字串。</span><span class="sxs-lookup"><span data-stu-id="41d29-119">This function relies on the application-defined callback function WinPropProc to display the strings in the window's client area.</span></span>


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



## <a name="deleting-a-window-property"></a><span data-ttu-id="41d29-120">刪除視窗屬性</span><span class="sxs-lookup"><span data-stu-id="41d29-120">Deleting a Window Property</span></span>

<span data-ttu-id="41d29-121">當視窗損毀時，它必須終結它所設定的任何視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="41d29-121">When a window is destroyed, it must destroy any window properties it set.</span></span> <span data-ttu-id="41d29-122">下列範例會使用 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 函式和應用程式定義的回呼函式 DelPropProc 來終結與應用程式定義的 hwndSubclass 變數所識別之視窗相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="41d29-122">The following example uses the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function and the application-defined callback function DelPropProc to destroy the properties associated with the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="41d29-123">也會顯示使用 [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) 函式的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="41d29-123">The callback function, which uses the [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) function, is also shown.</span></span>


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



 

 
