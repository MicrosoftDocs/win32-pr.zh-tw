---
description: 步驟1：建立 Windows Framework
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 步驟1：建立 Windows Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975167"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="e808b-103">步驟1：建立 Windows Framework</span><span class="sxs-lookup"><span data-stu-id="e808b-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="e808b-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e808b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e808b-105">首先，建立 Windows 應用程式的基本架構，包括 WinMain 和視窗程式。</span><span class="sxs-lookup"><span data-stu-id="e808b-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="e808b-106">WinMain 函式不會顯示于此處;在訊息迴圈之前呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫，並在訊息迴圈結束後 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。</span><span class="sxs-lookup"><span data-stu-id="e808b-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="e808b-107">從下列最基本的視窗程式開始：</span><span class="sxs-lookup"><span data-stu-id="e808b-107">Start with the following minimal window procedure:</span></span>


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



<span data-ttu-id="e808b-108">當您從媒體偵測器取出海報框架時，它會傳回一個緩衝區，其中包含 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，後面接著影像位。</span><span class="sxs-lookup"><span data-stu-id="e808b-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="e808b-109">因此，請在視窗程式中定義兩個靜態變數： *pbmi* 會保留 **BITMAPINFOHEADER** 結構的指標，而 *pBuffer* 會保存點陣圖的指標。</span><span class="sxs-lookup"><span data-stu-id="e808b-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="e808b-110">應用程式會使用在 *pbmi* 中配置緩衝區 `new` ，因此它必須在終結視窗之前先刪除緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e808b-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="e808b-111">*PBuffer* 指標會計算為 *pbmi* 的位移，所以不需要將它刪除。</span><span class="sxs-lookup"><span data-stu-id="e808b-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="e808b-112">下一 [步：步驟2：加入功能表命令以抓取海報畫面](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="e808b-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e808b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e808b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e808b-114">抓取海報框架</span><span class="sxs-lookup"><span data-stu-id="e808b-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
