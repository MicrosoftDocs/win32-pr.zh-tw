---
title: 複製命令
description: Copy 命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- 複製命令 Windows 多媒體
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685657"
---
# <a name="copy-command"></a><span data-ttu-id="7d9bb-105">複製命令</span><span class="sxs-lookup"><span data-stu-id="7d9bb-105">copy command</span></span>

<span data-ttu-id="7d9bb-106">Copy 命令會將資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="7d9bb-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7d9bb-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7d9bb-109">參數</span><span class="sxs-lookup"><span data-stu-id="7d9bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d9bb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7d9bb-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-111">Identifier of an MCI device.</span></span> <span data-ttu-id="7d9bb-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7d9bb-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="7d9bb-114">下列其中一個識別要複製之專案的旗標。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="7d9bb-115">值</span><span class="sxs-lookup"><span data-stu-id="7d9bb-115">Value</span></span>                 | <span data-ttu-id="7d9bb-116">意義</span><span class="sxs-lookup"><span data-stu-id="7d9bb-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9bb-117">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-117">at *rectangle*</span></span>        | <span data-ttu-id="7d9bb-118">指定將複製的每個框架的部分。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="7d9bb-119">如果省略，則預設設定為整個框架。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="7d9bb-120">音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-120">audio stream *stream*</span></span> | <span data-ttu-id="7d9bb-121">指定工作區中受命令影響的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="7d9bb-122">如果您使用此旗標，而且也想要複製影片，您也必須使用「影片串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="7d9bb-123"> (如果未指定任何旗標，則會複製所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="7d9bb-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="7d9bb-124">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-124">from *position*</span></span>       | <span data-ttu-id="7d9bb-125">指定複製的範圍開始。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="7d9bb-126">如果省略，則預設設定為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="7d9bb-127">*定位*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-127">to *position*</span></span>         | <span data-ttu-id="7d9bb-128">指定複製之範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="7d9bb-129">複製的音訊和影片資料是此位置專屬的。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="7d9bb-130">如果省略，則預設設定為工作區的結尾。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="7d9bb-131">影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-131">video stream *stream*</span></span> | <span data-ttu-id="7d9bb-132">在工作區中指定受命令影響的影片串流。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="7d9bb-133">如果您使用此旗標，而且也想要複製音訊，您也必須使用「音訊串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="7d9bb-134"> (如果未指定任何旗標，則會複製所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="7d9bb-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="7d9bb-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7d9bb-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7d9bb-136">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="7d9bb-137">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d9bb-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d9bb-138">Return Value</span></span>

<span data-ttu-id="7d9bb-139">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d9bb-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9bb-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d9bb-140">Requirements</span></span>



| <span data-ttu-id="7d9bb-141">需求</span><span class="sxs-lookup"><span data-stu-id="7d9bb-141">Requirement</span></span> | <span data-ttu-id="7d9bb-142">值</span><span class="sxs-lookup"><span data-stu-id="7d9bb-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d9bb-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d9bb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7d9bb-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d9bb-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7d9bb-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d9bb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7d9bb-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d9bb-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7d9bb-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d9bb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9bb-148">Mci</span><span class="sxs-lookup"><span data-stu-id="7d9bb-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7d9bb-149">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="7d9bb-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

