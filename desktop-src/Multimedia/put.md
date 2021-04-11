---
title: put 命令
description: Put 命令定義來源影像的區域和用於顯示的目的地視窗。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- put 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105707"
---
# <a name="put-command"></a><span data-ttu-id="51bc4-105">put 命令</span><span class="sxs-lookup"><span data-stu-id="51bc4-105">put command</span></span>

<span data-ttu-id="51bc4-106">Put 命令定義來源影像的區域和用於顯示的目的地視窗。</span><span class="sxs-lookup"><span data-stu-id="51bc4-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="51bc4-107">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="51bc4-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="51bc4-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="51bc4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="51bc4-109">參數</span><span class="sxs-lookup"><span data-stu-id="51bc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51bc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="51bc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="51bc4-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="51bc4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="51bc4-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="51bc4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="51bc4-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span><span class="sxs-lookup"><span data-stu-id="51bc4-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="51bc4-114">用來定義區域的旗標。</span><span class="sxs-lookup"><span data-stu-id="51bc4-114">Flag for defining the area.</span></span> <span data-ttu-id="51bc4-115">下表列出可辨識 put 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="51bc4-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="51bc4-116">值</span><span class="sxs-lookup"><span data-stu-id="51bc4-116">Value</span></span>        | <span data-ttu-id="51bc4-117">意義</span><span class="sxs-lookup"><span data-stu-id="51bc4-117">Meaning</span></span>                                                                                      | <span data-ttu-id="51bc4-118">意義</span><span class="sxs-lookup"><span data-stu-id="51bc4-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bc4-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="51bc4-119">digitalvideo</span></span> | <span data-ttu-id="51bc4-120">*矩形* 來源來源 *矩形框架框架* 的 *目的地* 目的地</span><span class="sxs-lookup"><span data-stu-id="51bc4-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="51bc4-121">矩形 *視窗視窗* 用戶端 *矩形視窗客戶\*\*端的影片* 影片</span><span class="sxs-lookup"><span data-stu-id="51bc4-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="51bc4-122">overlay</span><span class="sxs-lookup"><span data-stu-id="51bc4-122">overlay</span></span>      | <span data-ttu-id="51bc4-123">*矩形框架框架\*\*的目的地* 目的地</span><span class="sxs-lookup"><span data-stu-id="51bc4-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="51bc4-124">*矩形\*\*上的來源來源影片影片* 影片</span><span class="sxs-lookup"><span data-stu-id="51bc4-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="51bc4-125">下表列出可在 **lpszRegions** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="51bc4-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="51bc4-126">值</span><span class="sxs-lookup"><span data-stu-id="51bc4-126">Value</span></span>                        | <span data-ttu-id="51bc4-127">意義</span><span class="sxs-lookup"><span data-stu-id="51bc4-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bc4-128">目的地</span><span class="sxs-lookup"><span data-stu-id="51bc4-128">destination</span></span>                  | <span data-ttu-id="51bc4-129">選取目的地視窗的整個工作區以顯示資料。</span><span class="sxs-lookup"><span data-stu-id="51bc4-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="51bc4-130">在 *矩形* 的目的地</span><span class="sxs-lookup"><span data-stu-id="51bc4-130">destination at *rectangle*</span></span>   | <span data-ttu-id="51bc4-131">選取用來顯示影像之目的視窗的部分工作區。</span><span class="sxs-lookup"><span data-stu-id="51bc4-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="51bc4-132">當指定顯示視窗的區域且裝置支援延展時，會將來源影像延伸至目的地位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="51bc4-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="51bc4-133">框架</span><span class="sxs-lookup"><span data-stu-id="51bc4-133">frame</span></span>                        | <span data-ttu-id="51bc4-134">選取整個框架緩衝區以接收傳入的影片影像。</span><span class="sxs-lookup"><span data-stu-id="51bc4-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="51bc4-135">*矩形* 的框架</span><span class="sxs-lookup"><span data-stu-id="51bc4-135">frame at *rectangle*</span></span>         | <span data-ttu-id="51bc4-136">選取畫面格緩衝區的一部分，以接收傳入的影片影像。</span><span class="sxs-lookup"><span data-stu-id="51bc4-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51bc4-137">source</span><span class="sxs-lookup"><span data-stu-id="51bc4-137">source</span></span>                       | <span data-ttu-id="51bc4-138">選取要顯示在目的地視窗中的整個影像。</span><span class="sxs-lookup"><span data-stu-id="51bc4-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="51bc4-139">來源的 *矩形*</span><span class="sxs-lookup"><span data-stu-id="51bc4-139">source at *rectangle*</span></span>        | <span data-ttu-id="51bc4-140">選取要在目的地視窗中顯示的影像部分。</span><span class="sxs-lookup"><span data-stu-id="51bc4-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="51bc4-141">當您指定來源影像的區域，且裝置支援擴充功能時，會將來源影像延展至目的地位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="51bc4-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="51bc4-142">影片</span><span class="sxs-lookup"><span data-stu-id="51bc4-142">video</span></span>                        | <span data-ttu-id="51bc4-143">選取要在框架緩衝區中捕捉的整個傳入影片影像。</span><span class="sxs-lookup"><span data-stu-id="51bc4-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="51bc4-144">在 *矩形* 的影片</span><span class="sxs-lookup"><span data-stu-id="51bc4-144">video at *rectangle*</span></span>         | <span data-ttu-id="51bc4-145">選取要在框架緩衝區中捕捉的傳入影片影像部分。</span><span class="sxs-lookup"><span data-stu-id="51bc4-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="51bc4-146">時間範圍</span><span class="sxs-lookup"><span data-stu-id="51bc4-146">window</span></span>                       | <span data-ttu-id="51bc4-147">還原顯示畫面上的初始視窗大小。</span><span class="sxs-lookup"><span data-stu-id="51bc4-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="51bc4-148">此命令也會顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="51bc4-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="51bc4-149">*矩形* 中的視窗</span><span class="sxs-lookup"><span data-stu-id="51bc4-149">window at *rectangle*</span></span>        | <span data-ttu-id="51bc4-150">變更顯示視窗的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="51bc4-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="51bc4-151">指定的矩形相對於顯示視窗的父視窗 (一般而言，如果 [開啟](open.md) 的命令使用「樣式子」旗標，則桌面) 。</span><span class="sxs-lookup"><span data-stu-id="51bc4-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="51bc4-152">若要變更視窗的位置，而不變更其高度或寬度，請將 [高度] 和 [寬度] 指定為零。</span><span class="sxs-lookup"><span data-stu-id="51bc4-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="51bc4-153">視窗用戶端</span><span class="sxs-lookup"><span data-stu-id="51bc4-153">window client</span></span>                | <span data-ttu-id="51bc4-154">還原視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="51bc4-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="51bc4-155">*矩形* 中的視窗用戶端</span><span class="sxs-lookup"><span data-stu-id="51bc4-155">window client at *rectangle*</span></span> | <span data-ttu-id="51bc4-156">變更視窗工作區的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="51bc4-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="51bc4-157">指定的矩形相對於用戶端視窗的父視窗。</span><span class="sxs-lookup"><span data-stu-id="51bc4-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="51bc4-158">若要變更視窗的位置，而不變更其高度或寬度，請將 [高度] 和 [寬度] 指定為零。</span><span class="sxs-lookup"><span data-stu-id="51bc4-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="51bc4-159">當旗標包含矩形時，矩形座標會相對於視窗原點或影像原點（視情況而定），並指定為 **X1 Y1 X2 Y2**。</span><span class="sxs-lookup"><span data-stu-id="51bc4-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="51bc4-160">座標 **X1Y1** 指定左上角，而座標 **X2Y2** 則指定矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="51bc4-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="51bc4-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="51bc4-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="51bc4-162">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="51bc4-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="51bc4-163">若為數位視訊裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="51bc4-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="51bc4-164">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="51bc4-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51bc4-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="51bc4-165">Return Value</span></span>

<span data-ttu-id="51bc4-166">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="51bc4-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51bc4-167">備註</span><span class="sxs-lookup"><span data-stu-id="51bc4-167">Remarks</span></span>

<span data-ttu-id="51bc4-168">Put 命令會在使用影片重迭裝置時，定義下列一或多個矩形：</span><span class="sxs-lookup"><span data-stu-id="51bc4-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="51bc4-169">影片矩形會定義要捕捉之內送影片影像的區域。</span><span class="sxs-lookup"><span data-stu-id="51bc4-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="51bc4-170">框架矩形會定義接收傳入影片影像的框架緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="51bc4-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="51bc4-171">來源矩形會定義要將框架緩衝區的哪個區域複製到目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="51bc4-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="51bc4-172">目的地矩形會定義接收影片影像之顯示視窗工作區的區域。</span><span class="sxs-lookup"><span data-stu-id="51bc4-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="51bc4-173">影片矩形與框架矩形相關，與來源矩形與目的地矩形的關聯方式相同。</span><span class="sxs-lookup"><span data-stu-id="51bc4-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="51bc4-174">從影片矩形到框架矩形，以及從來源矩形到目的矩形，都可以進行延展。</span><span class="sxs-lookup"><span data-stu-id="51bc4-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="51bc4-175">並非所有裝置都支援延展，而且必須使用 [set](set.md) 命令) 來啟用延展 (。</span><span class="sxs-lookup"><span data-stu-id="51bc4-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="51bc4-176">下列命令會定義影片、畫面格和來源的三個區域。</span><span class="sxs-lookup"><span data-stu-id="51bc4-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="51bc4-177">此範例中的區域定義如下：</span><span class="sxs-lookup"><span data-stu-id="51bc4-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="51bc4-178">傳入影片資料的200到200圖元區域（從左上角開始，從原點120圖元開始）將會被捕獲到框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="51bc4-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="51bc4-179">影片資料會放在框架緩衝區左上角的200到200圖元區域中。</span><span class="sxs-lookup"><span data-stu-id="51bc4-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="51bc4-180">從框架緩衝區左上角的200到 200-圖元區域傳輸到目的地視窗。</span><span class="sxs-lookup"><span data-stu-id="51bc4-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bc4-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="51bc4-181">Requirements</span></span>



| <span data-ttu-id="51bc4-182">需求</span><span class="sxs-lookup"><span data-stu-id="51bc4-182">Requirement</span></span> | <span data-ttu-id="51bc4-183">值</span><span class="sxs-lookup"><span data-stu-id="51bc4-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="51bc4-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51bc4-184">Minimum supported client</span></span><br/> | <span data-ttu-id="51bc4-185">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bc4-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51bc4-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51bc4-186">Minimum supported server</span></span><br/> | <span data-ttu-id="51bc4-187">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bc4-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="51bc4-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51bc4-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bc4-189">Mci</span><span class="sxs-lookup"><span data-stu-id="51bc4-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="51bc4-190">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="51bc4-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="51bc4-191">open</span><span class="sxs-lookup"><span data-stu-id="51bc4-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="51bc4-192">set</span><span class="sxs-lookup"><span data-stu-id="51bc4-192">set</span></span>](set.md)
</dt> </dl>

 

