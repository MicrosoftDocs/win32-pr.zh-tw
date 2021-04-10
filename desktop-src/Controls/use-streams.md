---
title: 如何使用資料流程
description: 您可以使用資料流程將資料傳入或傳出 rich edit 控制項。 資料流是由 EDITSTREAM 結構所定義，其中指定緩衝區和應用程式定義的回呼函式。
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104092603"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="babe1-104">如何使用資料流程</span><span class="sxs-lookup"><span data-stu-id="babe1-104">How to Use Streams</span></span>

<span data-ttu-id="babe1-105">您可以使用資料流程將資料傳入或傳出 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="babe1-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="babe1-106">資料流程是由 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) 結構所定義，它會指定緩衝區和應用程式定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="babe1-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="babe1-107">若要將資料讀入 rich edit 控制項 (也就是在資料) 中串流，請使用 [**EM \_ STREAMIN**](em-streamin.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="babe1-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="babe1-108">控制項會不斷地呼叫應用程式的回呼函式，每次都會將部分資料傳送到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="babe1-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="babe1-109">若要儲存 rich edit 控制項的內容 (也就是串流出資料) ，您可以使用 [**EM \_ STREAMOUT**](em-streamout.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="babe1-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="babe1-110">控制項會重複寫入緩衝區，然後呼叫應用程式的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="babe1-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="babe1-111">回呼函式會在每次呼叫時儲存緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="babe1-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="babe1-112">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="babe1-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="babe1-113">技術</span><span class="sxs-lookup"><span data-stu-id="babe1-113">Technologies</span></span>

-   [<span data-ttu-id="babe1-114">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="babe1-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="babe1-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="babe1-115">Prerequisites</span></span>

-   <span data-ttu-id="babe1-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="babe1-116">C/C++</span></span>
-   <span data-ttu-id="babe1-117">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="babe1-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="babe1-118">指示</span><span class="sxs-lookup"><span data-stu-id="babe1-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="babe1-119">使用資料流程</span><span class="sxs-lookup"><span data-stu-id="babe1-119">Use a Stream</span></span>

<span data-ttu-id="babe1-120">下列程式碼範例會示範如何將 .rtf 檔案讀取至 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="babe1-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="babe1-121">檔案控制代碼會透過 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **dwCookie** 成員傳遞至回呼函數。</span><span class="sxs-lookup"><span data-stu-id="babe1-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="babe1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="babe1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="babe1-123">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="babe1-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="babe1-124">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="babe1-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




