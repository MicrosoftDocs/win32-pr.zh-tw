---
title: 'MCI_SETTUNER 命令 (Mmsystem .h) '
description: MCI \_ SETTUNER 命令會設定調諧器上的目前通道。 VCR 裝置會辨識此命令。
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025473"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="21b6a-105">MCI \_ SETTUNER 命令</span><span class="sxs-lookup"><span data-stu-id="21b6a-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="21b6a-106">MCI \_ SETTUNER 命令會設定調諧器上的目前通道。</span><span class="sxs-lookup"><span data-stu-id="21b6a-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="21b6a-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="21b6a-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="21b6a-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="21b6a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="21b6a-109">參數</span><span class="sxs-lookup"><span data-stu-id="21b6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b6a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="21b6a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="21b6a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="21b6a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="21b6a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="21b6a-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="21b6a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span><span class="sxs-lookup"><span data-stu-id="21b6a-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-116">[**MCI \_ VCR \_ SETTUNER \_ PARMS**](mci-vcr-settuner-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="21b6a-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b6a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="21b6a-117">Return Value</span></span>

<span data-ttu-id="21b6a-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="21b6a-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="21b6a-119">備註</span><span class="sxs-lookup"><span data-stu-id="21b6a-119">Remarks</span></span>

<span data-ttu-id="21b6a-120">下列其他旗標適用于 VCR 裝置：</span><span class="sxs-lookup"><span data-stu-id="21b6a-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="21b6a-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI \_ VCR \_ SETTUNER \_ 通道</span><span class="sxs-lookup"><span data-stu-id="21b6a-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-122">由 *lpSetTuner* 所識別之結構的 **dwChannel** 成員包含新的頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="21b6a-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI \_ VCR \_ SETTUNER \_ 頻道 \_ 關閉</span><span class="sxs-lookup"><span data-stu-id="21b6a-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-124">遞減調諧器頻道。</span><span class="sxs-lookup"><span data-stu-id="21b6a-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI \_ VCR \_ SETTUNER \_ 通道 \_ \_ 向下搜尋</span><span class="sxs-lookup"><span data-stu-id="21b6a-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-126">以反向方向搜尋有效的通道。</span><span class="sxs-lookup"><span data-stu-id="21b6a-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI \_ VCR \_ SETTUNER \_ 通道 \_ 搜尋 \_</span><span class="sxs-lookup"><span data-stu-id="21b6a-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-128">以正向方向搜尋有效的通道。</span><span class="sxs-lookup"><span data-stu-id="21b6a-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ UP</span><span class="sxs-lookup"><span data-stu-id="21b6a-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-130">遞增調諧器頻道。</span><span class="sxs-lookup"><span data-stu-id="21b6a-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="21b6a-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI \_ VCR \_ SETTUNER \_ 號碼</span><span class="sxs-lookup"><span data-stu-id="21b6a-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="21b6a-132">*LpSetTuner* 所識別之結構的 **dwNumber** 成員會指定要使用此命令影響的邏輯調諧器。</span><span class="sxs-lookup"><span data-stu-id="21b6a-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21b6a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="21b6a-133">Requirements</span></span>



| <span data-ttu-id="21b6a-134">需求</span><span class="sxs-lookup"><span data-stu-id="21b6a-134">Requirement</span></span> | <span data-ttu-id="21b6a-135">值</span><span class="sxs-lookup"><span data-stu-id="21b6a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b6a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21b6a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21b6a-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21b6a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="21b6a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21b6a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21b6a-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21b6a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="21b6a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="21b6a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b6a-141"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="21b6a-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b6a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21b6a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b6a-143">Mci</span><span class="sxs-lookup"><span data-stu-id="21b6a-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="21b6a-144">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="21b6a-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

