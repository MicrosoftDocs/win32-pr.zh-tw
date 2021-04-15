---
description: 滑鼠游標方法可讓應用程式藉由提供包含影像的介面來指定色彩游標。
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: 使用 (Direct3D 9) 的滑鼠游標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467865"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="8d681-103">使用 (Direct3D 9) 的滑鼠游標</span><span class="sxs-lookup"><span data-stu-id="8d681-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="8d681-104">滑鼠游標方法可讓應用程式藉由提供包含影像的介面來指定色彩游標。</span><span class="sxs-lookup"><span data-stu-id="8d681-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="8d681-105">如果應用程式的畫面播放速率很慢，系統將確保此資料指標會以顯示速率的一半或更高的頻率更新。</span><span class="sxs-lookup"><span data-stu-id="8d681-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="8d681-106">但是，資料指標的更新頻率絕不會比顯示器重新整理速率更頻繁。</span><span class="sxs-lookup"><span data-stu-id="8d681-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="8d681-107">滑鼠游標位置會系結至系統游標，並針對目前的顯示模式空間解析度適當地調整，但應用程式可以明確地移動。</span><span class="sxs-lookup"><span data-stu-id="8d681-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="8d681-108">這與 WIN32 API 支援的系統滑鼠游標的行為類似。</span><span class="sxs-lookup"><span data-stu-id="8d681-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="8d681-109">如需如何在 Direct3D 應用程式中使用滑鼠游標的詳細資訊，請參閱下列參考主題。</span><span class="sxs-lookup"><span data-stu-id="8d681-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="8d681-110">**IDirect3DDevice9::ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="8d681-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="8d681-111">**IDirect3DDevice9::SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="8d681-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="8d681-112">**IDirect3DDevice9::SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="8d681-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="8d681-113">Direct3D 可確保在呼叫 IDirect3DDevice9 時執行硬體加速 blitting 作業的硬體執行或 Direct3D 執行時間支援滑鼠 [**：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送。</span><span class="sxs-lookup"><span data-stu-id="8d681-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d681-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d681-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d681-115">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="8d681-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
