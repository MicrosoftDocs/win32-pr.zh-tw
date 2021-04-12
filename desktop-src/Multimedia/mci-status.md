---
title: 'MCI_STATUS 命令 (Mmsystem .h) '
description: MCI \_ STATUS 命令會抓取有關 MCI 裝置的資訊。 所有裝置都會辨識此命令。 資訊會以 lpStatus 參數所識別之結構的 dwReturn 成員傳回。
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "104321252"
---
# <a name="mci_status-command"></a><span data-ttu-id="f801c-106">MCI \_ 狀態命令</span><span class="sxs-lookup"><span data-stu-id="f801c-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="f801c-107">無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。</span><span class="sxs-lookup"><span data-stu-id="f801c-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="f801c-108">本檔中有 ' 從屬 ' 這個字的參考。</span><span class="sxs-lookup"><span data-stu-id="f801c-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="f801c-109">Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。</span><span class="sxs-lookup"><span data-stu-id="f801c-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="f801c-110">這種用語是用來做為命令內所使用的用語。</span><span class="sxs-lookup"><span data-stu-id="f801c-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="f801c-111">為求一致，本檔包含此字。</span><span class="sxs-lookup"><span data-stu-id="f801c-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="f801c-112">當您在命令中更改這個字時，我們會將此檔修正為一致。</span><span class="sxs-lookup"><span data-stu-id="f801c-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="f801c-113">MCI \_ STATUS 命令會抓取有關 MCI 裝置的資訊。</span><span class="sxs-lookup"><span data-stu-id="f801c-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="f801c-114">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="f801c-114">All devices recognize this command.</span></span> <span data-ttu-id="f801c-115">資訊會以 *lpStatus* 參數所識別之結構的 **dwReturn** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="f801c-116">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="f801c-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f801c-117">參數</span><span class="sxs-lookup"><span data-stu-id="f801c-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f801c-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f801c-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f801c-119">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f801c-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f801c-121">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f801c-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="f801c-122">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="f801c-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f801c-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span><span class="sxs-lookup"><span data-stu-id="f801c-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="f801c-124">[**MCI \_ 狀態 \_ PARMS**](mci-status-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f801c-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="f801c-125">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="f801c-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f801c-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f801c-126">Return Value</span></span>

<span data-ttu-id="f801c-127">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f801c-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f801c-128">備註</span><span class="sxs-lookup"><span data-stu-id="f801c-128">Remarks</span></span>

<span data-ttu-id="f801c-129">下列其他標準和命令特定旗標適用于所有支援 MCI 狀態的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="f801c-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="f801c-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI \_ 狀態 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="f801c-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="f801c-131">指定由 *lpStatus* 所識別之結構的 **dwItem** 成員包含常數，指定要取得的狀態專案。</span><span class="sxs-lookup"><span data-stu-id="f801c-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="f801c-132">下列常數會定義要在結構的 **dwReturn** 成員中傳回的狀態專案：</span><span class="sxs-lookup"><span data-stu-id="f801c-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="f801c-133">MCI \_ 狀態 \_ 目前的 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="f801c-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="f801c-134">**DwReturn** 成員會設定為目前的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="f801c-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="f801c-135">MCI 使用連續的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="f801c-136">MCI \_ 狀態 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="f801c-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="f801c-137">**DwReturn** 成員會設定為媒體總長度。</span><span class="sxs-lookup"><span data-stu-id="f801c-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI \_ 狀態 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f801c-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-139">**DwReturn** 成員會設定為裝置的目前模式。</span><span class="sxs-lookup"><span data-stu-id="f801c-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="f801c-140">這些模式包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="f801c-140">The modes include the following:</span></span>

-   <span data-ttu-id="f801c-141">MCI \_ 模式 \_ 未 \_ 就緒</span><span class="sxs-lookup"><span data-stu-id="f801c-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="f801c-142">MCI \_ 模式 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="f801c-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="f801c-143">MCI \_ 模式 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="f801c-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="f801c-144">MCI \_ 模式 \_ 停止</span><span class="sxs-lookup"><span data-stu-id="f801c-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="f801c-145">\_開啟 MCI 模式 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="f801c-146">MCI \_ 模式 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="f801c-147">MCI \_ 模式 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="f801c-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="f801c-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI \_ 狀態 \_ \_ 追蹤數目 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-149">**DwReturn** 成員會設定為可播放的曲目總數。</span><span class="sxs-lookup"><span data-stu-id="f801c-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI \_ 狀態 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="f801c-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="f801c-151">**DwReturn** 成員會設定為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="f801c-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI \_ 狀態 \_ 就緒</span><span class="sxs-lookup"><span data-stu-id="f801c-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="f801c-153">如果裝置已備妥， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI \_ 狀態 \_ 時間 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="f801c-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-155">**DwReturn** 成員會設定為裝置目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="f801c-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="f801c-156">時間格式包括：</span><span class="sxs-lookup"><span data-stu-id="f801c-156">The time formats include:</span></span>

-   <span data-ttu-id="f801c-157">MCI \_ 格式 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f801c-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="f801c-158">MCI \_ 格式 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="f801c-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="f801c-159">MCI \_ 格式 \_ HMS</span><span class="sxs-lookup"><span data-stu-id="f801c-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="f801c-160">MCI \_ 格式 \_ 毫秒</span><span class="sxs-lookup"><span data-stu-id="f801c-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="f801c-161">MCI \_ 格式 \_ MSF</span><span class="sxs-lookup"><span data-stu-id="f801c-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="f801c-162">MCI \_ 格式 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="f801c-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="f801c-163">MCI \_ 格式 \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="f801c-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="f801c-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI \_ 狀態 \_ 開始</span><span class="sxs-lookup"><span data-stu-id="f801c-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="f801c-165">取得媒體的開始位置。</span><span class="sxs-lookup"><span data-stu-id="f801c-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="f801c-166">若要取得開始位置，請將此旗標與 MCI \_ 狀態專案合併， \_ 並將 *lpStatus* 所識別之結構的 **dwItem** 成員設定為 mci \_ 狀態 \_ 位置。</span><span class="sxs-lookup"><span data-stu-id="f801c-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ 曲目</span><span class="sxs-lookup"><span data-stu-id="f801c-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="f801c-168">指出狀態追蹤參數包含在 *lpStatus* 所識別之結構的 **dwTrack** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f801c-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="f801c-169">您必須使用此旗標搭配 MCI \_ 狀態 \_ 位置或 mci \_ 狀態 \_ 長度常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="f801c-170">搭配 MCI \_ 狀態位置使用時 \_ ，MCI TRACK 會取得 \_ 指定之追蹤的開始位置。搭配 MCI \_ 狀態長度使用時 \_ ，MCI TRACK 會取得指定的 \_ 曲目長度。MCI 使用連續的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-171">下列其他旗標會搭配 **cdaudio** 裝置類型使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="f801c-172">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI \_ CDA \_ 狀態 \_ 類型 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="f801c-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="f801c-174">**DwReturn** 成員會設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f801c-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="f801c-175">MCI \_ CDA \_ 追蹤 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="f801c-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="f801c-176">MCI \_ CDA \_ 追蹤 \_ 其他</span><span class="sxs-lookup"><span data-stu-id="f801c-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="f801c-177">若要使用此旗標， \_ 必須設定 MCI TRACK 旗標，且由 *lpStatus* 所識別之結構的 **dwTrack** 成員必須包含有效的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="f801c-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-179">如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-180">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="f801c-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f801c-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI \_ DGV \_ 狀態 \_ 磁碟空間</span><span class="sxs-lookup"><span data-stu-id="f801c-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-182">由 *lpStatus* 所識別之結構的 **lpstrDrive** 成員會指定磁片磁碟機，或在某些實作為路徑中指定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f801c-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="f801c-183">MCI \_ STATUS 命令會傳回 *lpStatus* 所識別之結構的 **DwReturn** 成員中， [mci \_ RESERVE](mci-reserve.md)命令可取得的大約磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="f801c-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="f801c-184">磁碟空間是以目前時間格式的單位來測量。</span><span class="sxs-lookup"><span data-stu-id="f801c-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI \_ DGV \_ 狀態 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="f801c-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-186">由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至輸入。</span><span class="sxs-lookup"><span data-stu-id="f801c-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>剩餘的 MCI \_ DGV \_ 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-188">由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至左方音訊通道。</span><span class="sxs-lookup"><span data-stu-id="f801c-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV \_ 狀態 \_ 名義</span><span class="sxs-lookup"><span data-stu-id="f801c-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="f801c-190">由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會要求名義值，而不是目前的值。</span><span class="sxs-lookup"><span data-stu-id="f801c-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI \_ DGV \_ 狀態 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="f801c-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-192">由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至輸出。</span><span class="sxs-lookup"><span data-stu-id="f801c-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI \_ DGV \_ 狀態 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-194">針對 [MCI DGV STATUS frame rate] 旗標傳回的畫面播放速率 \_ \_ \_ \_ 是用於壓縮的速率。</span><span class="sxs-lookup"><span data-stu-id="f801c-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI \_ DGV \_ 狀態 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="f801c-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-196">由 *lpStatus* 所識別之結構的 **dwReturn** 成員會傳回最接近 **dwReference** 成員中指定之框架之前的主要畫面格影像。</span><span class="sxs-lookup"><span data-stu-id="f801c-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI \_ DGV \_ STATUS \_ RIGHT</span><span class="sxs-lookup"><span data-stu-id="f801c-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-198">由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至正確的音訊通道。</span><span class="sxs-lookup"><span data-stu-id="f801c-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-199">當   \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，會使用下列常數搭配 lpStatus 參數所指向之結構 dwItem 成員中的 digitalvideo 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI \_ AVI \_ 狀態 \_ 音訊 \_ 中斷</span><span class="sxs-lookup"><span data-stu-id="f801c-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-201">**DwReturn** 成員會傳回最後一個 AVI 序列的音訊部分所中斷的次數。</span><span class="sxs-lookup"><span data-stu-id="f801c-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="f801c-202">當系統嘗試將音訊資料寫入設備磁碟機，併發現該驅動程式已經播放了所有可用的資料時，系統就會計算出一份音訊中斷的次數。</span><span class="sxs-lookup"><span data-stu-id="f801c-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="f801c-203">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>已 \_ \_ 略過 MCI AVI 狀態 \_ 框架 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-205">**DwReturn** 成員會傳回播放最後一個 AVI 序列時未繪製的框架數目。</span><span class="sxs-lookup"><span data-stu-id="f801c-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="f801c-206">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI \_ AVI \_ 狀態 \_ 上次 \_ 播放 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="f801c-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-208">**DwReturn** 成員會傳回一個值，表示最後一個 AVI 序列的實際播放時間與目標播放時間相符的程度。</span><span class="sxs-lookup"><span data-stu-id="f801c-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="f801c-209">值1000表示目標時間和實際時間相同。</span><span class="sxs-lookup"><span data-stu-id="f801c-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="f801c-210">例如，值為2000時，會指出 AVI 序列所花的時間比應該有兩倍的時間。</span><span class="sxs-lookup"><span data-stu-id="f801c-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="f801c-211">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI \_ DGV \_ 狀態 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="f801c-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="f801c-213">**DwReturn** 成員會根據 \_ \_ \_ \_ [mci \_ set](mci-set.md)命令最新的 MCI set AUDIO 選項，將 mci 回傳或 mci OFF。</span><span class="sxs-lookup"><span data-stu-id="f801c-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="f801c-214">\_如果已啟用其中一或兩個喇叭，則會傳回 mci，否則會傳回 mci \_ 。</span><span class="sxs-lookup"><span data-stu-id="f801c-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="f801c-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-216">**DwReturn** 成員會傳回類比音訊信號的近似即時音訊層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="f801c-217">大於1000的值表示有裁剪失真。</span><span class="sxs-lookup"><span data-stu-id="f801c-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="f801c-218">某些裝置只能在錄製音訊時決定此值。</span><span class="sxs-lookup"><span data-stu-id="f801c-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="f801c-219">此狀態值沒有相關聯的 **MCI \_ SET** 或 [mci \_ SETAUDIO](mci-setaudio.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="f801c-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="f801c-220">此值與 WAVE-音訊命令 MCI \_ WAVE \_ 狀態層級相關，但以不同的方式來正規化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f801c-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-222">**DwReturn** 成員會 \_ \_ 依 \_ \_ \_ **mci \_ SETAUDIO** 命令的 mci DGV SETAUDIO 記錄旗標來反映狀態所設定的狀態，以傳回 mci 或 mci。</span><span class="sxs-lookup"><span data-stu-id="f801c-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f801c-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-224">**DwReturn** 成員會傳回目前的音訊數位化器來源：</span><span class="sxs-lookup"><span data-stu-id="f801c-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="f801c-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI \_ DGV \_ SETAUDIO \_ AVERAGE</span><span class="sxs-lookup"><span data-stu-id="f801c-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-226">指定左右音訊頻道的平均值。</span><span class="sxs-lookup"><span data-stu-id="f801c-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ \_ SETAUDIO \_ 剩下的 MCI DGV</span><span class="sxs-lookup"><span data-stu-id="f801c-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-228">指定左聲道。</span><span class="sxs-lookup"><span data-stu-id="f801c-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT</span><span class="sxs-lookup"><span data-stu-id="f801c-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-230">指定正確的音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="f801c-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ 身歷聲</span><span class="sxs-lookup"><span data-stu-id="f801c-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="f801c-232">指定身歷聲。</span><span class="sxs-lookup"><span data-stu-id="f801c-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="f801c-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f801c-234">**DwReturn** 成員會傳回目前的音訊資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV \_ 狀態 \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="f801c-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f801c-236">**DwReturn** 成員會傳回每秒用於錄製的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="f801c-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV \_ 狀態 \_ 低音</span><span class="sxs-lookup"><span data-stu-id="f801c-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-238">**DwReturn** 成員會傳回目前的音訊低音等級。</span><span class="sxs-lookup"><span data-stu-id="f801c-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="f801c-239">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI \_ DGV \_ 狀態 \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="f801c-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="f801c-241">**DwReturn** 成員會傳回用於儲存已捕捉或已記錄資料之每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="f801c-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV \_ 狀態 \_ BITSPERSAMPLE</span><span class="sxs-lookup"><span data-stu-id="f801c-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-243">**DwReturn** 成員會傳回裝置用來錄製的每個樣本位數。</span><span class="sxs-lookup"><span data-stu-id="f801c-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="f801c-244">這僅適用于支援 PCM 格式的裝置。</span><span class="sxs-lookup"><span data-stu-id="f801c-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ 狀態 \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="f801c-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="f801c-246">**DwReturn** 成員會傳回相對於輸入波形開頭的資料區塊對齊。</span><span class="sxs-lookup"><span data-stu-id="f801c-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI \_ DGV \_ 狀態 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="f801c-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-248">**DwReturn** 成員會傳回目前的影片亮度等級。</span><span class="sxs-lookup"><span data-stu-id="f801c-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="f801c-249">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI \_ DGV \_ 狀態 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="f801c-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="f801c-251">**DwReturn** 成員會傳回目前的色彩層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="f801c-252">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI \_ DGV \_ 狀態 \_ 對比</span><span class="sxs-lookup"><span data-stu-id="f801c-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="f801c-254">**DwReturn** 成員會傳回目前的對比層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="f801c-255">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ 狀態 \_ >FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="f801c-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-257">**DwReturn** 成員會傳回目前的檔案格式以進行錄製或儲存。</span><span class="sxs-lookup"><span data-stu-id="f801c-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI \_ DGV \_ 狀態 \_ 檔案 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f801c-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-259">**DwReturn** 成員會傳回檔案作業的狀態：</span><span class="sxs-lookup"><span data-stu-id="f801c-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="f801c-260">MCI \_ DGV \_ 檔 \_ 模式 \_ 編輯</span><span class="sxs-lookup"><span data-stu-id="f801c-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="f801c-261">在剪下、複製、刪除、貼上和復原作業期間傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="f801c-262">MCI \_ DGV \_ 檔 \_ 模式 \_ 閒置</span><span class="sxs-lookup"><span data-stu-id="f801c-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="f801c-263">當檔案準備好進行下一項作業時傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="f801c-264">MCI \_ DGV \_ FILE \_ MODE \_ 載入</span><span class="sxs-lookup"><span data-stu-id="f801c-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="f801c-265">在載入檔案時傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="f801c-266">\_正在儲存 MCI DGV \_ 檔 \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="f801c-267">在儲存檔案時傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI \_ DGV \_ 狀態 \_ 檔案 \_ 完成</span><span class="sxs-lookup"><span data-stu-id="f801c-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="f801c-269">**DwReturn** 成員會傳回負載、儲存、捕捉、剪下、複製、刪除、貼上或復原作業進度的估計百分比。</span><span class="sxs-lookup"><span data-stu-id="f801c-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="f801c-270"> (的應用程式可以使用此功能來提供進度的視覺指標。 ) 所有數位視訊裝置都不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI \_ DGV \_ 狀態 \_ 轉寄</span><span class="sxs-lookup"><span data-stu-id="f801c-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-272">如果裝置方向為轉寄或裝置未播放， **dwReturn** 成員會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI \_ DGV \_ STATUS \_ FRAME \_ 速率</span><span class="sxs-lookup"><span data-stu-id="f801c-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-274">**DwReturn** 成員必須搭配 mci \_ DGV \_ 狀態 \_ 名義、mci \_ DGV \_ 狀態 \_ 記錄或兩者一起使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="f801c-275">與 MCI \_ DGV 狀態記錄搭配使用時 \_ \_ ，會傳回目前用來錄製的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f801c-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="f801c-276">搭配使用 MCI \_ DGV \_ 狀態 \_ 記錄和 mci \_ DGV 狀態時 \_ \_ ，會傳回與輸入視訊訊號相關聯的名義畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f801c-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="f801c-277">與 MCI \_ DGV 狀態名義搭配使用時 \_ \_ ，會傳回與檔案相關聯的名義框架費率。</span><span class="sxs-lookup"><span data-stu-id="f801c-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="f801c-278">在所有情況下，單位都是每秒畫面格乘以1000。</span><span class="sxs-lookup"><span data-stu-id="f801c-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI \_ DGV \_ 狀態 \_ GAMMA</span><span class="sxs-lookup"><span data-stu-id="f801c-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="f801c-280">**DwReturn** 成員會傳回目前的 gamma 值。</span><span class="sxs-lookup"><span data-stu-id="f801c-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="f801c-281">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ 狀態 \_ HPAL</span><span class="sxs-lookup"><span data-stu-id="f801c-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="f801c-283">**DwReturn** 成員會傳回目前調色板控制碼的 ASCII 十進位值。</span><span class="sxs-lookup"><span data-stu-id="f801c-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="f801c-284">控制碼包含在傳回值的低序位字中。</span><span class="sxs-lookup"><span data-stu-id="f801c-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI \_ DGV \_ 狀態 \_ HWND</span><span class="sxs-lookup"><span data-stu-id="f801c-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="f801c-286">**DwReturn** 成員會針對與此設備磁碟機實例相關聯的目前明確或預設視窗控制碼，傳回 ASCII 十進位值。</span><span class="sxs-lookup"><span data-stu-id="f801c-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="f801c-287">控制碼包含在傳回值的低序位字中。</span><span class="sxs-lookup"><span data-stu-id="f801c-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI \_ DGV \_ STATUS \_ KEY \_ COLOR</span><span class="sxs-lookup"><span data-stu-id="f801c-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="f801c-289">**DwReturn** 成員會傳回目前的按鍵色彩值。</span><span class="sxs-lookup"><span data-stu-id="f801c-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI \_ DGV \_ STATUS \_ KEY \_ INDEX</span><span class="sxs-lookup"><span data-stu-id="f801c-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="f801c-291">**DwReturn** 成員會傳回目前的索引鍵索引值。</span><span class="sxs-lookup"><span data-stu-id="f801c-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI \_ DGV \_ 狀態 \_ 監視</span><span class="sxs-lookup"><span data-stu-id="f801c-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="f801c-293">**DwReturn** 成員會傳回常數，指出目前簡報的來源。</span><span class="sxs-lookup"><span data-stu-id="f801c-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="f801c-294">以下是定義的常數：</span><span class="sxs-lookup"><span data-stu-id="f801c-294">The following constants are defined:</span></span>

<span data-ttu-id="f801c-295">MCI \_ DGV \_ 監視 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="f801c-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="f801c-296">檔案是來源。</span><span class="sxs-lookup"><span data-stu-id="f801c-296">A file is the source.</span></span>

<span data-ttu-id="f801c-297">MCI \_ DGV \_ 監視 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="f801c-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="f801c-298">輸入為來源。</span><span class="sxs-lookup"><span data-stu-id="f801c-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI \_ DGV \_ STATUS \_ 監視 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="f801c-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-300">**DwReturn** 成員會傳回常數，指出用於輸入監視的方法。</span><span class="sxs-lookup"><span data-stu-id="f801c-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="f801c-301">以下是定義的常數：</span><span class="sxs-lookup"><span data-stu-id="f801c-301">The following constants are defined:</span></span>

<span data-ttu-id="f801c-302">MCI \_ DGV \_ 方法 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="f801c-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="f801c-303">直接輸入監視。</span><span class="sxs-lookup"><span data-stu-id="f801c-303">Direct input monitoring.</span></span>

<span data-ttu-id="f801c-304">MCI \_ DGV \_ 方法 \_ 文章</span><span class="sxs-lookup"><span data-stu-id="f801c-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="f801c-305">輸入後監視。</span><span class="sxs-lookup"><span data-stu-id="f801c-305">Post-input monitoring.</span></span>

<span data-ttu-id="f801c-306">MCI \_ DGV \_ 方法 \_ 預先</span><span class="sxs-lookup"><span data-stu-id="f801c-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="f801c-307">預先輸入監視。</span><span class="sxs-lookup"><span data-stu-id="f801c-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI \_ DGV \_ 狀態 \_ 暫停 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f801c-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-309">如果裝置在播放時暫停， **dwReturn** 成員會傳回 mci \_ 模式 \_ ， \_ 如果裝置在錄製時暫停，則會傳回 mci 模式 \_ 記錄。</span><span class="sxs-lookup"><span data-stu-id="f801c-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="f801c-310">此命令會傳回 MCIERR \_ NONAPPLICABLE 函式， \_ 以在裝置未暫停時傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f801c-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ 狀態 \_ SAMPLESPERSECOND</span><span class="sxs-lookup"><span data-stu-id="f801c-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="f801c-312">**DwReturn** 成員會傳回每秒記錄的樣本數。</span><span class="sxs-lookup"><span data-stu-id="f801c-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV \_ 狀態 \_ \_ 精確搜尋</span><span class="sxs-lookup"><span data-stu-id="f801c-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="f801c-314">**DwReturn** 成員會傳回 **TRUE** 或 **FALSE** ，指出是否已設定搜尋確切格式。</span><span class="sxs-lookup"><span data-stu-id="f801c-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="f801c-315"> (的應用程式可以使用 [mci \_ set](mci-set.md) 命令搭配 mci \_ DGV \_ set \_ SEEK 確切旗標來設定此格式 \_ 。 ) </span><span class="sxs-lookup"><span data-stu-id="f801c-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="f801c-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI \_ DGV \_ 狀態 \_ 清晰度</span><span class="sxs-lookup"><span data-stu-id="f801c-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-317">**DwReturn** 成員會傳回目前的清晰度層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="f801c-318">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI \_ DGV \_ 狀態 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f801c-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-320">**DwReturn** 成員會傳回保留工作區將保留之壓縮資料的大約播放持續時間。</span><span class="sxs-lookup"><span data-stu-id="f801c-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="f801c-321">持續時間單位為目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="f801c-321">The duration units are in the current time format.</span></span> <span data-ttu-id="f801c-322">如果沒有保留的磁碟空間，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f801c-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="f801c-323">傳回的大小為近似值，因為壓縮資料的精確磁碟空間無法在資料壓縮後才進行預測。</span><span class="sxs-lookup"><span data-stu-id="f801c-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI \_ DGV \_ 狀態 \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="f801c-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-325">**DwReturn** 成員會傳回與工作區中目前位置相關聯的 SMPTE 時間碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV \_ 狀態 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="f801c-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-327">**DwReturn** 成員會傳回目前的播放速度。</span><span class="sxs-lookup"><span data-stu-id="f801c-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI \_ DGV \_ 狀態 \_ 仍 \_ >FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="f801c-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-329">**DwReturn** 成員會傳回 [MCI \_ CAPTURE](mci-capture.md)命令的目前檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f801c-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV \_ 狀態 \_ 淡色</span><span class="sxs-lookup"><span data-stu-id="f801c-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-331">**DwReturn** 成員會傳回目前的影片色調層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="f801c-332">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI \_ DGV \_ 狀態 \_ 高音</span><span class="sxs-lookup"><span data-stu-id="f801c-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-334">**DwReturn** 成員會傳回目前的音訊高音層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="f801c-335">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>未儲存的 MCI \_ DGV \_ 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-337">如果工作區中有記錄的資料可能由於 [mci \_ 關閉](mci-close.md)、 [mci \_ 負載](mci-load.md)、 [mci \_ 記錄](mci-record.md)、 [Mci \_ 保留](mci-reserve.md)、 [mci \_ 剪](mci-cut.md)下、mci [ \_ 刪除](mci-delete.md)或 [mci \_ 貼](mci-paste.md)上命令而遺失， **dwReturn** 成員會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="f801c-338">否則，成員會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI \_ DGV \_ 狀態 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="f801c-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="f801c-340"> \_ 如果啟用影片或停用 mci，dwReturn 成員會傳回 mci \_ 。</span><span class="sxs-lookup"><span data-stu-id="f801c-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-342">**DwReturn** 成員會將 mci 回傳 \_ 或 mci \_ OFF，以反映 \_ \_ \_ [mci \_ SETVIDEO](mci-setvideo.md)命令的 mci DGV SETVIDEO 記錄旗標所設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="f801c-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f801c-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-344">**DwReturn** 成員會傳回常數，指出由 \_ \_ \_ **mci \_ SETVIDEO** 命令的 mci DGV SETVIDEO 來源旗標所設定的影片來源類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ SRC \_ NUM</span><span class="sxs-lookup"><span data-stu-id="f801c-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="f801c-346">**DwReturn** 成員會傳回目前作用中的影片輸入來源類型內的數位。</span><span class="sxs-lookup"><span data-stu-id="f801c-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="f801c-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f801c-348">**DwReturn** 成員會傳回目前的視頻串流號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI \_ DGV \_ 狀態 \_ 磁片區</span><span class="sxs-lookup"><span data-stu-id="f801c-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="f801c-350">**DwReturn** 成員會將磁片區的平均值傳回給左邊和右邊的喇叭。</span><span class="sxs-lookup"><span data-stu-id="f801c-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="f801c-351">使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>[MCI \_ DGV \_ 狀態 \_ ] 視窗 \_ 可見</span><span class="sxs-lookup"><span data-stu-id="f801c-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-353">如果視窗不是隱藏的， **dwReturn** 成員會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_ \_ \_ 最小化 MCI DGV 狀態視窗 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-355">如果視窗最小化， **dwReturn** 成員會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_最大化的 MCI DGV \_ 狀態 \_ 視窗 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-357">如果視窗最大化， **dwReturn** 成員會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-359">**DwReturn** 成員會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f801c-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-360">針對數位影片裝置， *lpStatus* 參數會指向 [**MCI \_ DGV \_ STATUS \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="f801c-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="f801c-361">下列其他旗標會搭配 **sequencer** 裝置類型使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="f801c-362">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ SEQ \_ STATUS \_ DIVTYPE</span><span class="sxs-lookup"><span data-stu-id="f801c-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-364">**DwReturn** 成員會設定為下列其中一個值，表示序列的目前除法類型：</span><span class="sxs-lookup"><span data-stu-id="f801c-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="f801c-365">MCI \_ SEQ \_ DIV \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="f801c-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="f801c-366">MCI \_ SEQ \_ DIV （ \_ SMPTE \_ 24）</span><span class="sxs-lookup"><span data-stu-id="f801c-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="f801c-367">MCI \_ SEQ \_ DIV 的 \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="f801c-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="f801c-368">MCI \_ SEQ \_ DIV \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="f801c-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="f801c-369">MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="f801c-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="f801c-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI \_ SEQ \_ 狀態 \_ 主機</span><span class="sxs-lookup"><span data-stu-id="f801c-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-371">**DwReturn** 成員會設定為主要作業所使用的同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI \_ SEQ \_ 狀態 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="f801c-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="f801c-373">**DwReturn** 成員會設定為序列的目前 SMPTE 位移。</span><span class="sxs-lookup"><span data-stu-id="f801c-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI \_ SEQ \_ 狀態 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="f801c-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-375">**DwReturn** 成員會設定為序列所使用之目前埠的 MIDI 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ SEQ \_ 狀態 \_ 從屬</span><span class="sxs-lookup"><span data-stu-id="f801c-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-377">**DwReturn** 成員會設定為用於從屬作業的同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI \_ SEQ \_ STATUS \_ 節奏</span><span class="sxs-lookup"><span data-stu-id="f801c-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="f801c-379">**DwReturn** 成員會設定為 PPQN 檔案在每分鐘的每分鐘的最新節奏，或每秒的每秒畫面格數。</span><span class="sxs-lookup"><span data-stu-id="f801c-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-381">如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-382">下列其他旗標會搭配 **vcr** 裝置類型使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="f801c-383">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-385">如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI \_ VCR \_ 狀態 \_ 組合 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-387">如果組合模式為開啟， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 監視器</span><span class="sxs-lookup"><span data-stu-id="f801c-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="f801c-389">**DwReturn** 成員會設定為常數，表示目前選取的音訊監視器類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 監視器 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="f801c-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-391">**DwReturn** 成員會設定為目前選取之音訊監視器類型的數目。</span><span class="sxs-lookup"><span data-stu-id="f801c-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-393">如果指定了下一個 [記錄] 命令，則 **dwReturn** 成員會設定為 **TRUE** ，否則會記錄音訊。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="f801c-394">如果您 \_ 在此命令的 *dwFlags* 參數中指定 MCI TRACK， **dwTrack** 就會包含此查詢適用的曲目。</span><span class="sxs-lookup"><span data-stu-id="f801c-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f801c-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-396">**DwReturn** 成員會設定為常數，表示目前的音訊來源類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 來源 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="f801c-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-398">**DwReturn** 成員會設定為目前選取之音訊來源類型的編號。</span><span class="sxs-lookup"><span data-stu-id="f801c-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI \_ VCR \_ 狀態 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="f801c-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="f801c-400">**DwReturn** 成員會設定為目前的時鐘值（以總時鐘遞增）。</span><span class="sxs-lookup"><span data-stu-id="f801c-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI \_ VCR \_ 狀態 \_ 時鐘 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f801c-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="f801c-402">**DwReturn** 成員會設定為可唯一描述使用中時鐘的數位。</span><span class="sxs-lookup"><span data-stu-id="f801c-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI \_ VCR \_ 狀態 \_ 計數器 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="f801c-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-404">**DwReturn** 成員會設定為描述目前計數器格式的常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="f801c-405">如需詳細資訊，請參閱 \_ \_ \_ [MCI \_ set](mci-set.md) 命令的 mci set TIME FORMAT 旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI \_ VCR \_ 狀態 \_ 計數器 \_ 解析</span><span class="sxs-lookup"><span data-stu-id="f801c-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="f801c-407">**DwReturn** 成員會設定為描述計數器解析的常數，而且是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f801c-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="f801c-408">MCI \_ VCR \_ 計數器 \_ RES \_ 框架：計數器具有框架的解析度。</span><span class="sxs-lookup"><span data-stu-id="f801c-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="f801c-409">MCI \_ VCR \_ 計數器 \_ RES \_ seconds：計數器的解決方式為秒。</span><span class="sxs-lookup"><span data-stu-id="f801c-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="f801c-410">MCI \_ VCR \_ 狀態 \_ 計數器 \_ 值：在目前的計數器時間格式中， **dwReturn** 成員會設定為目前的計數器讀取。</span><span class="sxs-lookup"><span data-stu-id="f801c-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI \_ VCR \_ 狀態 \_ 幀 \_ 速率</span><span class="sxs-lookup"><span data-stu-id="f801c-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-412">**DwReturn** 成員會設定為裝置目前的原生畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f801c-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI \_ VCR \_ 狀態 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="f801c-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="f801c-414">**DwReturn** 成員會設定為常數，以描述螢幕上顯示的目前內容，而且是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="f801c-415">MCI \_ VCR \_ 索引 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="f801c-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="f801c-416">MCI \_ VCR \_ 索引 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="f801c-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="f801c-417">MCI \_ VCR \_ 索引 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="f801c-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="f801c-418">MCI \_ VCR \_ 索引時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="f801c-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="f801c-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_上的 MCI VCR \_ 狀態 \_ 索引 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f801c-420">如果螢幕上顯示開啟， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI \_ VCR \_ 狀態 \_ 媒體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f801c-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-422">**DwReturn** 成員會設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="f801c-423">MCI \_ VCR \_ 媒體 \_ 8</span><span class="sxs-lookup"><span data-stu-id="f801c-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="f801c-424">MCI \_ VCR \_ 媒體 \_ HI8</span><span class="sxs-lookup"><span data-stu-id="f801c-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="f801c-425">MCI \_ VCR \_ 媒體 \_ VHS</span><span class="sxs-lookup"><span data-stu-id="f801c-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="f801c-426">MCI \_ VCR \_ 媒體 \_ SVHS</span><span class="sxs-lookup"><span data-stu-id="f801c-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="f801c-427">MCI \_ VCR \_ 媒體搶鮮版（ \_ BETA）</span><span class="sxs-lookup"><span data-stu-id="f801c-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="f801c-428">MCI \_ VCR \_ 媒體 \_ EDBETA</span><span class="sxs-lookup"><span data-stu-id="f801c-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="f801c-429">MCI \_ VCR \_ 媒體 \_ 其他</span><span class="sxs-lookup"><span data-stu-id="f801c-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="f801c-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI \_ VCR \_ 狀態 \_ 號碼</span><span class="sxs-lookup"><span data-stu-id="f801c-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-431">當您搭配使用此旗標與 MCI \_ VCR \_ 狀態 \_ 調諧器 \_ 通道旗標時，dwNumber 成員會設定為邏輯調諧器號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ \_ \_ 音訊 \_ 曲目的 MCI VCR 狀態數位</span><span class="sxs-lookup"><span data-stu-id="f801c-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-433">**DwReturn** 成員會設定為可獨立選取的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="f801c-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ \_ \_ \_ 影片 \_ 曲目的 MCI VCR 狀態編號</span><span class="sxs-lookup"><span data-stu-id="f801c-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-435">**DwReturn** 成員會設定為可獨立選取的影片曲目數目。</span><span class="sxs-lookup"><span data-stu-id="f801c-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI \_ VCR \_ 狀態 \_ 暫停 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="f801c-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-437">**DwReturn** 成員會設定為 pause 命令的最長持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f801c-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="f801c-438">傳回值為零表示不會進行任何超時。</span><span class="sxs-lookup"><span data-stu-id="f801c-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI \_ VCR \_ 狀態 \_ 播放 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="f801c-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-440">**DwReturn** 成員會設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="f801c-441">MCI \_ VCR \_ 格式 \_ EP</span><span class="sxs-lookup"><span data-stu-id="f801c-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="f801c-442">MCI \_ VCR \_ 格式 \_ LP</span><span class="sxs-lookup"><span data-stu-id="f801c-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="f801c-443">其他的 MCI \_ VCR \_ 格式 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="f801c-444">MCI \_ VCR \_ 格式 \_ SP</span><span class="sxs-lookup"><span data-stu-id="f801c-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="f801c-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI \_ VCR \_ 狀態 \_ POSTROLL \_ 持續期間</span><span class="sxs-lookup"><span data-stu-id="f801c-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="f801c-446">**DwReturn** 成員會設定為以目前時間格式在停止的位置之後將播放的磁帶長度。</span><span class="sxs-lookup"><span data-stu-id="f801c-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="f801c-447">若要從停止或暫停命令煞車 VCR 磁帶傳輸，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="f801c-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI \_ VCR \_ 狀態 \_ 開啟 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f801c-449">如果開啟電源， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI \_ VCR \_ 狀態 \_ \_ 持續時間</span><span class="sxs-lookup"><span data-stu-id="f801c-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="f801c-451">**DwReturn** 成員會設定為將在其啟動所在位置之前播放的磁帶長度（以目前的時間格式）。</span><span class="sxs-lookup"><span data-stu-id="f801c-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="f801c-452">這是穩定 VCR 輸出的必要項。</span><span class="sxs-lookup"><span data-stu-id="f801c-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI \_ VCR \_ 狀態 \_ 記錄 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="f801c-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-454">**DwReturn** 成員會設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="f801c-455">MCI \_ VCR \_ 格式 \_ EP</span><span class="sxs-lookup"><span data-stu-id="f801c-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="f801c-456">MCI \_ VCR \_ 格式 \_ LP</span><span class="sxs-lookup"><span data-stu-id="f801c-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="f801c-457">其他的 MCI \_ VCR \_ 格式 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="f801c-458">MCI \_ VCR \_ 格式 \_ SP</span><span class="sxs-lookup"><span data-stu-id="f801c-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="f801c-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI \_ VCR \_ 狀態 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="f801c-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-460">**DwReturn** 成員會設定為目前的速度。</span><span class="sxs-lookup"><span data-stu-id="f801c-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="f801c-461">如需詳細資訊，請參閱 \_ \_ \_ [MCI \_ set](mci-set.md) 命令的 mci VCR 設定速度旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI \_ VCR \_ 狀態 \_ 時間 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f801c-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-463">**DwReturn** 成員會設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="f801c-464">MCI \_ VCR \_ 時間 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="f801c-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="f801c-465">MCI \_ VCR \_ 時間 \_ 偵測</span><span class="sxs-lookup"><span data-stu-id="f801c-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="f801c-466">MCI \_ VCR \_ 時間時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="f801c-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="f801c-467">如需詳細資訊，請參閱 \_ \_ \_ \_ [mci \_ set](mci-set.md) 命令的 mci VCR 設定時間模式旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI \_ VCR \_ 狀態 \_ 時間 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f801c-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-469">**DwReturn** 成員會設定為常數，以描述 [play](play.md)、 [record](record.md)、 [seek](seek.md)等) 所使用 (目前的時間類型，而且是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="f801c-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI \_ VCR \_ 時間 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="f801c-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-471">計數器正在使用中。</span><span class="sxs-lookup"><span data-stu-id="f801c-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ 時間時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="f801c-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-473">時間碼正在使用中。</span><span class="sxs-lookup"><span data-stu-id="f801c-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_存在 MCI VCR 狀態的時間 \_ \_ 碼 \_</span><span class="sxs-lookup"><span data-stu-id="f801c-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-475">如果時間碼出現在內容中的目前位置， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI \_ VCR \_ 狀態時間 \_ 碼 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-477">如果指定了下一個記錄命令，則 **dwReturn** 成員會設定為 **TRUE** ，否則會記錄時間碼。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI \_ VCR \_ 狀態時間 \_ 碼 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f801c-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-479">**DwReturn** 成員會設定為常數，描述裝置直接支援的時間碼類型，而且是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f801c-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="f801c-480">MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ NONE：此裝置不使用時間碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="f801c-481">MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ OTHER：此裝置使用未指定的時間碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="f801c-482">MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ SMPTE：此裝置使用的是 smpte 時間碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="f801c-483">MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ SMPTE \_ 捨棄：此裝置使用的是 SMPTE drop 時間碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI \_ VCR \_ 狀態 \_ 調諧器 \_ 頻道</span><span class="sxs-lookup"><span data-stu-id="f801c-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="f801c-485">**DwReturn** 成員會設定為目前的頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="f801c-486">如果您 \_ \_ \_ 在此命令的 *DWFLAGS* 參數中指定 MCI VCR 狀態號碼， **dwNumber** 就會包含此命令適用的邏輯調諧器號碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 監視</span><span class="sxs-lookup"><span data-stu-id="f801c-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="f801c-488">**DwReturn** 成員會設定為常數，表示目前選取的影片監視器類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 監視器 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="f801c-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-490">**DwReturn** 成員會設定為目前所選影片監視器類型的編號。</span><span class="sxs-lookup"><span data-stu-id="f801c-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-492">如果指定了下一個記錄命令，則 **dwReturn** 成員會設定為 **TRUE** ，如果影片將會錄製;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="f801c-493">如果您 \_ 在此命令的 *dwFlags* 參數中指定 MCI TRACK， **dwTrack** 就會包含此查詢適用的曲目。</span><span class="sxs-lookup"><span data-stu-id="f801c-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f801c-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-495">**DwReturn** 成員會設定為常數，指出目前選取的影片來源類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 來源 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="f801c-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f801c-497">**DwReturn** 成員會設定為目前所選影片來源類型的編號。</span><span class="sxs-lookup"><span data-stu-id="f801c-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ 狀態 \_ 寫入 \_ 受保護</span><span class="sxs-lookup"><span data-stu-id="f801c-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-499">如果媒體有寫入保護， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-500">若為 VCR 裝置， *lpStatus* 參數會指向 [**MCI \_ VCR \_ 狀態 \_ PARMS**](mci-vcr-status-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f801c-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="f801c-501">\_ \_ 除非已使用[mci \_ SET](mci-set.md)命令明確變更長度，否則使用 mci STATUS LENGTH 旗標來決定媒體的長度一律會傳回2小時的 VCR 裝置。</span><span class="sxs-lookup"><span data-stu-id="f801c-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="f801c-502">下列其他旗標會搭配覆迭 **裝置類型** 使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="f801c-503">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI \_ OVLY \_ 狀態 \_ HWND</span><span class="sxs-lookup"><span data-stu-id="f801c-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="f801c-505">**DwReturn** 成員會設定為與影片重迭裝置相關聯的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="f801c-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI \_ OVLY \_ 狀態 \_ 延展</span><span class="sxs-lookup"><span data-stu-id="f801c-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="f801c-507">如果已啟用延展， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-509">如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-510">下列其他旗標會搭配 **videodisc** 裝置類型使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="f801c-511">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="f801c-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-513">如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI \_ 狀態 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f801c-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-515">**DwReturn** 成員會設定為裝置的目前模式。</span><span class="sxs-lookup"><span data-stu-id="f801c-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="f801c-516">Videodisc 裝置除了可傳回的 \_ \_ 常數之外，還可以傳回 MCI VD 模式 \_ 公園常數，如 *dwFlags* 參數所述。</span><span class="sxs-lookup"><span data-stu-id="f801c-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI \_ VD \_ 狀態 \_ 光碟 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f801c-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-518">**DwReturn** 成員會設定為載入的光碟大小（以英寸為單位） (8 或 12) 。</span><span class="sxs-lookup"><span data-stu-id="f801c-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="f801c-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI \_ VD \_ 狀態 \_ 轉寄</span><span class="sxs-lookup"><span data-stu-id="f801c-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="f801c-520">如果向前播放， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f801c-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="f801c-521">MCI videodisc 裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI \_ VD \_ 狀態 \_ 媒體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f801c-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-523">**DwReturn** 成員會設定為所插入媒體的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f801c-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="f801c-524">可以傳回下列媒體類型：</span><span class="sxs-lookup"><span data-stu-id="f801c-524">The following media types can be returned:</span></span>

<span data-ttu-id="f801c-525">MCI \_ VD \_ MEDIA \_ CAV</span><span class="sxs-lookup"><span data-stu-id="f801c-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="f801c-526">MCI \_ VD \_ MEDIA \_ CLV</span><span class="sxs-lookup"><span data-stu-id="f801c-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="f801c-527">MCI \_ VD \_ \_ 其他媒體</span><span class="sxs-lookup"><span data-stu-id="f801c-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="f801c-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI \_ VD \_ 狀態 \_ 端</span><span class="sxs-lookup"><span data-stu-id="f801c-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-529">**DwReturn** 成員設定為1或2，表示已載入光碟的哪一端。</span><span class="sxs-lookup"><span data-stu-id="f801c-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="f801c-530">並非所有 videodisc 裝置都支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="f801c-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI \_ VD \_ 狀態 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="f801c-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f801c-532">**DwReturn** 成員會設定為每秒畫面格的播放速度。</span><span class="sxs-lookup"><span data-stu-id="f801c-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="f801c-533">MCIPIONR。WINSPOOL.DRV 設備磁碟機會傳回 MCIERR \_ 不支援的函式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f801c-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="f801c-534">下列其他旗標會搭配 **waveaudio** 裝置類型使用。</span><span class="sxs-lookup"><span data-stu-id="f801c-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="f801c-535">當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f801c-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="f801c-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ WAVE \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="f801c-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="f801c-537">**DwReturn** 成員會設定為目前用來播放、錄製和儲存的格式標記。</span><span class="sxs-lookup"><span data-stu-id="f801c-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="f801c-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-539">**DwReturn** 成員會設定為用於錄製的 wave 輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="f801c-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="f801c-540">如果沒有使用中的裝置，且未明確設定任何裝置，則錯誤會傳回 MCIERR \_ WAVE \_ INPUTUNSPECIFIED。</span><span class="sxs-lookup"><span data-stu-id="f801c-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="f801c-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f801c-542">**DwReturn** 成員會設定為用於播放的 wave 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="f801c-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="f801c-543">如果沒有使用中的裝置，且未明確設定任何裝置，則錯誤會傳回 MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED。</span><span class="sxs-lookup"><span data-stu-id="f801c-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI \_ WAVE \_ 狀態 \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="f801c-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f801c-545">**DwReturn** 成員會設定為目前每秒用來播放、錄製和儲存的位元組。</span><span class="sxs-lookup"><span data-stu-id="f801c-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI \_ WAVE \_ 狀態 \_ BITSPERSAMPLE</span><span class="sxs-lookup"><span data-stu-id="f801c-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="f801c-547">**DwReturn** 成員會設定為每個樣本的目前位數，用來播放、錄製和儲存 PCM 格式的資料。</span><span class="sxs-lookup"><span data-stu-id="f801c-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI \_ WAVE \_ 狀態 \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="f801c-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="f801c-549">**DwReturn** 成員會設定為目前用來播放、錄製和儲存的區塊對齊。</span><span class="sxs-lookup"><span data-stu-id="f801c-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI \_ WAVE \_ 狀態 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="f801c-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="f801c-551">**DwReturn** 成員會設定為目前用來播放、錄製和儲存的通道計數。</span><span class="sxs-lookup"><span data-stu-id="f801c-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI \_ WAVE \_ 狀態 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="f801c-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="f801c-553">**DwReturn** 成員會設定為 PCM 格式化資料的目前記錄或播放層級。</span><span class="sxs-lookup"><span data-stu-id="f801c-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="f801c-554">此值會以8或16位值傳回，視使用的樣本大小而定。</span><span class="sxs-lookup"><span data-stu-id="f801c-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="f801c-555">右側或 mono 通道層級會以低序位字組傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="f801c-556">左聲道層級會以高序位字的方式傳回。</span><span class="sxs-lookup"><span data-stu-id="f801c-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="f801c-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI \_ WAVE \_ 狀態 \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="f801c-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f801c-558">**DwReturn** 成員會設定為每秒用來播放、錄製和儲存的最新樣本。</span><span class="sxs-lookup"><span data-stu-id="f801c-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f801c-559">規格需求</span><span class="sxs-lookup"><span data-stu-id="f801c-559">Requirements</span></span>



| <span data-ttu-id="f801c-560">需求</span><span class="sxs-lookup"><span data-stu-id="f801c-560">Requirement</span></span> | <span data-ttu-id="f801c-561">值</span><span class="sxs-lookup"><span data-stu-id="f801c-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f801c-562">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f801c-562">Minimum supported client</span></span><br/> | <span data-ttu-id="f801c-563">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f801c-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f801c-564">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f801c-564">Minimum supported server</span></span><br/> | <span data-ttu-id="f801c-565">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f801c-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f801c-566">標頭</span><span class="sxs-lookup"><span data-stu-id="f801c-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="f801c-567"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f801c-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f801c-568">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f801c-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f801c-569">Mci</span><span class="sxs-lookup"><span data-stu-id="f801c-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f801c-570">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="f801c-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="f801c-571">MCI \_ 剪下</span><span class="sxs-lookup"><span data-stu-id="f801c-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="f801c-572">MCI \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="f801c-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="f801c-573">MCI \_ 貼上</span><span class="sxs-lookup"><span data-stu-id="f801c-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="f801c-574">MCI \_ 保留</span><span class="sxs-lookup"><span data-stu-id="f801c-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="f801c-575">MCI \_ 組</span><span class="sxs-lookup"><span data-stu-id="f801c-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="f801c-576">玩</span><span class="sxs-lookup"><span data-stu-id="f801c-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="f801c-577">記錄</span><span class="sxs-lookup"><span data-stu-id="f801c-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="f801c-578">尋求</span><span class="sxs-lookup"><span data-stu-id="f801c-578">seek</span></span>](seek.md)
</dt> </dl>

 

