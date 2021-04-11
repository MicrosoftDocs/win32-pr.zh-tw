---
description: 'VMR Renderless 播放模式 (自訂配置器-展示者) '
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: 'VMR Renderless 播放模式 (自訂配置器-展示者) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693752"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="988d1-103">VMR Renderless 播放模式 (自訂配置器-展示者) </span><span class="sxs-lookup"><span data-stu-id="988d1-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="988d1-104">在 renderless 播放模式中，VMR 不會執行轉譯。</span><span class="sxs-lookup"><span data-stu-id="988d1-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="988d1-105">相反地，它會使用應用程式所提供的自訂配置器提供者。</span><span class="sxs-lookup"><span data-stu-id="988d1-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="988d1-106">這種模式適用于具有複雜影片效果的遊戲和其他類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="988d1-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="988d1-107">Renderless 播放模式可讓應用程式建立和控制自己的 DirectDraw 介面 (VMR-7) 或 Direct3D 介面 (VMR 9) ，以及在簡報時存取影片位。</span><span class="sxs-lookup"><span data-stu-id="988d1-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="988d1-108">在 renderless 模式中，VMR-9 不會自動載入其混音器元件。</span><span class="sxs-lookup"><span data-stu-id="988d1-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="988d1-109">在 renderless 播放模式中，應用程式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="988d1-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="988d1-110">管理播放視窗。</span><span class="sxs-lookup"><span data-stu-id="988d1-110">Manages the playback window.</span></span>
-   <span data-ttu-id="988d1-111">配置 DirectDraw 或 Direct3D 物件和最終的框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="988d1-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="988d1-112">通知所使用物件的其餘播放系統。</span><span class="sxs-lookup"><span data-stu-id="988d1-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="988d1-113">提供正確時間的框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="988d1-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="988d1-114">處理所有解決模式變更、監視變更和介面遺失。</span><span class="sxs-lookup"><span data-stu-id="988d1-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="988d1-115">它必須建議這些事件的其餘播放系統。</span><span class="sxs-lookup"><span data-stu-id="988d1-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="988d1-116">VMR 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="988d1-116">The VMR does the following:</span></span>

-   <span data-ttu-id="988d1-117">處理與呈現影片框架相關的所有時間。</span><span class="sxs-lookup"><span data-stu-id="988d1-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="988d1-118">提供品質控制資訊給應用程式和其餘的播放系統。</span><span class="sxs-lookup"><span data-stu-id="988d1-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="988d1-119">為播放系統的上游元件提供一致的介面，這並不知道應用程式是否提供框架緩衝區配置和執行轉譯。</span><span class="sxs-lookup"><span data-stu-id="988d1-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="988d1-120">提供轉譯之前可能需要的任何影片資料流程混合。</span><span class="sxs-lookup"><span data-stu-id="988d1-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="988d1-121">由於去交錯是由混音器所執行，因此配置器呈現者一律會收到 deinterlaced 的畫面格。</span><span class="sxs-lookup"><span data-stu-id="988d1-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="988d1-122">如需詳細資訊，請參閱 [設定隔行掃描喜好設定](setting-deinterlace-preferences.md)。</span><span class="sxs-lookup"><span data-stu-id="988d1-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="988d1-123">如需提供自訂配置器-展示者的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="988d1-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="988d1-124">提供 VMR-7 的自訂 Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="988d1-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="988d1-125">提供 VMR-9 的自訂 Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="988d1-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="988d1-126">將 VMR 同步處理至監視器的更新速率</span><span class="sxs-lookup"><span data-stu-id="988d1-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



