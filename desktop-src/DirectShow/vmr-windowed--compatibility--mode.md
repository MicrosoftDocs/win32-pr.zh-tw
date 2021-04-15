---
description: VMR 視窗 (相容性) 模式
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: VMR 視窗 (相容性) 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570462"
---
# <a name="vmr-windowed-compatibility-mode"></a><span data-ttu-id="2397a-103">VMR 視窗 (相容性) 模式</span><span class="sxs-lookup"><span data-stu-id="2397a-103">VMR Windowed (Compatibility) Mode</span></span>

<span data-ttu-id="2397a-104">VMR 的設計目的是要與所有現有的 DirectShow 應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="2397a-104">The VMR is designed to be compatible with all existing DirectShow applications.</span></span> <span data-ttu-id="2397a-105">當它與現有的應用程式搭配使用時，VMR 會以視窗模式使用單一影片串流（也稱為相容性模式）來運作。</span><span class="sxs-lookup"><span data-stu-id="2397a-105">When it is used with an existing application, the VMR operates in windowed mode with a single video stream, also called compatibility mode.</span></span> <span data-ttu-id="2397a-106">提供此模式的原因是，VMR-7 是 Windows XP 上的預設轉譯器，因此會自動用於對 [智慧型連接](intelligent-connect.md) 方法的呼叫，例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)。</span><span class="sxs-lookup"><span data-stu-id="2397a-106">This mode is provided because the VMR-7 is the default renderer on Windows XP, and is therefore automatically used in calls to [Intelligent Connect](intelligent-connect.md) methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="2397a-107">如果您的應用程式使用智慧型 Connect，而且只需要基本的轉譯功能，您就不需要任何特殊的程式碼，就能在 Windows XP 上正確地使用 VMR-7 轉譯。</span><span class="sxs-lookup"><span data-stu-id="2397a-107">If your application uses Intelligent Connect and requires only basic rendering capabilities, you do not need any special code to render correctly with the VMR-7 on Windows XP.</span></span>

<span data-ttu-id="2397a-108">VMR-9 預設也會在視窗型/相容性模式下執行。</span><span class="sxs-lookup"><span data-stu-id="2397a-108">The VMR-9 also runs in windowed/compatibility mode by default.</span></span> <span data-ttu-id="2397a-109">不過，VMR-9 永遠不是預設的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2397a-109">However, the VMR-9 is never the default video renderer.</span></span> <span data-ttu-id="2397a-110">若要在應用程式中使用 VMR-9，您必須明確地將它加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="2397a-110">To use the VMR-9 in an application, you must explicitly add it to the filter graph.</span></span> <span data-ttu-id="2397a-111">基於這個理由，而且因為無視窗模式提供比視窗模式更好的功能，所以在視窗型/相容性模式中使用 VMR-9 沒有特定的優點。</span><span class="sxs-lookup"><span data-stu-id="2397a-111">For that reason, and because windowless mode provides better functionality than windowed mode, there is no particular advantage to using the VMR-9 in windowed/compatibility mode.</span></span>

<span data-ttu-id="2397a-112">**在視窗型/相容性模式中使用 VMR-7**</span><span class="sxs-lookup"><span data-stu-id="2397a-112">**Using the VMR-7 in Windowed/Compatibility Mode**</span></span>

<span data-ttu-id="2397a-113">不需要進行任何特殊的程式設計，就能在視窗型/相容性模式下設定或控制 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="2397a-113">No special programming is required to set up or control the VMR-7 in windowed/compatibility mode.</span></span> <span data-ttu-id="2397a-114">只要使用標準的圖形建立呼叫來建立篩選圖形，VMR 就會預設為這種模式。</span><span class="sxs-lookup"><span data-stu-id="2397a-114">Simply build the filter graph using the standard graph-building calls, and the VMR-7 will default to this mode.</span></span>

<span data-ttu-id="2397a-115">在視窗型/相容性模式中，VMR 7 會建立自己的視窗來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="2397a-115">In windowed/compatibility mode, the VMR-7 creates its own window to display the video.</span></span> <span data-ttu-id="2397a-116">若要這樣做，它會載入可公開 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 和 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面的視窗管理員元件。</span><span class="sxs-lookup"><span data-stu-id="2397a-116">To do so, it loads the Window Manager component, which exposes the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces.</span></span> <span data-ttu-id="2397a-117">您的應用程式可以查詢這些介面的篩選圖形管理員，與使用舊的影片轉譯器篩選器的方式完全相同。</span><span class="sxs-lookup"><span data-stu-id="2397a-117">Your application can query the Filter Graph Manager for these interfaces, exactly as you would with the old Video Renderer filter.</span></span> <span data-ttu-id="2397a-118">如需詳細資訊，請參閱 [使用視窗模式](using-windowed-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="2397a-118">For more information, see [Using Windowed Mode](using-windowed-mode.md).</span></span>

<span data-ttu-id="2397a-119">下圖顯示視窗型/相容性模式中的 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="2397a-119">The following illustration shows the VMR-7 in windowed/compatibility mode.</span></span>

![在相容性模式中 vmr](images/vmr-compat-mode.png)

<span data-ttu-id="2397a-121">為了保證最大的相容性層級，影片視窗的類別名稱會與舊的影片轉譯器篩選器所建立的相同，而且 VMR 仍會使用舊影片轉譯器的大部分視窗管理員程式碼。</span><span class="sxs-lookup"><span data-stu-id="2397a-121">To guarantee the maximum level of compatibility, the video window has the same class name as the one created by the old Video Renderer filter, and most of the Window Manager code from the old Video Renderer is still used by the VMR.</span></span> <span data-ttu-id="2397a-122">在視窗型/相容性模式中，VMR 所耗用的系統資源不會超過舊的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2397a-122">In windowed/compatibility mode, the VMR consumes no more system resources than the old Video Renderer.</span></span> <span data-ttu-id="2397a-123">因為 VMR-7 只有一個輸入資料流程處於視窗型/相容性模式，所以不會載入其混音器或組合器元件。</span><span class="sxs-lookup"><span data-stu-id="2397a-123">Since the VMR-7 has only one input stream in windowed/compatibility mode, it does not load its mixer or compositor components.</span></span>

<span data-ttu-id="2397a-124">根據預設，VMR 會伸展影像以填滿影片視窗。</span><span class="sxs-lookup"><span data-stu-id="2397a-124">By default, the VMR stretches the image to fill the video window.</span></span> <span data-ttu-id="2397a-125">若要保留來源的外觀比例，請使用 VMR ARMODE LETTER 方塊旗標來呼叫 [**IVMRAspectRatioControl：： SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) 方法 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2397a-125">To preserve the aspect ratio of the source, call the [**IVMRAspectRatioControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) method with the VMR\_ARMODE\_LETTER\_BOX flag.</span></span>

> [!Note]  
> <span data-ttu-id="2397a-126">將影片視窗放在子視窗中的 MFC 應用程式必須定義空的 WM \_ ERASEBKGND 訊息處理常式，否則影片顯示區域將無法正確地重新繪製。</span><span class="sxs-lookup"><span data-stu-id="2397a-126">MFC applications that place the video window in a child window must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="2397a-127">**在具有多個資料流程的視窗型/相容性模式中使用 VMR-7**</span><span class="sxs-lookup"><span data-stu-id="2397a-127">**Using the VMR-7 in Windowed/Compatibility Mode with Multiple Streams**</span></span>

<span data-ttu-id="2397a-128">在視窗型/相容性模式中，VMR-7 預設會建立單一輸入的 pin，並停用混合模式。</span><span class="sxs-lookup"><span data-stu-id="2397a-128">In windowed/compatibility mode, the VMR-7 creates a single input pin by default, and disables mixing mode.</span></span> <span data-ttu-id="2397a-129">若要啟用混合模式，您必須先設定 VMR，然後再進行連接。</span><span class="sxs-lookup"><span data-stu-id="2397a-129">To enable mixing mode, you must configure the VMR before you connect it.</span></span> <span data-ttu-id="2397a-130">如需詳細資訊，請參閱 [使用多個資料流程 (混合模式) 的 VMR ](vmr-with-multiple-streams--mixing-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="2397a-130">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span> <span data-ttu-id="2397a-131">在混合模式中，VMR 會載入混合和組合器元件，這需要更多的系統資源。</span><span class="sxs-lookup"><span data-stu-id="2397a-131">In mixing mode, the VMR loads the mixing and compositor components, which require more system resources.</span></span>

<span data-ttu-id="2397a-132">**在視窗模式中使用 VMR-9**</span><span class="sxs-lookup"><span data-stu-id="2397a-132">**Using the VMR-9 in Windowed Mode**</span></span>

<span data-ttu-id="2397a-133">由於 VMR-9 不是預設轉譯器，因此它的相容性模式不會像這樣。</span><span class="sxs-lookup"><span data-stu-id="2397a-133">Because the VMR-9 is not the default renderer, it does not have a compatibility mode as such.</span></span> <span data-ttu-id="2397a-134">相反地，VMR-9 預設為視窗模式，具有四個輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="2397a-134">Instead, the VMR-9 defaults to windowed mode with four input pins.</span></span> <span data-ttu-id="2397a-135">您可以使用此模式來混合最多四個影片串流。</span><span class="sxs-lookup"><span data-stu-id="2397a-135">You can use this mode to mix up to four video streams.</span></span> <span data-ttu-id="2397a-136">如果您需要混用較大量的資料流程，您必須如 VMR 中所述，設定 [多個資料流程 (混合模式) ](vmr-with-multiple-streams--mixing-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="2397a-136">If you need to mix a larger number of streams, you must configure it as described in [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span> <span data-ttu-id="2397a-137">否則，以視窗模式模式的 VMR-9 在視窗型/相容性模式中的行為就如同 VMR-7 一樣。</span><span class="sxs-lookup"><span data-stu-id="2397a-137">Otherwise, the VMR-9 in windowed mode behaves exactly like the VMR-7 in windowed/compatibility mode.</span></span>

 

 



