---
title: 顯示對話方塊以設定影片特性
description: 顯示對話方塊以設定影片特性
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS 結構
- capDriverGetCaps 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eea12d69a3d23b0345bee3495d32cbb1ad0ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840700"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a><span data-ttu-id="815fd-105">顯示對話方塊以設定影片特性</span><span class="sxs-lookup"><span data-stu-id="815fd-105">Displaying Dialog Boxes to Set Video Characteristics</span></span>

<span data-ttu-id="815fd-106">每個 capture 驅動程式最多可提供三個不同的對話方塊，用來控制影片數位化和捕捉流程的各個層面。</span><span class="sxs-lookup"><span data-stu-id="815fd-106">Each capture driver can provide up to three different dialog boxes used to control aspects of the video digitization and capture process.</span></span> <span data-ttu-id="815fd-107">下列範例示範如何顯示這些對話方塊。</span><span class="sxs-lookup"><span data-stu-id="815fd-107">The following example demonstrates how to display these dialog boxes.</span></span> <span data-ttu-id="815fd-108">在顯示每個對話方塊之前，此範例會呼叫 [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏，並檢查傳回的 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) 結構，以查看捕獲驅動程式是否可以顯示該結構。</span><span class="sxs-lookup"><span data-stu-id="815fd-108">Before displaying each dialog box, the example calls the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro and checks the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure returned to see if the capture driver can display it.</span></span>


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a><span data-ttu-id="815fd-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="815fd-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="815fd-110">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="815fd-110">Using Video Capture</span></span>](using-video-capture.md)
</dt> <dt>

[<span data-ttu-id="815fd-111">**capDriverGetCaps**</span><span class="sxs-lookup"><span data-stu-id="815fd-111">**capDriverGetCaps**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




