---
title: 剪下命令
description: 剪下的命令會從工作區中移除資料，並將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- 剪下命令 Windows 多媒體
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934883"
---
# <a name="cut-command"></a><span data-ttu-id="39c92-105">剪下命令</span><span class="sxs-lookup"><span data-stu-id="39c92-105">cut command</span></span>

<span data-ttu-id="39c92-106">剪下的命令會從工作區中移除資料，並將資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="39c92-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="39c92-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="39c92-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="39c92-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="39c92-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="39c92-109">參數</span><span class="sxs-lookup"><span data-stu-id="39c92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c92-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="39c92-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="39c92-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39c92-111">Identifier of an MCI device.</span></span> <span data-ttu-id="39c92-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="39c92-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="39c92-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="39c92-114">下列其中一個識別要剪下之專案的旗標。</span><span class="sxs-lookup"><span data-stu-id="39c92-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="39c92-115">值</span><span class="sxs-lookup"><span data-stu-id="39c92-115">Value</span></span>                 | <span data-ttu-id="39c92-116">意義</span><span class="sxs-lookup"><span data-stu-id="39c92-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c92-117">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="39c92-117">at *rectangle*</span></span>        | <span data-ttu-id="39c92-118">指定每個框架剪下的部分。</span><span class="sxs-lookup"><span data-stu-id="39c92-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="39c92-119">如果省略，則會預設為整個框架。</span><span class="sxs-lookup"><span data-stu-id="39c92-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="39c92-120">指定此專案時，不會刪除畫面格。</span><span class="sxs-lookup"><span data-stu-id="39c92-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="39c92-121">而是矩形內的區域會變成黑色。</span><span class="sxs-lookup"><span data-stu-id="39c92-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="39c92-122">音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="39c92-122">audio stream *stream*</span></span> | <span data-ttu-id="39c92-123">指定工作區中受命令影響的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="39c92-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="39c92-124">如果您使用此旗標，而且也想要剪下影片，您也必須使用「影片串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="39c92-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="39c92-125"> (如果未指定任何旗標，則會剪下所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="39c92-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="39c92-126">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="39c92-126">from *position*</span></span>       | <span data-ttu-id="39c92-127">指定剪下的範圍開始。</span><span class="sxs-lookup"><span data-stu-id="39c92-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="39c92-128">如果省略，則會預設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="39c92-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="39c92-129">*定位*</span><span class="sxs-lookup"><span data-stu-id="39c92-129">to *position*</span></span>         | <span data-ttu-id="39c92-130">指定剪下的範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="39c92-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="39c92-131">音訊和影片資料剪下是此位置專屬的。</span><span class="sxs-lookup"><span data-stu-id="39c92-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="39c92-132">如果省略，則會預設為工作區的結尾。</span><span class="sxs-lookup"><span data-stu-id="39c92-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="39c92-133">影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="39c92-133">video stream *stream*</span></span> | <span data-ttu-id="39c92-134">在工作區中指定受命令影響的影片串流。</span><span class="sxs-lookup"><span data-stu-id="39c92-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="39c92-135">如果您使用此旗標，而且也想要剪下音訊，您也必須使用「音訊串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="39c92-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="39c92-136"> (如果未指定任何旗標，則會剪下所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="39c92-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="39c92-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="39c92-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="39c92-138">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="39c92-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="39c92-139">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="39c92-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c92-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="39c92-140">Return Value</span></span>

<span data-ttu-id="39c92-141">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="39c92-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c92-142">備註</span><span class="sxs-lookup"><span data-stu-id="39c92-142">Remarks</span></span>

<span data-ttu-id="39c92-143">只有在明確儲存資料時，變更才會變成永久;不過，播放的行為就如同已移除資料一樣。</span><span class="sxs-lookup"><span data-stu-id="39c92-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c92-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="39c92-144">Requirements</span></span>



| <span data-ttu-id="39c92-145">需求</span><span class="sxs-lookup"><span data-stu-id="39c92-145">Requirement</span></span> | <span data-ttu-id="39c92-146">值</span><span class="sxs-lookup"><span data-stu-id="39c92-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="39c92-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39c92-147">Minimum supported client</span></span><br/> | <span data-ttu-id="39c92-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c92-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39c92-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39c92-149">Minimum supported server</span></span><br/> | <span data-ttu-id="39c92-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c92-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="39c92-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39c92-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c92-152">Mci</span><span class="sxs-lookup"><span data-stu-id="39c92-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39c92-153">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="39c92-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

