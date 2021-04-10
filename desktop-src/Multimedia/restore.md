---
title: restore 命令
description: Restore 命令會從檔案將靜止影像複製到框架緩衝區。 這是 capture 命令的反向。 數位影片裝置辨識此命令。
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- 還原命令 Windows 多媒體
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933940"
---
# <a name="restore-command"></a><span data-ttu-id="7de3f-106">restore 命令</span><span class="sxs-lookup"><span data-stu-id="7de3f-106">restore command</span></span>

<span data-ttu-id="7de3f-107">Restore 命令會從檔案將靜止影像複製到框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7de3f-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="7de3f-108">這是 [capture](capture.md) 命令的反向。</span><span class="sxs-lookup"><span data-stu-id="7de3f-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="7de3f-109">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="7de3f-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7de3f-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7de3f-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7de3f-111">參數</span><span class="sxs-lookup"><span data-stu-id="7de3f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de3f-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7de3f-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7de3f-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de3f-113">Identifier of an MCI device.</span></span> <span data-ttu-id="7de3f-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="7de3f-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7de3f-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span><span class="sxs-lookup"><span data-stu-id="7de3f-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="7de3f-116">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="7de3f-116">One or more of the following flags.</span></span>



| <span data-ttu-id="7de3f-117">值</span><span class="sxs-lookup"><span data-stu-id="7de3f-117">Value</span></span>           | <span data-ttu-id="7de3f-118">意義</span><span class="sxs-lookup"><span data-stu-id="7de3f-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de3f-119">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="7de3f-119">at *rectangle*</span></span>  | <span data-ttu-id="7de3f-120">指定相對於框架緩衝區來源的矩形。</span><span class="sxs-lookup"><span data-stu-id="7de3f-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="7de3f-121">*矩形* 會指定為 *X1 Y1 X2 Y2*。</span><span class="sxs-lookup"><span data-stu-id="7de3f-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="7de3f-122">座標 *X1 Y1* 指定左上角，而座標 *X2 Y2* 指定寬度和高度。如果未使用此旗標，則會將影像複製到框架緩衝區的左上角。</span><span class="sxs-lookup"><span data-stu-id="7de3f-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="7de3f-123">從 *檔案名*</span><span class="sxs-lookup"><span data-stu-id="7de3f-123">from *filename*</span></span> | <span data-ttu-id="7de3f-124">指定要重新叫用的映射檔案名。</span><span class="sxs-lookup"><span data-stu-id="7de3f-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="7de3f-125">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="7de3f-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="7de3f-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7de3f-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7de3f-127">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="7de3f-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="7de3f-128">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="7de3f-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de3f-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="7de3f-129">Return Value</span></span>

<span data-ttu-id="7de3f-130">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7de3f-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7de3f-131">備註</span><span class="sxs-lookup"><span data-stu-id="7de3f-131">Remarks</span></span>

<span data-ttu-id="7de3f-132">裝置可辨識各種不同的影像格式;Windows 裝置獨立點陣圖一律會被辨識。</span><span class="sxs-lookup"><span data-stu-id="7de3f-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de3f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7de3f-133">Requirements</span></span>



| <span data-ttu-id="7de3f-134">需求</span><span class="sxs-lookup"><span data-stu-id="7de3f-134">Requirement</span></span> | <span data-ttu-id="7de3f-135">值</span><span class="sxs-lookup"><span data-stu-id="7de3f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7de3f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7de3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7de3f-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7de3f-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7de3f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7de3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7de3f-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7de3f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7de3f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7de3f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de3f-141">Mci</span><span class="sxs-lookup"><span data-stu-id="7de3f-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7de3f-142">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="7de3f-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7de3f-143">捕獲</span><span class="sxs-lookup"><span data-stu-id="7de3f-143">capture</span></span>](capture.md)
</dt> </dl>

 

