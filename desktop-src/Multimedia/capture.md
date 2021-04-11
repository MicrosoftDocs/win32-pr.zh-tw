---
title: capture 命令
description: Capture 命令會複製框架緩衝區的內容，並將其儲存在指定的檔案中。 數位影片裝置辨識此命令。
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- 捕捉命令 Windows 多媒體
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105918"
---
# <a name="capture-command"></a><span data-ttu-id="6857d-105">capture 命令</span><span class="sxs-lookup"><span data-stu-id="6857d-105">capture command</span></span>

<span data-ttu-id="6857d-106">Capture 命令會複製框架緩衝區的內容，並將其儲存在指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="6857d-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="6857d-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6857d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6857d-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6857d-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6857d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6857d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6857d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6857d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6857d-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6857d-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6857d-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="6857d-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6857d-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span><span class="sxs-lookup"><span data-stu-id="6857d-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="6857d-114">下列其中一個或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="6857d-114">One or more of the following flags:</span></span>



| <span data-ttu-id="6857d-115">值</span><span class="sxs-lookup"><span data-stu-id="6857d-115">Value</span></span>          | <span data-ttu-id="6857d-116">意義</span><span class="sxs-lookup"><span data-stu-id="6857d-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6857d-117">as *路徑名稱*</span><span class="sxs-lookup"><span data-stu-id="6857d-117">as *pathname*</span></span>  | <span data-ttu-id="6857d-118">指定所捕獲映射的目的地路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="6857d-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="6857d-119">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="6857d-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="6857d-120">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="6857d-120">at *rectangle*</span></span> | <span data-ttu-id="6857d-121">指定框架緩衝區內裝置裁切並儲存至磁片的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="6857d-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="6857d-122">如果省略，則裁剪的區域預設為此裝置實例先前 [放置](put.md) "source" 命令上指定或預設的矩形。</span><span class="sxs-lookup"><span data-stu-id="6857d-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6857d-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6857d-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6857d-124">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="6857d-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6857d-125">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6857d-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6857d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="6857d-126">Return Value</span></span>

<span data-ttu-id="6857d-127">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6857d-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6857d-128">備註</span><span class="sxs-lookup"><span data-stu-id="6857d-128">Remarks</span></span>

<span data-ttu-id="6857d-129">如果裝置目前現正播放運動影片，或執行其他需要大量資源的作業，此命令可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="6857d-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="6857d-130">如果框架緩衝區正在即時更新，則更新會短暫暫停，以便捕獲完整的映射。</span><span class="sxs-lookup"><span data-stu-id="6857d-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="6857d-131">如果裝置暫停更新，可能會有視覺效果或聲音效果。</span><span class="sxs-lookup"><span data-stu-id="6857d-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="6857d-132">如果檔案格式、壓縮演算法和品質層級尚未設定，則會使用其預設值。</span><span class="sxs-lookup"><span data-stu-id="6857d-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6857d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6857d-133">Requirements</span></span>



| <span data-ttu-id="6857d-134">需求</span><span class="sxs-lookup"><span data-stu-id="6857d-134">Requirement</span></span> | <span data-ttu-id="6857d-135">值</span><span class="sxs-lookup"><span data-stu-id="6857d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6857d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6857d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6857d-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6857d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6857d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6857d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6857d-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6857d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6857d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6857d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6857d-141">Mci</span><span class="sxs-lookup"><span data-stu-id="6857d-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6857d-142">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="6857d-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6857d-143">把</span><span class="sxs-lookup"><span data-stu-id="6857d-143">put</span></span>](put.md)
</dt> </dl>

 

