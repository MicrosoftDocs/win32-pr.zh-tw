---
description: 步驟4：在工作區上繪製點陣圖
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 步驟4：在工作區上繪製點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386302"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>步驟4：在工作區上繪製點陣圖

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟4。

最後一個步驟是使用 [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) 函式，在應用程式視窗的工作區上繪製點陣圖。 此範例只會在工作區的左上角繪製點陣圖，而不考慮視窗大小：


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



*PBuffer* 和 *pbmi* 變數是在 [步驟1：建立 Windows Framework](step-1--create-the-windows-framework.md)中宣告，而它們的值是在 [步驟3：執行 Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)函式中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[抓取海報框架](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
