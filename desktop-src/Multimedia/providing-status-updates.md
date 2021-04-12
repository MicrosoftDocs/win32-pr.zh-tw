---
title: 提供狀態更新
description: 提供狀態更新
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer 宏
- MCIWndSetInactiveTimer 宏
- MCIWndGetActiveTimer 宏
- MCIWndGetInactiveTimer 宏
- MCIWndSetTimers 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372111"
---
# <a name="providing-status-updates"></a><span data-ttu-id="f5b3d-108">提供狀態更新</span><span class="sxs-lookup"><span data-stu-id="f5b3d-108">Providing Status Updates</span></span>

<span data-ttu-id="f5b3d-109">MCIWnd 會使用計時器，定期更新視窗標題列和捲軸中的資訊，並將通知訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="f5b3d-110">其中一個計時器控制作用中 MCIWnd 視窗的更新期間，而第二個計時器則控制非使用中 MCIWnd 視窗的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="f5b3d-111">您的應用程式可以使用 MCIWnd 計時器宏來取出目前的計時器設定，並調整更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="f5b3d-112">您可以使用 [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) 宏來設定使用中視窗計時器所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="f5b3d-113">此宏會設定 MCIWnd 用來更新提要欄位的期間，以更新視窗標題列中所報告的播放位置，以及通知父視窗該媒體已變更。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="f5b3d-114">您可以使用 [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) 宏來取得使用中視窗計時器目前使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="f5b3d-115">使用中視窗計時器的預設更新期間是500毫秒。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="f5b3d-116">您可以使用 [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) 宏來設定非作用中視窗計時器所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="f5b3d-117">此宏會設定 MCIWnd 用來更新標題的期間，以更新在視窗標題中報告的播放位置，以及通知父視窗該媒體已變更。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="f5b3d-118">您可以使用 [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) 宏來取出非使用中視窗計時器目前使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="f5b3d-119">非作用中視窗計時器的預設更新期間是2000毫秒。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="f5b3d-120">您的應用程式可以使用 [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) 宏同時設定這兩個計時器的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="f5b3d-121">更新週期值的儲存體限制為16位。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="f5b3d-122">如果需要更新期間的較大數量，請個別設定計時器。</span><span class="sxs-lookup"><span data-stu-id="f5b3d-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




