---
title: where 命令
description: Where 命令會捕獲指定來源或目的地區域的矩形。 這個矩形是使用 put 命令指定的。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- where 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934934"
---
# <a name="where-command"></a><span data-ttu-id="6c298-106">where 命令</span><span class="sxs-lookup"><span data-stu-id="6c298-106">where command</span></span>

<span data-ttu-id="6c298-107">Where 命令會捕獲指定來源或目的地區域的矩形。</span><span class="sxs-lookup"><span data-stu-id="6c298-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="6c298-108">這個矩形是使用 [put](put.md) 命令指定的。</span><span class="sxs-lookup"><span data-stu-id="6c298-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="6c298-109">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6c298-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="6c298-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6c298-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6c298-111">參數</span><span class="sxs-lookup"><span data-stu-id="6c298-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c298-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6c298-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6c298-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c298-113">Identifier of an MCI device.</span></span> <span data-ttu-id="6c298-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="6c298-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6c298-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span><span class="sxs-lookup"><span data-stu-id="6c298-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="6c298-116">識別要抓取其維度之矩形的旗標。</span><span class="sxs-lookup"><span data-stu-id="6c298-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="6c298-117">下表列出可辨識 **where** 命令和每個型別所使用之旗標的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="6c298-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="6c298-118">值</span><span class="sxs-lookup"><span data-stu-id="6c298-118">Value</span></span>        | <span data-ttu-id="6c298-119">意義</span><span class="sxs-lookup"><span data-stu-id="6c298-119">Meaning</span></span>                                                       | <span data-ttu-id="6c298-120">意義</span><span class="sxs-lookup"><span data-stu-id="6c298-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="6c298-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="6c298-121">digitalvideo</span></span> | <span data-ttu-id="6c298-122">destinationdestination [**max**](max.md)frameframe maxsource</span><span class="sxs-lookup"><span data-stu-id="6c298-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="6c298-123">來源 maxvideovideo maxwindowwindow 最大值</span><span class="sxs-lookup"><span data-stu-id="6c298-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="6c298-124">overlay</span><span class="sxs-lookup"><span data-stu-id="6c298-124">overlay</span></span>      | <span data-ttu-id="6c298-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="6c298-125">destinationframe</span></span>                                              | <span data-ttu-id="6c298-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="6c298-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="6c298-127">下表列出可在 **lpszRequestRect** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="6c298-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="6c298-128">值</span><span class="sxs-lookup"><span data-stu-id="6c298-128">Value</span></span>                          | <span data-ttu-id="6c298-129">意義</span><span class="sxs-lookup"><span data-stu-id="6c298-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c298-130">目的地</span><span class="sxs-lookup"><span data-stu-id="6c298-130">destination</span></span>                    | <span data-ttu-id="6c298-131">抓取目的地位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="6c298-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="6c298-132">若為影片重迭裝置，目的地矩形會定義顯示視窗工作區的區域，以顯示來自框架緩衝區的影像資料。</span><span class="sxs-lookup"><span data-stu-id="6c298-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="6c298-133">目的地 [**最大值**](max.md)</span><span class="sxs-lookup"><span data-stu-id="6c298-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="6c298-134">抓取用戶端矩形的目前大小。</span><span class="sxs-lookup"><span data-stu-id="6c298-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6c298-135">框架</span><span class="sxs-lookup"><span data-stu-id="6c298-135">frame</span></span>                          | <span data-ttu-id="6c298-136">抓取框架緩衝區矩形的位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="6c298-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="6c298-137">框架緩衝區矩形會定義接收傳入影片資料的框架緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="6c298-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="6c298-138">「影片」矩形中的影像會縮放到此區域。</span><span class="sxs-lookup"><span data-stu-id="6c298-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="6c298-139">[**最大** 框架](max.md)</span><span class="sxs-lookup"><span data-stu-id="6c298-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="6c298-140">傳回框架緩衝區的大小上限。</span><span class="sxs-lookup"><span data-stu-id="6c298-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6c298-141">source</span><span class="sxs-lookup"><span data-stu-id="6c298-141">source</span></span>                         | <span data-ttu-id="6c298-142">捕獲來源位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="6c298-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="6c298-143">若為影片重迭裝置，來源矩形會定義在目的地視窗中顯示的框架緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="6c298-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="6c298-144">裝置會使用這個矩形來裁剪影像，再將它伸展，以符合顯示上的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="6c298-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="6c298-145">來源 [**最大值**](max.md)</span><span class="sxs-lookup"><span data-stu-id="6c298-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="6c298-146">抓取框架緩衝區的大小上限。</span><span class="sxs-lookup"><span data-stu-id="6c298-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6c298-147">影片</span><span class="sxs-lookup"><span data-stu-id="6c298-147">video</span></span>                          | <span data-ttu-id="6c298-148">捕獲影片矩形的位移和範圍。</span><span class="sxs-lookup"><span data-stu-id="6c298-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="6c298-149">影片矩形會定義傳送至框架緩衝區之傳入影片資料的區域。</span><span class="sxs-lookup"><span data-stu-id="6c298-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="6c298-150">影片 [**最大值**](max.md)</span><span class="sxs-lookup"><span data-stu-id="6c298-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="6c298-151">傳回輸入的大小上限。</span><span class="sxs-lookup"><span data-stu-id="6c298-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6c298-152">時間範圍</span><span class="sxs-lookup"><span data-stu-id="6c298-152">window</span></span>                         | <span data-ttu-id="6c298-153">抓取顯示視窗框架的目前大小和位置。</span><span class="sxs-lookup"><span data-stu-id="6c298-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="6c298-154">視窗 [**最大值**](max.md)</span><span class="sxs-lookup"><span data-stu-id="6c298-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="6c298-155">抓取整個顯示器的大小。</span><span class="sxs-lookup"><span data-stu-id="6c298-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="6c298-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6c298-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6c298-157">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="6c298-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6c298-158">若為數位視訊裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="6c298-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="6c298-159">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6c298-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c298-160">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c298-160">Return Value</span></span>

<span data-ttu-id="6c298-161">傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函數的 *lpszReturnString* 參數中的矩形。</span><span class="sxs-lookup"><span data-stu-id="6c298-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="6c298-162">矩形描述此命令的 *lpszRequestRect* 參數中指定的區域。</span><span class="sxs-lookup"><span data-stu-id="6c298-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="6c298-163">矩形會指定為 *X1 Y1 X2 Y2*。</span><span class="sxs-lookup"><span data-stu-id="6c298-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="6c298-164">座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="6c298-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="6c298-165">範例</span><span class="sxs-lookup"><span data-stu-id="6c298-165">Examples</span></span>

<span data-ttu-id="6c298-166">下列命令會傳回 "movie" 裝置的顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="6c298-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="6c298-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c298-167">Requirements</span></span>



| <span data-ttu-id="6c298-168">需求</span><span class="sxs-lookup"><span data-stu-id="6c298-168">Requirement</span></span> | <span data-ttu-id="6c298-169">值</span><span class="sxs-lookup"><span data-stu-id="6c298-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6c298-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c298-170">Minimum supported client</span></span><br/> | <span data-ttu-id="6c298-171">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c298-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6c298-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c298-172">Minimum supported server</span></span><br/> | <span data-ttu-id="6c298-173">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c298-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6c298-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c298-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c298-175">Mci</span><span class="sxs-lookup"><span data-stu-id="6c298-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6c298-176">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="6c298-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6c298-177">把</span><span class="sxs-lookup"><span data-stu-id="6c298-177">put</span></span>](put.md)
</dt> </dl>

 

