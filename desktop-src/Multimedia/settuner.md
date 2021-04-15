---
title: settuner 命令
description: Settuner 命令會變更目前的調諧器或目前調諧器的通道設定。 VCR 裝置會辨識此命令。
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- settuner 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467076"
---
# <a name="settuner-command"></a><span data-ttu-id="29cd8-105">settuner 命令</span><span class="sxs-lookup"><span data-stu-id="29cd8-105">settuner command</span></span>

<span data-ttu-id="29cd8-106">Settuner 命令會變更目前的調諧器或目前調諧器的通道設定。</span><span class="sxs-lookup"><span data-stu-id="29cd8-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="29cd8-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="29cd8-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="29cd8-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="29cd8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="29cd8-109">參數</span><span class="sxs-lookup"><span data-stu-id="29cd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29cd8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="29cd8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="29cd8-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="29cd8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="29cd8-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="29cd8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="29cd8-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span><span class="sxs-lookup"><span data-stu-id="29cd8-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="29cd8-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="29cd8-114">One of the following flags.</span></span>



| <span data-ttu-id="29cd8-115">值</span><span class="sxs-lookup"><span data-stu-id="29cd8-115">Value</span></span>                            | <span data-ttu-id="29cd8-116">意義</span><span class="sxs-lookup"><span data-stu-id="29cd8-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29cd8-117">通道 *通道*</span><span class="sxs-lookup"><span data-stu-id="29cd8-117">channel *channel*</span></span>                | <span data-ttu-id="29cd8-118">將調諧器設定為 *頻道*。</span><span class="sxs-lookup"><span data-stu-id="29cd8-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="29cd8-119">根據 VCR，您可能無法在錄製時變更通道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="29cd8-120">大於最大通道的通道會將調諧器設定為最大頻道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="29cd8-121">頻道搜尋 upchannel 向下搜尋</span><span class="sxs-lookup"><span data-stu-id="29cd8-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="29cd8-122">使用有效的信號搜尋下一個通道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="29cd8-123">「搜尋」會在其搜尋中遞增頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="29cd8-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="29cd8-124">「向下搜尋」會在其搜尋中遞減頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="29cd8-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="29cd8-125">當超過最大頻道數目時，調諧器會換行至頻道1。</span><span class="sxs-lookup"><span data-stu-id="29cd8-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="29cd8-126">同樣地，當向下搜尋時，調諧器會換行到最大頻道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="29cd8-127">頻道 upchannel 向下</span><span class="sxs-lookup"><span data-stu-id="29cd8-127">channel upchannel down</span></span>           | <span data-ttu-id="29cd8-128">將調諧器頻道遞增或遞減。</span><span class="sxs-lookup"><span data-stu-id="29cd8-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="29cd8-129">根據 VCR，您可能無法在錄製時變更通道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="29cd8-130">當超過最大頻道數目時，調諧器會換行至頻道1。</span><span class="sxs-lookup"><span data-stu-id="29cd8-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="29cd8-131">同樣地，當向下搜尋時，調諧器會換行到最大頻道。</span><span class="sxs-lookup"><span data-stu-id="29cd8-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="29cd8-132">編號</span><span class="sxs-lookup"><span data-stu-id="29cd8-132">number *number*</span></span>                  | <span data-ttu-id="29cd8-133">指定要受 settuner 命令影響的調諧器。</span><span class="sxs-lookup"><span data-stu-id="29cd8-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="29cd8-134">如果未指定 *數位* ，則會假設為預設值1。</span><span class="sxs-lookup"><span data-stu-id="29cd8-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="29cd8-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="29cd8-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="29cd8-136">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="29cd8-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="29cd8-137">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="29cd8-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29cd8-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="29cd8-138">Return Value</span></span>

<span data-ttu-id="29cd8-139">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="29cd8-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="29cd8-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="29cd8-140">Requirements</span></span>



| <span data-ttu-id="29cd8-141">需求</span><span class="sxs-lookup"><span data-stu-id="29cd8-141">Requirement</span></span> | <span data-ttu-id="29cd8-142">值</span><span class="sxs-lookup"><span data-stu-id="29cd8-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="29cd8-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29cd8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="29cd8-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29cd8-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="29cd8-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29cd8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="29cd8-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29cd8-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="29cd8-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29cd8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29cd8-148">Mci</span><span class="sxs-lookup"><span data-stu-id="29cd8-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="29cd8-149">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="29cd8-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

