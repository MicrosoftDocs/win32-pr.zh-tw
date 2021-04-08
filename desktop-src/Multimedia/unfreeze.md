---
title: 解除凍結命令
description: 當凍結命令停用 reenables 時，[解除凍結] 命令會將影片捕獲到框架緩衝區。 數位影片、VCR 和影片重迭裝置會辨識此命令。
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- 解除凍結命令 Windows 多媒體
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686456"
---
# <a name="unfreeze-command"></a><span data-ttu-id="43127-105">解除凍結命令</span><span class="sxs-lookup"><span data-stu-id="43127-105">unfreeze command</span></span>

<span data-ttu-id="43127-106">當 [凍結](freeze.md) 命令停用 reenables 時，[解除凍結] 命令會將影片捕獲到框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="43127-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="43127-107">數位影片、VCR 和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="43127-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="43127-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="43127-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="43127-109">參數</span><span class="sxs-lookup"><span data-stu-id="43127-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43127-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="43127-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="43127-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43127-111">Identifier of an MCI device.</span></span> <span data-ttu-id="43127-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="43127-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="43127-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="43127-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="43127-114">用來重新啟用框架緩衝區取得影片的旗標。</span><span class="sxs-lookup"><span data-stu-id="43127-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="43127-115">下表列出可辨識 **解除凍結** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="43127-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="43127-116">值</span><span class="sxs-lookup"><span data-stu-id="43127-116">Value</span></span>        | <span data-ttu-id="43127-117">意義</span><span class="sxs-lookup"><span data-stu-id="43127-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="43127-118">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="43127-118">digitalvideo</span></span> | <span data-ttu-id="43127-119">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="43127-119">at *rectangle*</span></span> |
| <span data-ttu-id="43127-120">overlay</span><span class="sxs-lookup"><span data-stu-id="43127-120">overlay</span></span>      | <span data-ttu-id="43127-121">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="43127-121">at *rectangle*</span></span> |
| <span data-ttu-id="43127-122">錄影機</span><span class="sxs-lookup"><span data-stu-id="43127-122">vcr</span></span>          | <span data-ttu-id="43127-123">輸入輸出</span><span class="sxs-lookup"><span data-stu-id="43127-123">input output</span></span>   |



 

<span data-ttu-id="43127-124">下表列出可在 **lpszUnfreeze** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="43127-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="43127-125">值</span><span class="sxs-lookup"><span data-stu-id="43127-125">Value</span></span>          | <span data-ttu-id="43127-126">意義</span><span class="sxs-lookup"><span data-stu-id="43127-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43127-127">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="43127-127">at *rectangle*</span></span> | <span data-ttu-id="43127-128">指定將重新啟用影片的區域。</span><span class="sxs-lookup"><span data-stu-id="43127-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="43127-129">矩形相對於影片緩衝區原點，並指定為 *X1 Y1 X2 Y2*。</span><span class="sxs-lookup"><span data-stu-id="43127-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="43127-130">座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="43127-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="43127-131">input</span><span class="sxs-lookup"><span data-stu-id="43127-131">input</span></span>          | <span data-ttu-id="43127-132">解除凍結輸入影像。</span><span class="sxs-lookup"><span data-stu-id="43127-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="43127-133">output</span><span class="sxs-lookup"><span data-stu-id="43127-133">output</span></span>         | <span data-ttu-id="43127-134">解除凍結輸出影像。</span><span class="sxs-lookup"><span data-stu-id="43127-134">Unfreeze the output image.</span></span> <span data-ttu-id="43127-135">如果未提供 "input" 和 "output"，則會假設為 "output"。</span><span class="sxs-lookup"><span data-stu-id="43127-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="43127-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="43127-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="43127-137">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="43127-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="43127-138">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="43127-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="43127-139">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="43127-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43127-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="43127-140">Return Value</span></span>

<span data-ttu-id="43127-141">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="43127-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="43127-142">範例</span><span class="sxs-lookup"><span data-stu-id="43127-142">Examples</span></span>

<span data-ttu-id="43127-143">下列命令會 unfreezes 影片緩衝區的區域。</span><span class="sxs-lookup"><span data-stu-id="43127-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="43127-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="43127-144">Requirements</span></span>



| <span data-ttu-id="43127-145">需求</span><span class="sxs-lookup"><span data-stu-id="43127-145">Requirement</span></span> | <span data-ttu-id="43127-146">值</span><span class="sxs-lookup"><span data-stu-id="43127-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="43127-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43127-147">Minimum supported client</span></span><br/> | <span data-ttu-id="43127-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43127-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="43127-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43127-149">Minimum supported server</span></span><br/> | <span data-ttu-id="43127-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43127-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="43127-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43127-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43127-152">Mci</span><span class="sxs-lookup"><span data-stu-id="43127-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="43127-153">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="43127-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="43127-154">凍結</span><span class="sxs-lookup"><span data-stu-id="43127-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

