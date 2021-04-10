---
title: reserve 命令
description: Reserve 命令會為裝置實例的工作區配置連續的磁碟空間。 數位影片裝置辨識此命令。
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- 保留命令 Windows 多媒體
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933939"
---
# <a name="reserve-command"></a><span data-ttu-id="a77dd-105">reserve 命令</span><span class="sxs-lookup"><span data-stu-id="a77dd-105">reserve command</span></span>

<span data-ttu-id="a77dd-106">Reserve 命令會為裝置實例的工作區配置連續的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="a77dd-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="a77dd-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="a77dd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a77dd-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="a77dd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a77dd-109">參數</span><span class="sxs-lookup"><span data-stu-id="a77dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a77dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a77dd-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a77dd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a77dd-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="a77dd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a77dd-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span><span class="sxs-lookup"><span data-stu-id="a77dd-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="a77dd-114">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="a77dd-114">One or more of the following flags.</span></span>



| <span data-ttu-id="a77dd-115">值</span><span class="sxs-lookup"><span data-stu-id="a77dd-115">Value</span></span>           | <span data-ttu-id="a77dd-116">意義</span><span class="sxs-lookup"><span data-stu-id="a77dd-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77dd-117">在 *路徑* 中</span><span class="sxs-lookup"><span data-stu-id="a77dd-117">in *path*</span></span>       | <span data-ttu-id="a77dd-118">指定磁片磁碟機和目錄路徑 (但不是用來保存記錄資料之暫存檔案的名稱) 。</span><span class="sxs-lookup"><span data-stu-id="a77dd-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="a77dd-119">此檔案的名稱是由裝置所指定。</span><span class="sxs-lookup"><span data-stu-id="a77dd-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="a77dd-120">當裝置關閉時，就會刪除暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="a77dd-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="a77dd-121">如果省略此旗標，則裝置會指定磁碟空間的位置。</span><span class="sxs-lookup"><span data-stu-id="a77dd-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a77dd-122">大小 *持續時間*</span><span class="sxs-lookup"><span data-stu-id="a77dd-122">size *duration*</span></span> | <span data-ttu-id="a77dd-123">指定要在工作區中保留的大約磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="a77dd-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="a77dd-124">*Duration* 值是以目前時間格式指定。</span><span class="sxs-lookup"><span data-stu-id="a77dd-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="a77dd-125">裝置會以下列參數為所需磁碟空間的估計值：要求的時間、檔案格式、影片和音訊壓縮演算法，以及作用中的壓縮品質值。</span><span class="sxs-lookup"><span data-stu-id="a77dd-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="a77dd-126">如果 [setvideo](setvideo.md) "record" 為 "off"，則只會保留音訊的空間。</span><span class="sxs-lookup"><span data-stu-id="a77dd-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="a77dd-127">如果 [setaudio](setaudio.md) "record" 為 "off"，則只會保留影片的空間。</span><span class="sxs-lookup"><span data-stu-id="a77dd-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="a77dd-128">如果兩者都是「關閉」，或 *持續時間* 為零，則不會保留任何空間，而且會解除配置任何現有的保留空間。</span><span class="sxs-lookup"><span data-stu-id="a77dd-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="a77dd-129">如果省略此旗標，裝置將會使用裝置定義的預設值。</span><span class="sxs-lookup"><span data-stu-id="a77dd-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a77dd-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a77dd-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a77dd-131">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="a77dd-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="a77dd-132">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="a77dd-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77dd-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="a77dd-133">Return Value</span></span>

<span data-ttu-id="a77dd-134">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a77dd-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77dd-135">備註</span><span class="sxs-lookup"><span data-stu-id="a77dd-135">Remarks</span></span>

<span data-ttu-id="a77dd-136">如有需要，後續的 [記錄](record.md) 或 [儲存](save.md) 命令會使用這個命令所保留的空間。</span><span class="sxs-lookup"><span data-stu-id="a77dd-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="a77dd-137">如果工作區包含未儲存的資料，資料就會遺失。</span><span class="sxs-lookup"><span data-stu-id="a77dd-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="a77dd-138">有些裝置不需要保留並予以忽略。</span><span class="sxs-lookup"><span data-stu-id="a77dd-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="a77dd-139">如果在錄製之前未保留磁碟空間，則記錄命令會使用裝置特定的預設旗標來執行隱含的保留。</span><span class="sxs-lookup"><span data-stu-id="a77dd-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="a77dd-140">如果您想要更充分掌控磁片配置的發生時間、控制配置多少空間，以及控制磁碟空間的配置位置，請使用明確的保留命令。</span><span class="sxs-lookup"><span data-stu-id="a77dd-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="a77dd-141">您的應用程式可以使用後續的 reserve 命令變更先前保留磁碟空間的數量和位置。</span><span class="sxs-lookup"><span data-stu-id="a77dd-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="a77dd-142">任何已配置且仍未使用的磁碟空間都不會解除配置，直到儲存任何記錄的資料，或直到裝置實例關閉為止。</span><span class="sxs-lookup"><span data-stu-id="a77dd-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77dd-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="a77dd-143">Requirements</span></span>



| <span data-ttu-id="a77dd-144">需求</span><span class="sxs-lookup"><span data-stu-id="a77dd-144">Requirement</span></span> | <span data-ttu-id="a77dd-145">值</span><span class="sxs-lookup"><span data-stu-id="a77dd-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a77dd-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a77dd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a77dd-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77dd-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a77dd-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a77dd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a77dd-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77dd-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a77dd-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a77dd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77dd-151">Mci</span><span class="sxs-lookup"><span data-stu-id="a77dd-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a77dd-152">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="a77dd-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a77dd-153">記錄</span><span class="sxs-lookup"><span data-stu-id="a77dd-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="a77dd-154">儲存</span><span class="sxs-lookup"><span data-stu-id="a77dd-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="a77dd-155">setaudio</span><span class="sxs-lookup"><span data-stu-id="a77dd-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="a77dd-156">setvideo</span><span class="sxs-lookup"><span data-stu-id="a77dd-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

