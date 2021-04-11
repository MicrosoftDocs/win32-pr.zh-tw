---
description: 步驟2：新增功能表命令以抓取海報畫面
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 步驟2：新增功能表命令以抓取海報畫面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115773"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="777e9-103">步驟2：新增功能表命令以抓取海報畫面</span><span class="sxs-lookup"><span data-stu-id="777e9-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="777e9-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="777e9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="777e9-105">本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟2。</span><span class="sxs-lookup"><span data-stu-id="777e9-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="777e9-106">接下來，新增一個命令，讓使用者從檔案抓取海報框架。</span><span class="sxs-lookup"><span data-stu-id="777e9-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="777e9-107">建立具有 IDM 點陣圖資源識別碼的功能表項目 \_ ，並將下列 case 語句新增至視窗程式：</span><span class="sxs-lookup"><span data-stu-id="777e9-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



<span data-ttu-id="777e9-108">DoShowBitmap 函式會在 *pbmi* 中傳回已配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="777e9-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="777e9-109">假設函式成功，則點陣圖的位址 (</span><span class="sxs-lookup"><span data-stu-id="777e9-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="777e9-110">) 可以計算為 *pbmi* 的位移。</span><span class="sxs-lookup"><span data-stu-id="777e9-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="777e9-111">在 DoShowBitmap 函式中，顯示 [ **開啟** 檔案] 對話方塊供使用者選擇檔案，然後呼叫應用程式定義的 GetBitmap 函式，此函式將會取出點陣圖：</span><span class="sxs-lookup"><span data-stu-id="777e9-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



<span data-ttu-id="777e9-112">下一[步：步驟3：執行 Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)函式</span><span class="sxs-lookup"><span data-stu-id="777e9-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="777e9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="777e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="777e9-114">抓取海報框架</span><span class="sxs-lookup"><span data-stu-id="777e9-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



