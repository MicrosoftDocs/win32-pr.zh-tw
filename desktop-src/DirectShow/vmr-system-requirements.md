---
description: VMR 系統需求
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR 系統需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193519"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="bda4f-103">VMR 系統需求</span><span class="sxs-lookup"><span data-stu-id="bda4f-103">VMR System Requirements</span></span>

<span data-ttu-id="bda4f-104">VMR 會以獨佔方式使用電腦顯示配接器的圖形處理功能;VMR 不會使用主機處理器來執行任何的影片混色或轉譯，因為這樣做會大幅影響畫面播放速率和所顯示影片的品質。</span><span class="sxs-lookup"><span data-stu-id="bda4f-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="bda4f-105">當您利用 VMR 所提供的新功能時（特別是多個影片串流及/或應用程式影像的混合），所取得的整體效能將高度依賴電腦上所使用之圖形配接器的功能。</span><span class="sxs-lookup"><span data-stu-id="bda4f-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="bda4f-106">與 VMR 搭配運作的圖形配接器，具有下列內建的硬體支援：</span><span class="sxs-lookup"><span data-stu-id="bda4f-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="bda4f-107">支援 YUV 和「非乘2」 Direct3D 材質表面。</span><span class="sxs-lookup"><span data-stu-id="bda4f-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="bda4f-108">從 YUV StretchBlt 至 RGB DirectDraw 表面的能力。</span><span class="sxs-lookup"><span data-stu-id="bda4f-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="bda4f-109">如果有多個影片串流要混合在一起，則至少有16MB 的視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="bda4f-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="bda4f-110">實際所需的記憶體數量取決於影片串流的影像大小，以及所使用的顯示模式解析度。</span><span class="sxs-lookup"><span data-stu-id="bda4f-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="bda4f-111">支援 RGB 重迭或 blend 至 YUV 重迭表面的能力。</span><span class="sxs-lookup"><span data-stu-id="bda4f-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="bda4f-112">硬體加速影片 (支援 DirectX Video 加速) 解碼。</span><span class="sxs-lookup"><span data-stu-id="bda4f-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="bda4f-113">高圖元填滿率。</span><span class="sxs-lookup"><span data-stu-id="bda4f-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="bda4f-114">VMR 要求系統監視器必須設定至少16位的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="bda4f-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="bda4f-115">如果已針對256色彩設定監視，則無法將 VMR 置於執行狀態。</span><span class="sxs-lookup"><span data-stu-id="bda4f-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="bda4f-116">此外，當顯示器設為每圖元24位時，某些視訊卡無法執行 Direct3D 作業。</span><span class="sxs-lookup"><span data-stu-id="bda4f-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bda4f-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="bda4f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda4f-118">關於影片混合轉譯</span><span class="sxs-lookup"><span data-stu-id="bda4f-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



