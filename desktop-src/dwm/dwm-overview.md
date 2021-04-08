---
title: 桌面視窗管理員
description: Windows Vista 引進的桌面撰寫功能，基本上改變了應用程式在螢幕上顯示圖元的方式。
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- 桌面視窗管理員 (DWM) ，關於
- DWM (桌面視窗管理員) ，關於
- 桌面視窗管理員 (DWM) ，組合
- DWM (桌面視窗管理員) ，組合
- 桌面電腦群組合
- 組合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673660"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="3aa36-109">桌面視窗管理員</span><span class="sxs-lookup"><span data-stu-id="3aa36-109">Desktop Window Manager</span></span>

<span data-ttu-id="3aa36-110">Windows Vista 引進的桌面撰寫功能，基本上改變了應用程式在螢幕上顯示圖元的方式。</span><span class="sxs-lookup"><span data-stu-id="3aa36-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="3aa36-111">啟用桌面電腦群組合時，個別的 windows 不再像在舊版 Windows 中一樣直接繪製到螢幕或主要顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="3aa36-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="3aa36-112">相反地，它們的繪圖會重新導向至視訊記憶體中的螢幕表面，然後轉譯成桌面影像並顯示在顯示器上。</span><span class="sxs-lookup"><span data-stu-id="3aa36-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="3aa36-113">桌面電腦群組合是由桌面視窗管理員 (DWM) 所執行。</span><span class="sxs-lookup"><span data-stu-id="3aa36-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="3aa36-114">透過桌面電腦群組合，DWM 可在桌面上啟用視覺效果，以及各種功能，例如半透明視窗框架、立體視窗轉換動畫、Windows Flip 和 Windows Flip3D，以及高解析度支援。</span><span class="sxs-lookup"><span data-stu-id="3aa36-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="3aa36-115">桌面視窗管理員會以 Windows 服務的形式執行。</span><span class="sxs-lookup"><span data-stu-id="3aa36-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="3aa36-116">您可以在 [服務] 下的 [系統管理工具] 主控台專案中啟用和停用，如桌面視窗管理員會話管理員。</span><span class="sxs-lookup"><span data-stu-id="3aa36-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="3aa36-117">應用程式可以透過 DWM Api 來控制或存取許多 DWM 功能。</span><span class="sxs-lookup"><span data-stu-id="3aa36-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="3aa36-118">下列檔說明 DWM Api 的功能和需求。</span><span class="sxs-lookup"><span data-stu-id="3aa36-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="3aa36-119">DWM 總覽</span><span class="sxs-lookup"><span data-stu-id="3aa36-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="3aa36-120">DWM 範例程式碼</span><span class="sxs-lookup"><span data-stu-id="3aa36-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="3aa36-121">DWM 參考</span><span class="sxs-lookup"><span data-stu-id="3aa36-121">DWM Reference</span></span>](reference.md)

 

 




