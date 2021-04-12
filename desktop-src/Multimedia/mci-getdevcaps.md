---
title: 'MCI_GETDEVCAPS 命令 (Mmsystem .h) '
description: MCI \_ GETDEVCAPS 命令會捕獲裝置的靜態資訊。
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509419"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="ff28b-104">MCI \_ GETDEVCAPS 命令</span><span class="sxs-lookup"><span data-stu-id="ff28b-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="ff28b-105">MCI \_ GETDEVCAPS 命令會捕獲裝置的靜態資訊。</span><span class="sxs-lookup"><span data-stu-id="ff28b-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="ff28b-106">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="ff28b-106">All devices recognize this command.</span></span> <span data-ttu-id="ff28b-107">適用于此命令的參數和旗標取決於選取的裝置。</span><span class="sxs-lookup"><span data-stu-id="ff28b-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="ff28b-108">資訊會以 *lpCapsParms* 所識別之結構的 **dwReturn** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="ff28b-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="ff28b-109">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="ff28b-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="ff28b-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff28b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ff28b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-112">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff28b-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ff28b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-114">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ff28b-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ff28b-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span><span class="sxs-lookup"><span data-stu-id="ff28b-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-117">[**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ff28b-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff28b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff28b-118">Return Value</span></span>

<span data-ttu-id="ff28b-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff28b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff28b-120">備註</span><span class="sxs-lookup"><span data-stu-id="ff28b-120">Remarks</span></span>

<span data-ttu-id="ff28b-121">下列其他標準和命令特定旗標適用于所有支援 MCI GETDEVCAPS 的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ff28b-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ GETDEVCAPS \_ 複合 \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="ff28b-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-123">如果裝置使用必須明確開啟和關閉的資料儲存體， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI \_ GETDEVCAPS \_ 裝置 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff28b-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-125">**DwReturn** 成員會設定為 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ff28b-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ 有 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="ff28b-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-127">如果裝置有音訊輸出， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ 有 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="ff28b-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-129">如果裝置有影片輸出， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="ff28b-130">例如，針對支援 videodisc 命令集的裝置，此成員會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ GETDEVCAPS \_ 專案</span><span class="sxs-lookup"><span data-stu-id="ff28b-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-132">指定 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)結構的 **dwItem** 成員包含下列其中一個常數：</span><span class="sxs-lookup"><span data-stu-id="ff28b-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 退出</span><span class="sxs-lookup"><span data-stu-id="ff28b-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-134">如果裝置可以退出媒體， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="ff28b-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-136">如果裝置可以播放媒體， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="ff28b-137">如果裝置指定 **為 TRUE**，表示裝置支援 [Mci \_ PAUSE](mci-pause.md) 和 [mci \_ STOP](mci-stop.md) 命令，以及 [mci \_ PLAY](mci-play.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="ff28b-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="ff28b-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-139">如果裝置支援錄製， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="ff28b-140">如果裝置指定 **為 TRUE**，表示裝置支援 mci \_ PAUSE 和 mci \_ STOP 命令，以及 [mci \_ 記錄](mci-record.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="ff28b-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 節省</span><span class="sxs-lookup"><span data-stu-id="ff28b-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-142">如果裝置可以儲存檔案， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ 使用 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="ff28b-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-144">如果裝置需要檔案名， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ff28b-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="ff28b-145">只有複合裝置會使用檔案。</span><span class="sxs-lookup"><span data-stu-id="ff28b-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="ff28b-146">下列旗標可指定于 **digitalvideo** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：</span><span class="sxs-lookup"><span data-stu-id="ff28b-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 凍結</span><span class="sxs-lookup"><span data-stu-id="ff28b-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-148">如果裝置可以凍結畫面格， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="ff28b-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-150">如果裝置可以鎖定， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="ff28b-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-152">如果裝置可以反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以是 \_ STR \_</span><span class="sxs-lookup"><span data-stu-id="ff28b-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-154">如果裝置可以延展輸入， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 延展</span><span class="sxs-lookup"><span data-stu-id="ff28b-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-156">如果裝置可以延展影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 測試</span><span class="sxs-lookup"><span data-stu-id="ff28b-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-158">如果裝置可以執行測試， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ 還在</span><span class="sxs-lookup"><span data-stu-id="ff28b-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-160">如果裝置可以顯示仍是影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS</span><span class="sxs-lookup"><span data-stu-id="ff28b-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-162">**DwReturn** 成員會設定為裝置可同時處理的最大視窗數目。</span><span class="sxs-lookup"><span data-stu-id="ff28b-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ 最大 \_ 速率</span><span class="sxs-lookup"><span data-stu-id="ff28b-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-164">**DwReturn** 成員會設定為裝置的最大播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="ff28b-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ 最低 \_ 費率</span><span class="sxs-lookup"><span data-stu-id="ff28b-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-166">**DwReturn** 成員會設定為裝置的最小播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="ff28b-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI \_ DGV \_ GETDEVCAPS \_ 調色板</span><span class="sxs-lookup"><span data-stu-id="ff28b-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-168">如果裝置可以傳回檔色板控制碼， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="ff28b-169">您可以在適用于 **vcr** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中指定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="ff28b-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ GETDEVCAPS \_ 時鐘 \_ 遞增 \_ 率</span><span class="sxs-lookup"><span data-stu-id="ff28b-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-171">**DwReturn** 成員會設定為每秒的遞增數目。</span><span class="sxs-lookup"><span data-stu-id="ff28b-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以偵測 \_ 到 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="ff28b-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-173">如果裝置能夠偵測媒體的長度， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 凍結</span><span class="sxs-lookup"><span data-stu-id="ff28b-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-175">如果裝置能夠凍結輸出影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 監視 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="ff28b-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-177">如果裝置能夠監視來源， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以預先進行 \_</span><span class="sxs-lookup"><span data-stu-id="ff28b-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-179">如果裝置可以預先進行， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 預覽</span><span class="sxs-lookup"><span data-stu-id="ff28b-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-181">如果裝置能夠進行預覽， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="ff28b-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-183">如果裝置能夠反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 測試</span><span class="sxs-lookup"><span data-stu-id="ff28b-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-185">如果裝置能夠測試， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ 有 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="ff28b-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-187">如果裝置支援外部時鐘， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ 有時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="ff28b-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-189">如果裝置具有時間碼功能或這項功能未知， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ GETDEVCAPS \_ \_ 標記數目 \_</span><span class="sxs-lookup"><span data-stu-id="ff28b-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-191">**DwReturn** 成員會設定為 (99) 的標記數目。</span><span class="sxs-lookup"><span data-stu-id="ff28b-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ GETDEVCAPS \_ 搜尋 \_ 精確度</span><span class="sxs-lookup"><span data-stu-id="ff28b-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-193">**DwReturn** 成員會設定為裝置的搜尋精確度。</span><span class="sxs-lookup"><span data-stu-id="ff28b-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="ff28b-194">下列旗標可在「 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中，針對重 **迭裝置類型** 指定：</span><span class="sxs-lookup"><span data-stu-id="ff28b-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ 可以 \_ 凍結</span><span class="sxs-lookup"><span data-stu-id="ff28b-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-196">如果裝置可以凍結映射， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ 可以 \_ 延展</span><span class="sxs-lookup"><span data-stu-id="ff28b-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-198">如果裝置可以延展影像以填滿框架， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS</span><span class="sxs-lookup"><span data-stu-id="ff28b-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-200">**DwReturn** 成員會設定為裝置可同時處理的最大視窗數目。</span><span class="sxs-lookup"><span data-stu-id="ff28b-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="ff28b-201">下列旗標可指定于 **videodisc** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：</span><span class="sxs-lookup"><span data-stu-id="ff28b-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ 可以 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="ff28b-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-203">如果 videodisc 播放程式可以反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ff28b-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="ff28b-204">有些玩家可以反向播放 CLV 光碟以及 CAV 光碟。</span><span class="sxs-lookup"><span data-stu-id="ff28b-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV</span><span class="sxs-lookup"><span data-stu-id="ff28b-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-206">與其他專案結合時，會指定傳回信息適用于 CAV 格式 videodiscs。</span><span class="sxs-lookup"><span data-stu-id="ff28b-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="ff28b-207">如果未插入任何 videodisc，則這是預設值。</span><span class="sxs-lookup"><span data-stu-id="ff28b-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV</span><span class="sxs-lookup"><span data-stu-id="ff28b-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-209">與其他專案結合時，會指定傳回信息適用于 CLV 格式 videodiscs。</span><span class="sxs-lookup"><span data-stu-id="ff28b-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ RATE</span><span class="sxs-lookup"><span data-stu-id="ff28b-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-211">**DwReturn** 成員會設定為每秒畫面格的標準快速播放速率。</span><span class="sxs-lookup"><span data-stu-id="ff28b-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ 一般 \_ 費率</span><span class="sxs-lookup"><span data-stu-id="ff28b-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-213">**DwReturn** 成員會設定為每秒畫面格的正常播放速率。</span><span class="sxs-lookup"><span data-stu-id="ff28b-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ 低速 \_ 率</span><span class="sxs-lookup"><span data-stu-id="ff28b-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-215">**DwReturn** 成員會設定為每秒畫面格的標準慢速播放速率。</span><span class="sxs-lookup"><span data-stu-id="ff28b-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="ff28b-216">下列旗標可指定于 **waveaudio** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：</span><span class="sxs-lookup"><span data-stu-id="ff28b-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ff28b-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI \_ WAVE \_ GETDEVCAPS \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="ff28b-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-218">**DwReturn** 成員會設定為錄製) 裝置 (的波形輸入總數。</span><span class="sxs-lookup"><span data-stu-id="ff28b-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="ff28b-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI \_ WAVE \_ GETDEVCAPS \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="ff28b-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="ff28b-220">**DwReturn** 成員會設定為 (播放) 裝置的波形輸出總數。</span><span class="sxs-lookup"><span data-stu-id="ff28b-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff28b-221">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff28b-221">Requirements</span></span>



| <span data-ttu-id="ff28b-222">需求</span><span class="sxs-lookup"><span data-stu-id="ff28b-222">Requirement</span></span> | <span data-ttu-id="ff28b-223">值</span><span class="sxs-lookup"><span data-stu-id="ff28b-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff28b-224">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff28b-224">Minimum supported client</span></span><br/> | <span data-ttu-id="ff28b-225">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff28b-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff28b-226">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff28b-226">Minimum supported server</span></span><br/> | <span data-ttu-id="ff28b-227">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff28b-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff28b-228">標頭</span><span class="sxs-lookup"><span data-stu-id="ff28b-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff28b-229"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ff28b-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff28b-230">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff28b-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff28b-231">Mci</span><span class="sxs-lookup"><span data-stu-id="ff28b-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ff28b-232">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="ff28b-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

