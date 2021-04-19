---
title: quality 命令
description: Quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- 品質命令 Windows 多媒體
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970001"
---
# <a name="quality-command"></a><span data-ttu-id="add22-105">quality 命令</span><span class="sxs-lookup"><span data-stu-id="add22-105">quality command</span></span>

<span data-ttu-id="add22-106">Quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。</span><span class="sxs-lookup"><span data-stu-id="add22-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="add22-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="add22-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="add22-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="add22-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="add22-109">參數</span><span class="sxs-lookup"><span data-stu-id="add22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add22-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="add22-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="add22-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="add22-111">Identifier of an MCI device.</span></span> <span data-ttu-id="add22-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="add22-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="add22-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span><span class="sxs-lookup"><span data-stu-id="add22-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="add22-114">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="add22-114">One or more of the following flags.</span></span> <span data-ttu-id="add22-115"> (必須有三個旗標「音訊」、「仍」和「影片」的其中一個。 ) </span><span class="sxs-lookup"><span data-stu-id="add22-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="add22-116">值</span><span class="sxs-lookup"><span data-stu-id="add22-116">Value</span></span>                 | <span data-ttu-id="add22-117">意義</span><span class="sxs-lookup"><span data-stu-id="add22-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="add22-118">演算法 *演算法*</span><span class="sxs-lookup"><span data-stu-id="add22-118">algorithm *algorithm*</span></span> | <span data-ttu-id="add22-119">將品質層級與指定的 *演算法* 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="add22-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="add22-120">裝置必須支援此 *演算法* ，且必須與使用的「音訊」、「仍」或「影片」旗標相容。</span><span class="sxs-lookup"><span data-stu-id="add22-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="add22-121">如果省略，則會使用目前的演算法。</span><span class="sxs-lookup"><span data-stu-id="add22-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="add22-122">音訊 *名稱*</span><span class="sxs-lookup"><span data-stu-id="add22-122">audio *name*</span></span>          | <span data-ttu-id="add22-123">指出此命令指定以 *名稱* 識別的「音訊」品質層級。</span><span class="sxs-lookup"><span data-stu-id="add22-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="add22-124">對話</span><span class="sxs-lookup"><span data-stu-id="add22-124">dialog</span></span>                | <span data-ttu-id="add22-125">要求裝置顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="add22-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="add22-126">此對話方塊具有演算法特定欄位，這些欄位會由裝置在內部使用，以建立描述特定品質層級的結構。</span><span class="sxs-lookup"><span data-stu-id="add22-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="add22-127">句 *柄*</span><span class="sxs-lookup"><span data-stu-id="add22-127">handle *handle*</span></span>       | <span data-ttu-id="add22-128">指定結構的 *控制碼* ，其中包含描述特定品質層級的演算法特定資料。</span><span class="sxs-lookup"><span data-stu-id="add22-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="add22-129">這個控制碼所參考的資料結構是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="add22-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="add22-130">仍然是 *名稱*</span><span class="sxs-lookup"><span data-stu-id="add22-130">still *name*</span></span>          | <span data-ttu-id="add22-131">表示命令指定以名稱識別的「仍」品質層級 *。*</span><span class="sxs-lookup"><span data-stu-id="add22-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="add22-132">影片 *名稱*</span><span class="sxs-lookup"><span data-stu-id="add22-132">video *name*</span></span>          | <span data-ttu-id="add22-133">表示命令指定以 *名稱* 識別的「影片」品質層級。</span><span class="sxs-lookup"><span data-stu-id="add22-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="add22-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="add22-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="add22-135">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="add22-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="add22-136">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="add22-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add22-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="add22-137">Return Value</span></span>

<span data-ttu-id="add22-138">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="add22-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="add22-139">備註</span><span class="sxs-lookup"><span data-stu-id="add22-139">Remarks</span></span>

<span data-ttu-id="add22-140">此命令會定義品質層級的字串名稱，然後以 [setvideo](setvideo.md) 的「品質」、setvideo 「仍品質」或 [setaudio](setaudio.md) 「品質」命令來建立，以將其建立為目前的影片、靜止或音訊壓縮品質層級。</span><span class="sxs-lookup"><span data-stu-id="add22-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="add22-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="add22-141">Requirements</span></span>



| <span data-ttu-id="add22-142">需求</span><span class="sxs-lookup"><span data-stu-id="add22-142">Requirement</span></span> | <span data-ttu-id="add22-143">值</span><span class="sxs-lookup"><span data-stu-id="add22-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="add22-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="add22-144">Minimum supported client</span></span><br/> | <span data-ttu-id="add22-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="add22-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="add22-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="add22-146">Minimum supported server</span></span><br/> | <span data-ttu-id="add22-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="add22-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="add22-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="add22-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add22-149">Mci</span><span class="sxs-lookup"><span data-stu-id="add22-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="add22-150">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="add22-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="add22-151">setaudio</span><span class="sxs-lookup"><span data-stu-id="add22-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="add22-152">setvideo</span><span class="sxs-lookup"><span data-stu-id="add22-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

