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
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>步驟2：新增功能表命令以抓取海報畫面

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟2。

接下來，新增一個命令，讓使用者從檔案抓取海報框架。 建立具有 IDM 點陣圖資源識別碼的功能表項目 \_ ，並將下列 case 語句新增至視窗程式：


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



DoShowBitmap 函式會在 *pbmi* 中傳回已配置的緩衝區。 假設函式成功，則點陣圖的位址 (


```C++
pBuffer
```



) 可以計算為 *pbmi* 的位移。 在 DoShowBitmap 函式中，顯示 [ **開啟** 檔案] 對話方塊供使用者選擇檔案，然後呼叫應用程式定義的 GetBitmap 函式，此函式將會取出點陣圖：


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



下一[步：步驟3：執行 Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)函式

## <a name="related-topics"></a>相關主題

<dl> <dt>

[抓取海報框架](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



