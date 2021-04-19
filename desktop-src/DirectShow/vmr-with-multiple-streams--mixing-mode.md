---
description: '具有多個資料流程 (混合模式的 VMR) '
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: '具有多個資料流程 (混合模式的 VMR) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984587"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a><span data-ttu-id="25d2f-103">具有多個資料流程 (混合模式的 VMR) </span><span class="sxs-lookup"><span data-stu-id="25d2f-103">VMR with Multiple Streams (Mixing Mode)</span></span>

<span data-ttu-id="25d2f-104">VMR 可以呈現多個輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="25d2f-104">The VMR can render multiple input streams.</span></span> <span data-ttu-id="25d2f-105">在此設定中，稱為混合模式，VMR 會載入其混音器和組合器，以在轉譯之前執行混合和混合。</span><span class="sxs-lookup"><span data-stu-id="25d2f-105">In this configuration, called mixing mode, the VMR loads its mixer and compositor to perform the mixing and blending prior to rendering.</span></span> <span data-ttu-id="25d2f-106">當 VMR 處於視窗模式或無視窗模式時，可以使用混合模式。</span><span class="sxs-lookup"><span data-stu-id="25d2f-106">Mixing mode can be used either while the VMR is in windowed mode or windowless mode.</span></span>

<span data-ttu-id="25d2f-107">混合模式需要圖形驅動程式支援 DDCAPS \_ BLTFOURCC 和 DDCAPS \_ BLTSTRETCH 功能旗標 (色彩空間轉換和延展 blitting，分別) 。</span><span class="sxs-lookup"><span data-stu-id="25d2f-107">Mixing mode requires that the graphics driver supports the DDCAPS\_BLTFOURCC and DDCAPS\_BLTSTRETCH capability flags (color space conversion and stretch blitting, respectively).</span></span> <span data-ttu-id="25d2f-108">幾乎所有新的圖形驅動程式都具有這些功能。</span><span class="sxs-lookup"><span data-stu-id="25d2f-108">Almost all new graphics drivers have those capabilities.</span></span> <span data-ttu-id="25d2f-109">此外，驅動程式必須支援為目前的顯示圖元深度建立 Direct3D 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="25d2f-109">In addition, the driver must support the creation of Direct3D render targets for the current display pixel depth.</span></span> <span data-ttu-id="25d2f-110">當顯示器設為每圖元24位時，某些裝置不支援 Direct3D 作業。</span><span class="sxs-lookup"><span data-stu-id="25d2f-110">Some devices do not support Direct3D operations when the display is set to 24 bits per pixel.</span></span> <span data-ttu-id="25d2f-111">如需詳細資訊，請參閱 DirectX 圖形 SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="25d2f-111">For more information, see the DirectX Graphics SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="25d2f-112">當 VMR 混合多個影片串流時，不會正確搜尋篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="25d2f-112">When the VMR mixes multiple video streams, the filter graph does not seek correctly.</span></span> <span data-ttu-id="25d2f-113">如果您需要搜尋多個影片串流，您必須建立個別的篩選圖形，以共用相同的自訂配置器呈現者物件。</span><span class="sxs-lookup"><span data-stu-id="25d2f-113">If you need to seek multiple video streams, you must create separate filter graphs that share the same custom allocator-presenter object.</span></span>

 

<span data-ttu-id="25d2f-114">**針對多個資料流程設定 VMR-7**</span><span class="sxs-lookup"><span data-stu-id="25d2f-114">**Configuring the VMR-7 for Multiple Streams**</span></span>

<span data-ttu-id="25d2f-115">若要使用 VMR-7 轉譯多個輸入資料流程，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="25d2f-115">To render multiple input streams with the VMR-7, do the following:</span></span>

1.  <span data-ttu-id="25d2f-116">在連接任何 VMR 的輸入圖釘之前，請以資料流程的數目呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) 方法。</span><span class="sxs-lookup"><span data-stu-id="25d2f-116">Before connecting any of the VMR's input pins, call the [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) method with the number of streams.</span></span> <span data-ttu-id="25d2f-117">這會導致 VMR 載入混音器和組合器，並建立指定數目的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="25d2f-117">This causes the VMR to load the mixer and compositor and to create the specified number of input pins.</span></span>
2.  <span data-ttu-id="25d2f-118">呼叫 [**IVMRFilterConfig：： SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) 來指定各種轉譯喜好設定。</span><span class="sxs-lookup"><span data-stu-id="25d2f-118">Call [**IVMRFilterConfig::SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) to specify various rendering preferences.</span></span>
3.  <span data-ttu-id="25d2f-119">將釘選到上游篩選器。</span><span class="sxs-lookup"><span data-stu-id="25d2f-119">Connect the pins to the upstream filters.</span></span> <span data-ttu-id="25d2f-120">最簡單的方法是針對每個輸入資料流程呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 。</span><span class="sxs-lookup"><span data-stu-id="25d2f-120">The easiest way to do this is to call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) for each input stream.</span></span> <span data-ttu-id="25d2f-121">如果上游篩選器上的輸出 pin (通常是) 的解碼器，而且 VMR 上的輸入 pin 不能同意連接，則會建立具有預設設定的 VMR 實例。</span><span class="sxs-lookup"><span data-stu-id="25d2f-121">If the output pin on the upstream filter (usually a decoder) and the input pin on the VMR cannot agree on a connection, then a new instance of the VMR with default settings will be created.</span></span> <span data-ttu-id="25d2f-122">這會導致標題列中有 "ActiveMovie" 的新視窗。</span><span class="sxs-lookup"><span data-stu-id="25d2f-122">This will result in a new window with "ActiveMovie" in the title bar.</span></span> <span data-ttu-id="25d2f-123">為了避免發生這種情況，應用程式應該一律透過呼叫方法（例如 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)）來確認 VMR 的正確實例正在使用中。</span><span class="sxs-lookup"><span data-stu-id="25d2f-123">To prevent this from happening, the application should always verify that the correct instance of the VMR is being used by calling a method such as [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto).</span></span> <span data-ttu-id="25d2f-124">另一個選項是新增來源篩選器，然後使用 **IGraphBuilder：： connect** 連接 pin。</span><span class="sxs-lookup"><span data-stu-id="25d2f-124">Another option is to add the source filter and then connect the pins using **IGraphBuilder::Connect**.</span></span>
4.  <span data-ttu-id="25d2f-125">使用 VMR 上的 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 介面來控制每個資料流程的參數，例如 Alpha 值、Z 順序和輸出矩形。</span><span class="sxs-lookup"><span data-stu-id="25d2f-125">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface on the VMR to control parameters for each stream, such as the alpha value, the Z-ordering, and the output rectangle.</span></span>
5.  <span data-ttu-id="25d2f-126">執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="25d2f-126">Run the filter graph.</span></span>

<span data-ttu-id="25d2f-127">**針對多個資料流程設定 VMR-9**</span><span class="sxs-lookup"><span data-stu-id="25d2f-127">**Configuring the VMR-9 for Multiple Streams**</span></span>

<span data-ttu-id="25d2f-128">根據預設，VMR-9 會建立四個輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="25d2f-128">By default, the VMR-9 creates four input pins.</span></span> <span data-ttu-id="25d2f-129">如果您想要混合四個以上的影片串流，請先呼叫 [**IVMRFilterConfig9：： SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) ，然後再連接任何輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="25d2f-129">If you want to mix more than four video streams, call [**IVMRFilterConfig9::SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) before connecting any input pins.</span></span> <span data-ttu-id="25d2f-130">您可以使用 [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) 介面來設定資料流程參數，例如 Alpha、Z 順序和位置。</span><span class="sxs-lookup"><span data-stu-id="25d2f-130">Use the [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) interface to set the stream parameters, such as alpha, Z-order, and position.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25d2f-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="25d2f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25d2f-132">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="25d2f-132">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



