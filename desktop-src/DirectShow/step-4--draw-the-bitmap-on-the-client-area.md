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
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="b3173-103">步驟4：在工作區上繪製點陣圖</span><span class="sxs-lookup"><span data-stu-id="b3173-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="b3173-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b3173-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b3173-105">本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟4。</span><span class="sxs-lookup"><span data-stu-id="b3173-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="b3173-106">最後一個步驟是使用 [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) 函式，在應用程式視窗的工作區上繪製點陣圖。</span><span class="sxs-lookup"><span data-stu-id="b3173-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="b3173-107">此範例只會在工作區的左上角繪製點陣圖，而不考慮視窗大小：</span><span class="sxs-lookup"><span data-stu-id="b3173-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


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



<span data-ttu-id="b3173-108">*PBuffer* 和 *pbmi* 變數是在 [步驟1：建立 Windows Framework](step-1--create-the-windows-framework.md)中宣告，而它們的值是在 [步驟3：執行 Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)函式中取得。</span><span class="sxs-lookup"><span data-stu-id="b3173-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3173-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3173-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3173-110">抓取海報框架</span><span class="sxs-lookup"><span data-stu-id="b3173-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
