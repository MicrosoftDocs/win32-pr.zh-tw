---
title: 模組3。 Windows 圖形
description: 本系列的課程模組1顯示如何建立空白視窗。
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021050"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="a3c50-104">模組3。</span><span class="sxs-lookup"><span data-stu-id="a3c50-104">Module 3.</span></span> <span data-ttu-id="a3c50-105">Windows 圖形</span><span class="sxs-lookup"><span data-stu-id="a3c50-105">Windows Graphics</span></span>

<span data-ttu-id="a3c50-106">本系列的[課程模組 1](your-first-windows-program.md)顯示如何建立空白視窗。</span><span class="sxs-lookup"><span data-stu-id="a3c50-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="a3c50-107">[模組 2](module-2--using-com-in-your-windows-program.md) 稍微繞道元件物件模型 (COM) ，這是許多新式 Windows api 的基礎。</span><span class="sxs-lookup"><span data-stu-id="a3c50-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="a3c50-108">現在是時候將圖形新增到我們在課程模組1中建立的空白視窗。</span><span class="sxs-lookup"><span data-stu-id="a3c50-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="a3c50-109">此課程模組從高階的 Windows 圖形架構總覽開始。</span><span class="sxs-lookup"><span data-stu-id="a3c50-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="a3c50-110">然後我們會探討 Direct2D，這是 Windows 7 中引進的強大圖形 API。</span><span class="sxs-lookup"><span data-stu-id="a3c50-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3c50-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="a3c50-111">In this section</span></span>

-   [<span data-ttu-id="a3c50-112">Windows 圖形架構總覽</span><span class="sxs-lookup"><span data-stu-id="a3c50-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="a3c50-113">桌面視窗管理員</span><span class="sxs-lookup"><span data-stu-id="a3c50-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="a3c50-114">保留模式與立即模式</span><span class="sxs-lookup"><span data-stu-id="a3c50-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="a3c50-115">您的第一個 Direct2D 計畫</span><span class="sxs-lookup"><span data-stu-id="a3c50-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="a3c50-116">呈現目標、裝置和資源</span><span class="sxs-lookup"><span data-stu-id="a3c50-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="a3c50-117">使用 Direct2D 繪製</span><span class="sxs-lookup"><span data-stu-id="a3c50-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="a3c50-118">DPI 和 Device-Independent 圖元</span><span class="sxs-lookup"><span data-stu-id="a3c50-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="a3c50-119">在 Direct2D 中使用色彩</span><span class="sxs-lookup"><span data-stu-id="a3c50-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="a3c50-120">在 Direct2D 中套用轉換</span><span class="sxs-lookup"><span data-stu-id="a3c50-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="a3c50-121">附錄：矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="a3c50-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="a3c50-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3c50-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3c50-123">學習如何以 c + + 撰寫 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="a3c50-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 




