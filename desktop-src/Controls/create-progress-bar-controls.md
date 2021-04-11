---
title: 如何使用進度列控制項
description: 本主題說明如何使用進度列來指出冗長檔案剖析作業的進度。
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933665"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="d2148-103">如何使用進度列控制項</span><span class="sxs-lookup"><span data-stu-id="d2148-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="d2148-104">本主題說明如何使用進度列來指出冗長檔案剖析作業的進度。</span><span class="sxs-lookup"><span data-stu-id="d2148-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2148-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d2148-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2148-106">技術</span><span class="sxs-lookup"><span data-stu-id="d2148-106">Technologies</span></span>

-   [<span data-ttu-id="d2148-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d2148-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d2148-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="d2148-108">Prerequisites</span></span>

-   <span data-ttu-id="d2148-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2148-109">C/C++</span></span>
-   <span data-ttu-id="d2148-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d2148-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d2148-111">指示</span><span class="sxs-lookup"><span data-stu-id="d2148-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="d2148-112">建立進度列控制項</span><span class="sxs-lookup"><span data-stu-id="d2148-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="d2148-113">下列程式碼範例會建立一個進度列，並將它置於父視窗工作區的底部。</span><span class="sxs-lookup"><span data-stu-id="d2148-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="d2148-114">進度列的高度是以捲軸中使用之箭號點陣圖的高度為基礎。</span><span class="sxs-lookup"><span data-stu-id="d2148-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="d2148-115">範圍是根據檔案的大小除以2048，這是從檔案讀取的每個資料「區塊」的大小。</span><span class="sxs-lookup"><span data-stu-id="d2148-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="d2148-116">此範例也會設定遞增，並將進度列的目前位置前移到剖析每個區塊之後的遞增。</span><span class="sxs-lookup"><span data-stu-id="d2148-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="d2148-117">備註</span><span class="sxs-lookup"><span data-stu-id="d2148-117">Remarks</span></span>

<span data-ttu-id="d2148-118">您必須確定正確使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函式，以確保應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="d2148-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="d2148-119">例如，在範例程式碼中，您應該檢查以確定實際上會 `ReadFile` 讀取所有要求的資料。</span><span class="sxs-lookup"><span data-stu-id="d2148-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="d2148-120">另請注意， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)的第四個參數（ (LPSECURITY \_ 屬性) **Null**）會設定預設的安全性值。</span><span class="sxs-lookup"><span data-stu-id="d2148-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="d2148-121">如果您需要特定的安全性設定，您必須在結構的成員中設定適當的值。</span><span class="sxs-lookup"><span data-stu-id="d2148-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="d2148-122">呼叫 **sizeof** 來設定 **LPSECURITY \_ 屬性** 結構的正確大小。</span><span class="sxs-lookup"><span data-stu-id="d2148-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="d2148-123">如需詳細資訊，請參閱 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md)。</span><span class="sxs-lookup"><span data-stu-id="d2148-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2148-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2148-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2148-125">使用進度列控制項</span><span class="sxs-lookup"><span data-stu-id="d2148-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="d2148-126">安全性考慮： Microsoft Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d2148-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 