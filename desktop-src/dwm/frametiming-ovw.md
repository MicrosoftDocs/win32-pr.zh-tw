---
title: 存取及控制 DWM 框架資料
description: 本主題討論用於排程和媒體簡報的桌面視窗管理員 (DWM) Api。
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- 桌面視窗管理員 (DWM) 、排程和媒體呈現 Api
- DWM (桌面視窗管理員) 、排程和媒體呈現 Api
- 排程和媒體簡報 Api
- 桌面視窗管理員 (DWM) ，存取畫面格資料
- DWM (桌面視窗管理員) ，存取畫面格資料
- 存取畫面格資料
- 桌面視窗管理員 (DWM) ，控制框架資料
- DWM (桌面視窗管理員) ，控制框架資料
- 控制框架資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301019"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="c856b-112">存取及控制 DWM 框架資料</span><span class="sxs-lookup"><span data-stu-id="c856b-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="c856b-113">本主題討論用於排程和媒體簡報的桌面視窗管理員 (DWM) Api。</span><span class="sxs-lookup"><span data-stu-id="c856b-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="c856b-114">DWM 框架計時 API</span><span class="sxs-lookup"><span data-stu-id="c856b-114">DWM Frame Timing API</span></span>

<span data-ttu-id="c856b-115">排程和媒體呈現 Api 可讓您更詳細地控制桌面映射的組成和呈現時間。</span><span class="sxs-lookup"><span data-stu-id="c856b-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="c856b-116">這通常是針對 DWM 以其本身的呈現排程以非同步方式執行的媒體和影片播放應用程式所需要，如果未受到嚴格控制，則可能會導致取樣構件。</span><span class="sxs-lookup"><span data-stu-id="c856b-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="c856b-117">排程和媒體展示功能包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="c856b-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="c856b-118">在這些頁面上可以找到其使用的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c856b-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="c856b-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss)。</span><span class="sxs-lookup"><span data-stu-id="c856b-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="c856b-120">通知 DWM 在呼叫進程保持運作時，啟用多媒體類別排程服務 (MMCSS) 排程。</span><span class="sxs-lookup"><span data-stu-id="c856b-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="c856b-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo)。</span><span class="sxs-lookup"><span data-stu-id="c856b-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="c856b-122">抓取目前的組合計時資訊。</span><span class="sxs-lookup"><span data-stu-id="c856b-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="c856b-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration)。</span><span class="sxs-lookup"><span data-stu-id="c856b-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="c856b-124">變更將顯示上一個畫面格的重新整理次數。</span><span class="sxs-lookup"><span data-stu-id="c856b-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="c856b-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration)。</span><span class="sxs-lookup"><span data-stu-id="c856b-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="c856b-126">設定要在其中顯示所呈現畫面格的重新整理次數。</span><span class="sxs-lookup"><span data-stu-id="c856b-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="c856b-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters)。</span><span class="sxs-lookup"><span data-stu-id="c856b-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="c856b-128">設定框架組合的目前參數。</span><span class="sxs-lookup"><span data-stu-id="c856b-128">Sets the present parameters for frame composition.</span></span>

 

 




