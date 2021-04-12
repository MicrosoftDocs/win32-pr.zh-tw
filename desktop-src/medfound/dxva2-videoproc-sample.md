---
description: 說明如何使用 DXVA 影片處理。
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317975"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="7bcf7-103">DXVA2 \_ VideoProc 範例</span><span class="sxs-lookup"><span data-stu-id="7bcf7-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="7bcf7-104">說明如何使用 [DXVA 影片處理](dxva-video-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="7bcf7-105">此範例會以程式設計方式產生具有主要資料流程和子資料流程的影片。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="7bcf7-106">主要資料流程會顯示 SMPTE 色軸，而子資料流程是半透明的矩形。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="7bcf7-107">接著會使用 DXVA 視頻處理器來處理並顯示影片。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="7bcf7-108">使用者可以變更平面 Alpha 值、來源和目的地矩形、色彩調整和色彩空間。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![dxva2 videoproc 範例的螢幕擷取畫面 \-](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="7bcf7-110">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="7bcf7-110">APIs Demonstrated</span></span>

<span data-ttu-id="7bcf7-111">這個範例會示範下列 DXVA 介面：</span><span class="sxs-lookup"><span data-stu-id="7bcf7-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="7bcf7-112">**IDirectXVideoProcessorService**</span><span class="sxs-lookup"><span data-stu-id="7bcf7-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="7bcf7-113">**IDirectXVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="7bcf7-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="7bcf7-114">使用方式</span><span class="sxs-lookup"><span data-stu-id="7bcf7-114">Usage</span></span>

<span data-ttu-id="7bcf7-115">DXVA2 \_ VideoProc 範例會建立 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="7bcf7-116">命令列選項：</span><span class="sxs-lookup"><span data-stu-id="7bcf7-116">Command line options:</span></span>



| <span data-ttu-id="7bcf7-117">選項</span><span class="sxs-lookup"><span data-stu-id="7bcf7-117">Option</span></span> | <span data-ttu-id="7bcf7-118">Description</span><span class="sxs-lookup"><span data-stu-id="7bcf7-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7bcf7-119">-hh</span><span class="sxs-lookup"><span data-stu-id="7bcf7-119">-hh</span></span>    | <span data-ttu-id="7bcf7-120">強制應用程式使用硬體 Direct3D 裝置和硬體 DXVA 裝置。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="7bcf7-121">-hs</span><span class="sxs-lookup"><span data-stu-id="7bcf7-121">-hs</span></span>    | <span data-ttu-id="7bcf7-122">強制應用程式使用硬體 Direct3D 裝置和軟體 DXVA 裝置。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="7bcf7-123">-ss</span><span class="sxs-lookup"><span data-stu-id="7bcf7-123">-ss</span></span>    | <span data-ttu-id="7bcf7-124">強制應用程式使用軟體 Direct3D 裝置和軟體 DXVA 裝置。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="7bcf7-125">鍵盤命令：</span><span class="sxs-lookup"><span data-stu-id="7bcf7-125">Keyboard commands:</span></span>



| <span data-ttu-id="7bcf7-126">Key</span><span class="sxs-lookup"><span data-stu-id="7bcf7-126">Key</span></span>       | <span data-ttu-id="7bcf7-127">描述</span><span class="sxs-lookup"><span data-stu-id="7bcf7-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="7bcf7-128">ALT+ENTER</span><span class="sxs-lookup"><span data-stu-id="7bcf7-128">ALT+ENTER</span></span> | <span data-ttu-id="7bcf7-129">切換視窗模式和全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="7bcf7-130">F1 – F8</span><span class="sxs-lookup"><span data-stu-id="7bcf7-130">F1–F8</span></span>     | <span data-ttu-id="7bcf7-131">輸入下表所示的其中一個模式。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="7bcf7-132">END</span><span class="sxs-lookup"><span data-stu-id="7bcf7-132">END</span></span>       | <span data-ttu-id="7bcf7-133">啟用或停用已卸載框架的偵錯工具記錄。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="7bcf7-134">HOME</span><span class="sxs-lookup"><span data-stu-id="7bcf7-134">HOME</span></span>      | <span data-ttu-id="7bcf7-135">將參數重設為其初始值。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="7bcf7-136">每個函式按鍵 F1 到 F8 都會切換至模式，以使用方向鍵來調整特定轉譯參數。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="7bcf7-137">此外，子流的色彩也會變更。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bcf7-138">Key</span><span class="sxs-lookup"><span data-stu-id="7bcf7-138">Key</span></span></th>
<th><span data-ttu-id="7bcf7-139">描述</span><span class="sxs-lookup"><span data-stu-id="7bcf7-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bcf7-140">F1</span><span class="sxs-lookup"><span data-stu-id="7bcf7-140">F1</span></span></td>
<td><span data-ttu-id="7bcf7-141">調整 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-142">向上：增加兩個數據流的平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="7bcf7-143">向下：減少這兩個數據流的平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="7bcf7-144">RIGHT：增加子流的圖元 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="7bcf7-145">左方：減少子流的圖元 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-146">子流色彩：白色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bcf7-147">F2</span><span class="sxs-lookup"><span data-stu-id="7bcf7-147">F2</span></span></td>
<td><span data-ttu-id="7bcf7-148">調整主要資料流程的來源區域 (縮放) 。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-149">向上：提高) 的垂直 (放大。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="7bcf7-150">下：減少垂直 (縮小) 。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="7bcf7-151">RIGHT：水準增加 (放大) 。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="7bcf7-152">左方：減少水準 (放大) 。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="7bcf7-153">子流色彩：紅色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bcf7-154">F3</span><span class="sxs-lookup"><span data-stu-id="7bcf7-154">F3</span></span></td>
<td><span data-ttu-id="7bcf7-155">移動主要資料流程的來源區域。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-156">向上：向上移動。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="7bcf7-157">向下：下移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="7bcf7-158">RIGHT：右移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="7bcf7-159">左方：左移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-160">子流色彩：黃色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bcf7-161">F4</span><span class="sxs-lookup"><span data-stu-id="7bcf7-161">F4</span></span></td>
<td><span data-ttu-id="7bcf7-162">調整主要資料流程的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-163">向上：垂直增加。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="7bcf7-164">向下：垂直減少。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="7bcf7-165">RIGHT：水準增加。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="7bcf7-166">左方：水準減少。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-167">子流色彩：綠色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bcf7-168">F5</span><span class="sxs-lookup"><span data-stu-id="7bcf7-168">F5</span></span></td>
<td><span data-ttu-id="7bcf7-169">移動主要資料流程的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-170">向上：向上移動。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="7bcf7-171">向下：下移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="7bcf7-172">RIGHT：右移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="7bcf7-173">左方：左移。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-174">子流色彩：青色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bcf7-175">F6</span><span class="sxs-lookup"><span data-stu-id="7bcf7-175">F6</span></span></td>
<td><span data-ttu-id="7bcf7-176">變更背景色彩或色彩空間。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-177">向上、向下：迴圈顯示色彩空間。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="7bcf7-178">靠右、靠左：迴圈顯示背景色彩。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-179">子流色彩：藍色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bcf7-180">F7</span><span class="sxs-lookup"><span data-stu-id="7bcf7-180">F7</span></span></td>
<td><span data-ttu-id="7bcf7-181">調整亮度和對比。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-182">向上：提高亮度。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="7bcf7-183">減少：降低亮度。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="7bcf7-184">RIGHT：提高對比。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="7bcf7-185">左方：減少對比。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-186">子流色彩：洋紅</span><span class="sxs-lookup"><span data-stu-id="7bcf7-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bcf7-187">F8</span><span class="sxs-lookup"><span data-stu-id="7bcf7-187">F8</span></span></td>
<td><span data-ttu-id="7bcf7-188">調整色調和飽和度。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="7bcf7-189">向上：提高色調。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="7bcf7-190">DOWN：減少色調。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="7bcf7-191">RIGHT：提高飽和度。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="7bcf7-192">左方：減少飽和度。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="7bcf7-193">子流色彩：黑色</span><span class="sxs-lookup"><span data-stu-id="7bcf7-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7bcf7-194">在每個模式中，按 HOME 鍵會將該模式的參數重設為其初始值。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bcf7-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bcf7-195">Requirements</span></span>



| <span data-ttu-id="7bcf7-196">產品</span><span class="sxs-lookup"><span data-stu-id="7bcf7-196">Product</span></span>                                                        | <span data-ttu-id="7bcf7-197">版本</span><span class="sxs-lookup"><span data-stu-id="7bcf7-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7bcf7-198">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7bcf7-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7bcf7-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7bcf7-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7bcf7-200">下載範例</span><span class="sxs-lookup"><span data-stu-id="7bcf7-200">Downloading the Sample</span></span>

<span data-ttu-id="7bcf7-201">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)中取得。</span><span class="sxs-lookup"><span data-stu-id="7bcf7-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bcf7-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bcf7-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bcf7-203">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="7bcf7-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="7bcf7-204">DXVA 影片處理</span><span class="sxs-lookup"><span data-stu-id="7bcf7-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="7bcf7-205">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="7bcf7-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




