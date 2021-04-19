---
title: 儲存命令
description: Save 命令會儲存 MCI 檔案。 影片-重迭和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不支援。
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- 儲存命令 Windows 多媒體
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966490"
---
# <a name="save-command"></a><span data-ttu-id="bda6d-106">儲存命令</span><span class="sxs-lookup"><span data-stu-id="bda6d-106">save command</span></span>

<span data-ttu-id="bda6d-107">Save 命令會儲存 MCI 檔案。</span><span class="sxs-lookup"><span data-stu-id="bda6d-107">The save command saves an MCI file.</span></span> <span data-ttu-id="bda6d-108">影片-重迭和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="bda6d-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="bda6d-109">雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不支援。</span><span class="sxs-lookup"><span data-stu-id="bda6d-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="bda6d-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="bda6d-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="bda6d-111">參數</span><span class="sxs-lookup"><span data-stu-id="bda6d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda6d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bda6d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bda6d-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bda6d-113">Identifier of an MCI device.</span></span> <span data-ttu-id="bda6d-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="bda6d-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="bda6d-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span><span class="sxs-lookup"><span data-stu-id="bda6d-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="bda6d-116">旗標，指定要儲存的檔案名，以及選擇性地修改儲存作業的其他旗標。</span><span class="sxs-lookup"><span data-stu-id="bda6d-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="bda6d-117">下表列出可辨識 **儲存** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="bda6d-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="bda6d-118">值</span><span class="sxs-lookup"><span data-stu-id="bda6d-118">Value</span></span>        | <span data-ttu-id="bda6d-119">意義</span><span class="sxs-lookup"><span data-stu-id="bda6d-119">Meaning</span></span>              | <span data-ttu-id="bda6d-120">意義</span><span class="sxs-lookup"><span data-stu-id="bda6d-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="bda6d-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="bda6d-121">digitalvideo</span></span> | <span data-ttu-id="bda6d-122">在 *矩形* 中中止</span><span class="sxs-lookup"><span data-stu-id="bda6d-122">abort at *rectangle*</span></span> | <span data-ttu-id="bda6d-123">*檔案名* keepreserve</span><span class="sxs-lookup"><span data-stu-id="bda6d-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="bda6d-124">overlay</span><span class="sxs-lookup"><span data-stu-id="bda6d-124">overlay</span></span>      | <span data-ttu-id="bda6d-125">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="bda6d-125">at *rectangle*</span></span>       | <span data-ttu-id="bda6d-126">*filename*</span><span class="sxs-lookup"><span data-stu-id="bda6d-126">*filename*</span></span>            |
| <span data-ttu-id="bda6d-127">排序器</span><span class="sxs-lookup"><span data-stu-id="bda6d-127">sequencer</span></span>    | <span data-ttu-id="bda6d-128">*filename*</span><span class="sxs-lookup"><span data-stu-id="bda6d-128">*filename*</span></span>           |                       |
| <span data-ttu-id="bda6d-129">waveaudio</span><span class="sxs-lookup"><span data-stu-id="bda6d-129">waveaudio</span></span>    | <span data-ttu-id="bda6d-130">*filename*</span><span class="sxs-lookup"><span data-stu-id="bda6d-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="bda6d-131">下表列出可在 **lpszFilename** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="bda6d-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="bda6d-132">值</span><span class="sxs-lookup"><span data-stu-id="bda6d-132">Value</span></span>          | <span data-ttu-id="bda6d-133">意義</span><span class="sxs-lookup"><span data-stu-id="bda6d-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda6d-134">abort</span><span class="sxs-lookup"><span data-stu-id="bda6d-134">abort</span></span>          | <span data-ttu-id="bda6d-135">停止進行中的 **儲存** 作業。</span><span class="sxs-lookup"><span data-stu-id="bda6d-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="bda6d-136">如果使用的話，這必須是唯一的專案。</span><span class="sxs-lookup"><span data-stu-id="bda6d-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bda6d-137">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="bda6d-137">at *rectangle*</span></span> | <span data-ttu-id="bda6d-138">指定相對於框架緩衝區來源的矩形。</span><span class="sxs-lookup"><span data-stu-id="bda6d-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="bda6d-139">*矩形* 會指定為 *X1 Y1 X2 Y2*。</span><span class="sxs-lookup"><span data-stu-id="bda6d-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="bda6d-140">座標 *X1 Y1* 指定左上角，而座標 *X2 Y2* 指定寬度和高度。若為數位視訊裝置，則會使用 [capture](capture.md) 命令來捕獲框架緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="bda6d-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="bda6d-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="bda6d-141">*filename*</span></span>     | <span data-ttu-id="bda6d-142">指定要指派給資料檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="bda6d-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="bda6d-143">如果未指定路徑，則會將檔案放在磁片上，並放在先前在明確或隱含 [保留](reserve.md) 命令上指定的目錄中。</span><span class="sxs-lookup"><span data-stu-id="bda6d-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="bda6d-144">如果尚未發出 **保留** ，則預設磁片磁碟機和目錄是與應用程式工作相關聯的磁片磁碟機和目錄。</span><span class="sxs-lookup"><span data-stu-id="bda6d-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="bda6d-145">如果指定路徑，則裝置可能會要求它位於明確或隱含 **保留** 所指定的磁片磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="bda6d-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="bda6d-146">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="bda6d-146">This flag is required.</span></span> |
| <span data-ttu-id="bda6d-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="bda6d-147">keepreserve</span></span>    | <span data-ttu-id="bda6d-148">指定從原始 **保留** 命令剩餘未使用的磁碟空間未解除配置。</span><span class="sxs-lookup"><span data-stu-id="bda6d-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="bda6d-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="bda6d-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bda6d-150">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="bda6d-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="bda6d-151">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="bda6d-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="bda6d-152">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="bda6d-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda6d-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="bda6d-153">Return Value</span></span>

<span data-ttu-id="bda6d-154">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bda6d-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda6d-155">備註</span><span class="sxs-lookup"><span data-stu-id="bda6d-155">Remarks</span></span>

<span data-ttu-id="bda6d-156">如果裝置是使用「新的」裝置識別碼來開啟，則需要 *filename* 變數。</span><span class="sxs-lookup"><span data-stu-id="bda6d-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="bda6d-157">範例</span><span class="sxs-lookup"><span data-stu-id="bda6d-157">Examples</span></span>

<span data-ttu-id="bda6d-158">下列命令會將整個影片緩衝區儲存至名為 VCAPFILE 的檔案。Tga。</span><span class="sxs-lookup"><span data-stu-id="bda6d-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="bda6d-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="bda6d-159">Requirements</span></span>



| <span data-ttu-id="bda6d-160">需求</span><span class="sxs-lookup"><span data-stu-id="bda6d-160">Requirement</span></span> | <span data-ttu-id="bda6d-161">值</span><span class="sxs-lookup"><span data-stu-id="bda6d-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bda6d-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bda6d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bda6d-163">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda6d-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bda6d-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bda6d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bda6d-165">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda6d-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bda6d-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bda6d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda6d-167">Mci</span><span class="sxs-lookup"><span data-stu-id="bda6d-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bda6d-168">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="bda6d-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="bda6d-169">捕獲</span><span class="sxs-lookup"><span data-stu-id="bda6d-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="bda6d-170">儲備</span><span class="sxs-lookup"><span data-stu-id="bda6d-170">reserve</span></span>](reserve.md)
</dt> </dl>

 

