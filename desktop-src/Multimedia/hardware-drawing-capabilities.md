---
title: 硬體繪圖功能
description: 硬體繪圖功能
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、繪圖
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，繪圖
- ICGetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021549"
---
# <a name="hardware-drawing-capabilities"></a><span data-ttu-id="153ce-106">硬體繪圖功能</span><span class="sxs-lookup"><span data-stu-id="153ce-106">Hardware Drawing Capabilities</span></span>

<span data-ttu-id="153ce-107">某些轉譯器可以在將影片畫面解壓縮時，直接繪製到影片硬體。</span><span class="sxs-lookup"><span data-stu-id="153ce-107">Some renderers can draw directly to video hardware as they decompress video frames.</span></span> <span data-ttu-id="153ce-108">這些轉譯器會傳回 VIDCF \_ DRAW 旗標以回應 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="153ce-108">These renderers return the VIDCF\_DRAW flag in response to the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="153ce-109">使用這種類型的轉譯器時，您的應用程式不需要處理解壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="153ce-109">When using this type of renderer, your application does not have to handle the decompressed data.</span></span> <span data-ttu-id="153ce-110">它可讓轉譯器保留解壓縮的資料以供繪製。</span><span class="sxs-lookup"><span data-stu-id="153ce-110">It lets the renderer retain the decompressed data for drawing.</span></span>

<span data-ttu-id="153ce-111">如果您的應用程式使用具有繪製功能的轉譯器，它必須處理下列工作：</span><span class="sxs-lookup"><span data-stu-id="153ce-111">If your application uses a renderer with drawing capabilities, it must handle the following tasks:</span></span>

-   <span data-ttu-id="153ce-112">選取轉譯器。</span><span class="sxs-lookup"><span data-stu-id="153ce-112">Select a renderer.</span></span>
-   <span data-ttu-id="153ce-113">指定影像格式。</span><span class="sxs-lookup"><span data-stu-id="153ce-113">Specify image formats.</span></span>
-   <span data-ttu-id="153ce-114">初始化轉譯器。</span><span class="sxs-lookup"><span data-stu-id="153ce-114">Initialize the renderer.</span></span>
-   <span data-ttu-id="153ce-115">繪製資料。</span><span class="sxs-lookup"><span data-stu-id="153ce-115">Draw the data.</span></span>
-   <span data-ttu-id="153ce-116">控制繪圖參數。</span><span class="sxs-lookup"><span data-stu-id="153ce-116">Control drawing parameters.</span></span>

## <a name="renderer-selection"></a><span data-ttu-id="153ce-117">轉譯器選取專案</span><span class="sxs-lookup"><span data-stu-id="153ce-117">Renderer Selection</span></span>

<span data-ttu-id="153ce-118">[**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)宏會開啟轉譯器，以使用指定的格式繪製影像。</span><span class="sxs-lookup"><span data-stu-id="153ce-118">The [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macro opens a renderer that can draw images with the specified format.</span></span> <span data-ttu-id="153ce-119">如果成功，則會傳回轉譯器的控制碼; 否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="153ce-119">It returns a handle of a renderer if it is successful, or zero otherwise.</span></span> <span data-ttu-id="153ce-120">此宏會使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 函式來開啟轉譯器。</span><span class="sxs-lookup"><span data-stu-id="153ce-120">This macro uses the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) function to open the renderer.</span></span>

## <a name="specifying-image-formats"></a><span data-ttu-id="153ce-121">指定影像格式</span><span class="sxs-lookup"><span data-stu-id="153ce-121">Specifying Image Formats</span></span>

<span data-ttu-id="153ce-122">因為您的應用程式不需要繪製解壓縮的資料，所以不需要特定的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="153ce-122">Because your application does not need to draw the decompressed data, it does not require a specific output format.</span></span> <span data-ttu-id="153ce-123">但是，它必須確保轉譯器可以使用輸入格式來繪製，方法是使用 [**ICM \_ draw \_ 查詢**](icm-draw-query.md) 訊息 (或使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="153ce-123">It must, however, ensure that the renderer can draw using the input format by using the [**ICM\_DRAW\_QUERY**](icm-draw-query.md) message (or use the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro).</span></span> <span data-ttu-id="153ce-124">此訊息無法判斷轉譯器是否可以繪製點陣圖。</span><span class="sxs-lookup"><span data-stu-id="153ce-124">This message cannot determine if a renderer can draw a bitmap.</span></span> <span data-ttu-id="153ce-125">如果您的應用程式必須判斷轉譯器是否可以繪製點陣圖，請使用此訊息搭配 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 函數。</span><span class="sxs-lookup"><span data-stu-id="153ce-125">If your application must determine if the renderer can draw the bitmap, use this message with the [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) function.</span></span>

<span data-ttu-id="153ce-126">您的應用程式可以使用 [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) 函式，讓轉譯器建議輸入格式。</span><span class="sxs-lookup"><span data-stu-id="153ce-126">Your application can have a renderer suggest an input format by using the [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) function.</span></span> <span data-ttu-id="153ce-127">當轉譯器將繪圖功能與解壓縮功能分開時，會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="153ce-127">This function is used when a renderer separates the drawing capabilities from the decompressing capabilities.</span></span> <span data-ttu-id="153ce-128">大部分使用繪圖函式的應用程式都不需要決定輸出格式。</span><span class="sxs-lookup"><span data-stu-id="153ce-128">Most applications using the drawing functions will not need to determine the output format.</span></span>

## <a name="renderer-initialization"></a><span data-ttu-id="153ce-129">轉譯器初始化</span><span class="sxs-lookup"><span data-stu-id="153ce-129">Renderer Initialization</span></span>

<span data-ttu-id="153ce-130">[**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin)函式會初始化轉譯器，並將其告知繪圖目的地。</span><span class="sxs-lookup"><span data-stu-id="153ce-130">The [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) function initializes a renderer and tells it the drawing destination.</span></span> <span data-ttu-id="153ce-131">此函式也可以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="153ce-131">This function can also perform the following tasks:</span></span>

-   <span data-ttu-id="153ce-132">判斷轉譯器是否支援特定輸入格式。</span><span class="sxs-lookup"><span data-stu-id="153ce-132">Determine whether the renderer supports a specific input format.</span></span>
-   <span data-ttu-id="153ce-133">指定繪圖作業是否佔用視窗或整個畫面。</span><span class="sxs-lookup"><span data-stu-id="153ce-133">Specify whether the drawing operation occupies a window or the entire screen.</span></span>
-   <span data-ttu-id="153ce-134">使用來源矩形來指定要顯示的影像部分。</span><span class="sxs-lookup"><span data-stu-id="153ce-134">Specify the part of the image to display using the source rectangle.</span></span>
-   <span data-ttu-id="153ce-135">定義影像順序的播放速率。</span><span class="sxs-lookup"><span data-stu-id="153ce-135">Define the playback rate of the image sequence.</span></span>

<span data-ttu-id="153ce-136">某些轉譯器會緩衝處理壓縮的資料，以便更有效率地運作。</span><span class="sxs-lookup"><span data-stu-id="153ce-136">Some renderers buffer the compressed data to operate more efficiently.</span></span> <span data-ttu-id="153ce-137">您的應用程式可以傳送 [**ICM \_ GETBUFFERSWANTED**](icm-getbufferswanted.md) 訊息 (或使用 [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) 宏) 來判斷轉譯器要求的緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="153ce-137">Your application can send the [**ICM\_GETBUFFERSWANTED**](icm-getbufferswanted.md) message (or use the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro) to determine the number of buffers the renderer requests.</span></span> <span data-ttu-id="153ce-138">您的應用程式應該預先載入這些緩衝區，並在繪製之前將它們傳送至轉譯器。</span><span class="sxs-lookup"><span data-stu-id="153ce-138">Your application should preload these buffers and send them to the renderer before drawing.</span></span>

## <a name="drawing-the-data"></a><span data-ttu-id="153ce-139">繪製資料</span><span class="sxs-lookup"><span data-stu-id="153ce-139">Drawing the Data</span></span>

<span data-ttu-id="153ce-140">您可以使用 [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) 函數將資料解壓縮以進行繪製。</span><span class="sxs-lookup"><span data-stu-id="153ce-140">You can use the [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) function to decompress the data for drawing.</span></span> <span data-ttu-id="153ce-141">但是，在您的應用程式傳送 [**ICM \_ DRAW \_ 開始**](icm-draw-start.md) 訊息 (或使用 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) 宏) 之前，轉譯器不會開始繪製資料。</span><span class="sxs-lookup"><span data-stu-id="153ce-141">The renderer, however, does not start drawing data until your application sends the [**ICM\_DRAW\_START**](icm-draw-start.md) message (or uses the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro).</span></span> <span data-ttu-id="153ce-142">當您的應用程式呼叫這個函式時，轉譯器會開始依 *dwRate* 參數所指定的速率除以 *dwScale* 參數來繪製框架;當應用程式使用 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 函式初始化轉譯器時，會提供這些參數。</span><span class="sxs-lookup"><span data-stu-id="153ce-142">When your application calls this function, the renderer begins to draw the frames at the rate specified by the *dwRate* parameter divided by the *dwScale* parameter; these parameters were supplied when the application initialized the renderer by using the [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) function.</span></span> <span data-ttu-id="153ce-143">繪圖會繼續進行，直到您的應用程式傳送 [**ICM \_ DRAW \_ 停止**](icm-draw-stop.md) 訊息 (或使用 [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="153ce-143">Drawing continues until your application sends the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message (or uses the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro).</span></span>

> [!Note]  
> <span data-ttu-id="153ce-144">如果轉譯器在繪圖之前緩衝資料，您的應用程式就不應該使用 **ICDrawStart** 宏，直到傳送轉譯器針對 **ICGetBuffersWanted** 宏傳回的框架數為止。</span><span class="sxs-lookup"><span data-stu-id="153ce-144">If a renderer buffers the data before drawing, your application should not use the **ICDrawStart** macro until it has sent the number of frames the renderer returned for the **ICGetBuffersWanted** macro.</span></span>

 

<span data-ttu-id="153ce-145">[**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw)的 *lTime* 參數會指定繪製框架的時間。</span><span class="sxs-lookup"><span data-stu-id="153ce-145">The *lTime* parameter of [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) specifies the time to draw a frame.</span></span> <span data-ttu-id="153ce-146">轉譯器會將這個整數除以以 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 指定的時間範圍，以取得實際時間。</span><span class="sxs-lookup"><span data-stu-id="153ce-146">The renderer divides this integer by the time scale specified with [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) to obtain the actual time.</span></span> <span data-ttu-id="153ce-147">**ICDraw** 函數的時間相對於 **ICDrawStart**。</span><span class="sxs-lookup"><span data-stu-id="153ce-147">Times for **ICDraw** functions are relative to **ICDrawStart**.</span></span> <span data-ttu-id="153ce-148">**ICDrawStart** 會將時鐘設定為零。</span><span class="sxs-lookup"><span data-stu-id="153ce-148">**ICDrawStart** sets the clock to zero.</span></span> <span data-ttu-id="153ce-149">例如，如果您的應用程式針對 *lTime* 的時間刻度和75指定1000，則轉譯器會將畫面格75毫秒繪製到序列中。</span><span class="sxs-lookup"><span data-stu-id="153ce-149">For example, if your application specifies 1000 for the time scale and 75 for *lTime*, the renderer draws the frame 75 milliseconds into the sequence.</span></span>

## <a name="controlling-drawing-parameters"></a><span data-ttu-id="153ce-150">控制繪圖參數</span><span class="sxs-lookup"><span data-stu-id="153ce-150">Controlling Drawing Parameters</span></span>

<span data-ttu-id="153ce-151">您可以藉由傳送 [**icm \_ draw \_ GETTIME**](icm-draw-gettime.md) 訊息 (或使用 [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) 宏) 來監視轉譯器的時鐘，也可以設定轉譯器的時鐘，藉由傳送 [**ICM \_ draw \_ SETTIME**](icm-draw-settime.md) 訊息 (或使用 [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) 宏) 來繪製資料。</span><span class="sxs-lookup"><span data-stu-id="153ce-151">You can monitor the clock of a renderer by sending the [**ICM\_DRAW\_GETTIME**](icm-draw-gettime.md) message (or use the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro), and you can set the clock of a renderer that can draw data by sending the [**ICM\_DRAW\_SETTIME**](icm-draw-settime.md) message (or use the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro).</span></span>

<span data-ttu-id="153ce-152">若要在轉譯器繪製時變更目前的位置，您的應用程式可以傳送 [**ICM \_ 繪製 \_ 視窗**](icm-draw-window.md) 訊息 (或使用 [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) 宏) 來錨定視窗。</span><span class="sxs-lookup"><span data-stu-id="153ce-152">To change the current position while a renderer is drawing, your application can send the [**ICM\_DRAW\_WINDOW**](icm-draw-window.md) message (or use the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro) for repositioning the window.</span></span> <span data-ttu-id="153ce-153">當視窗變更時，應用程式通常會使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="153ce-153">Applications typically use this message whenever the window changes.</span></span>

<span data-ttu-id="153ce-154">如果播放視窗取得好用的調色板訊息，則您的應用程式必須傳送 [**ICM \_ DRAW \_ 實現**](icm-draw-realize.md) 訊息 (或使用 [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) 宏) ，讓轉譯器再次發現該調色板以供播放。</span><span class="sxs-lookup"><span data-stu-id="153ce-154">If the playback window gets a realize-palette message, your application must send the [**ICM\_DRAW\_REALIZE**](icm-draw-realize.md) message (or use the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro) to have the renderer realize the palette again for playback.</span></span> <span data-ttu-id="153ce-155">應用程式可以藉由傳送 [**icm \_ draw \_ CHANGEPALETTE**](icm-draw-changepalette.md) 訊息 (或使用 [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) 宏) 來變更選擇區，並藉由傳送 [**icm \_ draw \_ GET \_ 調板**](icm-draw-get-palette.md) 訊息來取得目前的調色板。</span><span class="sxs-lookup"><span data-stu-id="153ce-155">Applications can change the palette by sending the [**ICM\_DRAW\_CHANGEPALETTE**](icm-draw-changepalette.md) message (or use the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro) and obtain the current palette by sending the [**ICM\_DRAW\_GET\_PALETTE**](icm-draw-get-palette.md) message.</span></span>

<span data-ttu-id="153ce-156">某些轉譯器必須明確指示，以顯示傳遞給它們的畫面格。</span><span class="sxs-lookup"><span data-stu-id="153ce-156">Some renderers must be specifically instructed to display frames passed to them.</span></span> <span data-ttu-id="153ce-157">傳送 [**ICM \_ DRAW \_ RENDERBUFFER**](icm-draw-renderbuffer.md) 訊息 (或使用 [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) 宏) 會導致這些轉譯器繪製框架。</span><span class="sxs-lookup"><span data-stu-id="153ce-157">Sending the [**ICM\_DRAW\_RENDERBUFFER**](icm-draw-renderbuffer.md) message (or use the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro) causes these renderers to draw the frame.</span></span>

 

 




