---
description: VMR 篩選元件
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: VMR 篩選元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513668"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="e7abd-103">VMR 篩選元件</span><span class="sxs-lookup"><span data-stu-id="e7abd-103">VMR Filter Components</span></span>

<span data-ttu-id="e7abd-104">VMR 採用模組化設計，可讓應用程式針對許多不同的轉譯案例進行設定。</span><span class="sxs-lookup"><span data-stu-id="e7abd-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="e7abd-105">根據其設定，除了) 的輸入圖釘之外，VMR 還包含二到五個子元件 (。</span><span class="sxs-lookup"><span data-stu-id="e7abd-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![具有多個資料流程的視窗模式 vmr](images/vmr-multiple-streams.png)

<span data-ttu-id="e7abd-107">**混音器：** 混音器是負責混合多個資料流程的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e7abd-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="e7abd-108">去交錯也會出現在混音器內。</span><span class="sxs-lookup"><span data-stu-id="e7abd-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="e7abd-109">當偵測到多個輸入資料流程時，或當輸入影片交錯時，VMR 會載入混音器。</span><span class="sxs-lookup"><span data-stu-id="e7abd-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="e7abd-110">此混音器會收集每個輸入資料流程的相關資訊，並將資料流程排序成正確的 Z 順序。</span><span class="sxs-lookup"><span data-stu-id="e7abd-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="e7abd-111">它負責判斷每個輸入 pin 何時收到範例，並在適當的時間指示影像組合器執行實際的混合。</span><span class="sxs-lookup"><span data-stu-id="e7abd-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="e7abd-112">混音器也會計算要套用至每個輸出影像的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e7abd-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="e7abd-113">當應用程式提供要顯示在複合影像上方的點陣圖時，混音器會負責確保即使在輸入資料流程的迭置順序已修改的情況下，點陣圖也會顯示在頂端。</span><span class="sxs-lookup"><span data-stu-id="e7abd-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="e7abd-114">**影像組合器：** 影像組合器是一種 COM 物件，它會執行輸入資料流程的實際混合，以在配置器提供者所提供的單一 DirectDraw 或 Direct3D 介面上執行。</span><span class="sxs-lookup"><span data-stu-id="e7abd-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="e7abd-115">VMR 會提供預設的影像組合器，可讓應用程式執行立體的 Alpha 混色效果。</span><span class="sxs-lookup"><span data-stu-id="e7abd-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="e7abd-116">應用程式可以提供自訂影像組合器來啟用其他的立體和3-d 效果，例如將材質套用至影像的部分、每圖元的 Alpha 混色、將影像對應至固定或移動立體物件等等。</span><span class="sxs-lookup"><span data-stu-id="e7abd-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="e7abd-117">配置器 **-展示者：** 配置器-展示者是一種 COM 物件，它會配置 DirectDraw 或 Direct3D 物件，並處理與圖形配接器的通訊。</span><span class="sxs-lookup"><span data-stu-id="e7abd-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="e7abd-118">繪圖可作為翻轉或 array.blit 執行。</span><span class="sxs-lookup"><span data-stu-id="e7abd-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="e7abd-119">您可以插入自己的配置器-展示器，以便建立及控制 DirectDraw 或 Direct3D 物件，以及/或在簡報時取得影片位的存取權。</span><span class="sxs-lookup"><span data-stu-id="e7abd-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="e7abd-120">**視窗管理員：** 視窗管理員只會在視窗模式中使用。</span><span class="sxs-lookup"><span data-stu-id="e7abd-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="e7abd-121">視窗管理員支援舊版 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 和 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="e7abd-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7abd-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7abd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7abd-123">關於影片混合轉譯</span><span class="sxs-lookup"><span data-stu-id="e7abd-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



