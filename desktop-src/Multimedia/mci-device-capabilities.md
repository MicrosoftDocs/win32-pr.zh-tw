---
title: MCI 裝置功能
description: MCI 裝置功能
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig 宏
- MCIWndCanEject 宏
- MCIWndCanPlay 宏
- MCIWndCanRecord 宏
- MCIWndCanSave 宏
- MCIWndCanWindow 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021999"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="c56b0-109">MCI 裝置功能</span><span class="sxs-lookup"><span data-stu-id="c56b0-109">MCI Device Capabilities</span></span>

<span data-ttu-id="c56b0-110">MCIWnd 包含下列宏，可讓您查詢 MCI 裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="c56b0-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="c56b0-111">巨集</span><span class="sxs-lookup"><span data-stu-id="c56b0-111">Macro</span></span>                                      | <span data-ttu-id="c56b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="c56b0-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c56b0-113">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="c56b0-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="c56b0-114">判斷裝置是否具有設定對話方塊，可支援多個設定，例如 MCIAVI 裝置。</span><span class="sxs-lookup"><span data-stu-id="c56b0-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="c56b0-115">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="c56b0-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="c56b0-116">判斷裝置是否有軟體控制的退出功能。</span><span class="sxs-lookup"><span data-stu-id="c56b0-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="c56b0-117">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="c56b0-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="c56b0-118">判斷裝置是否可以播放現有的內容。</span><span class="sxs-lookup"><span data-stu-id="c56b0-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="c56b0-119">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="c56b0-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="c56b0-120">判斷裝置是否可以錄製。</span><span class="sxs-lookup"><span data-stu-id="c56b0-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="c56b0-121">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="c56b0-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="c56b0-122">判斷裝置是否可以儲存資料。</span><span class="sxs-lookup"><span data-stu-id="c56b0-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="c56b0-123">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="c56b0-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="c56b0-124">判斷裝置是否支援 MCI 視窗命令 (例如 [**window**](window.md)、 [**put**](put.md) 和 [**where**](where.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c56b0-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="c56b0-125">如果裝置支援特定功能，這些宏會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c56b0-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




