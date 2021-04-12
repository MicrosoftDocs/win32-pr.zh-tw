---
title: 如何新增多個監視器的支援
description: DirectWrite 包含多個監視器的系統支援。
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375885"
---
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="c1913-103">如何新增多個監視器的支援</span><span class="sxs-lookup"><span data-stu-id="c1913-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="c1913-104">[DirectWrite](direct-write-portal.md) 包含多個監視器的系統支援。</span><span class="sxs-lookup"><span data-stu-id="c1913-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="c1913-105">不同的監視器可能會有不同的圖元幾何 (RGB、BGR 或平面) 或其他屬性。</span><span class="sxs-lookup"><span data-stu-id="c1913-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="c1913-106">如需圖元幾何的詳細資訊，請參閱 [**DWRITE \_ 圖元 \_ 幾何**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) 參考主題。</span><span class="sxs-lookup"><span data-stu-id="c1913-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="c1913-107">本主題將說明如何將多個監視器的支援新增至您的 DirectWrite 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c1913-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="c1913-108">為了支援多個監視器，您必須處理 **WM \_ WINDOWPOSCHANGED** 視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="c1913-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="c1913-109">此訊息會在移動視窗時傳送，因此您必須檢查視窗是否已移至不同的監視器，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="c1913-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



<span data-ttu-id="c1913-110">如果視窗位於新的監視器上，您就必須使用 [**IDWriteFactory：： CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) 方法來建立新監視器的呈現參數。</span><span class="sxs-lookup"><span data-stu-id="c1913-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="c1913-111">請勿使用 [**IDWriteFactory：： CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) 方法來建立轉譯參數，因為它一律會建立主要監視器的參數。</span><span class="sxs-lookup"><span data-stu-id="c1913-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="c1913-112">當您有 [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) 物件時，請使用 [**ID2DRenderTarget：： SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) 方法設定轉譯目標的轉譯參數。</span><span class="sxs-lookup"><span data-stu-id="c1913-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="c1913-113">最後，使用 [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) 函式，讓視窗以新的轉譯參數重新繪製。</span><span class="sxs-lookup"><span data-stu-id="c1913-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 