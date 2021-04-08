---
title: 將 CD 翻錄
description: 將 CD 翻錄
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，關於
- 翻錄 Cd、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840456"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="f1c94-112">將 CD 翻錄</span><span class="sxs-lookup"><span data-stu-id="f1c94-112">Ripping a CD</span></span>

<span data-ttu-id="f1c94-113">有兩種方式可以使用 Windows Media Player 控制項來燒錄 CD。</span><span class="sxs-lookup"><span data-stu-id="f1c94-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="f1c94-114">Windows Media Player 9 可以使用 **IWMPPlayerServices：： setTaskPane** 來燒錄 cd。</span><span class="sxs-lookup"><span data-stu-id="f1c94-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="f1c94-115">Windows Media Player 11 引進 **IWMPCdromRip** 介面來將 cd 翻錄。</span><span class="sxs-lookup"><span data-stu-id="f1c94-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="f1c94-116">此介面提供的功能比 **IWMPPlayerServices：： setTaskPane** 還多，建議您使用 **IWMPCdromRip** （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f1c94-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="f1c94-117">下列各節說明如何使用 Windows Media Player 來翻錄 CD。</span><span class="sxs-lookup"><span data-stu-id="f1c94-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="f1c94-118">使用 IWMPCdromRip 介面進行翻錄</span><span class="sxs-lookup"><span data-stu-id="f1c94-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="f1c94-119">使用 IWMPPlayerServices：： setTaskPane 進行翻錄</span><span class="sxs-lookup"><span data-stu-id="f1c94-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="f1c94-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1c94-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c94-121">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="f1c94-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




