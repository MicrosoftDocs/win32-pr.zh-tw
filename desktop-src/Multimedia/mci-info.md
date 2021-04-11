---
title: 'MCI_INFO 命令 (Mmsystem .h) '
description: MCI \_ INFO 命令會從裝置取出字串資訊。
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105708"
---
# <a name="mci_info-command"></a><span data-ttu-id="788d4-104">MCI \_ 資訊命令</span><span class="sxs-lookup"><span data-stu-id="788d4-104">MCI\_INFO command</span></span>

<span data-ttu-id="788d4-105">MCI \_ INFO 命令會從裝置取出字串資訊。</span><span class="sxs-lookup"><span data-stu-id="788d4-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="788d4-106">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="788d4-106">All devices recognize this command.</span></span> <span data-ttu-id="788d4-107">資訊會以 *lpInfo* 所識別之結構的 **lpstrReturn** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="788d4-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="788d4-108">**DwRetSize** 成員會指定傳回之資料的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="788d4-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="788d4-109">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="788d4-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="788d4-110">參數</span><span class="sxs-lookup"><span data-stu-id="788d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788d4-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="788d4-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="788d4-112">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="788d4-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="788d4-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="788d4-114">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="788d4-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="788d4-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="788d4-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="788d4-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="788d4-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="788d4-117">[**MCI \_ 資訊 \_ PARMS**](mci-info-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="788d4-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="788d4-118">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="788d4-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788d4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="788d4-119">Return Value</span></span>

<span data-ttu-id="788d4-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="788d4-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="788d4-121">備註</span><span class="sxs-lookup"><span data-stu-id="788d4-121">Remarks</span></span>

<span data-ttu-id="788d4-122">下列其他標準和命令特定旗標適用于所有支援 MCI 資訊的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="788d4-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI \_ 資訊 \_ 產品</span><span class="sxs-lookup"><span data-stu-id="788d4-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-124">取得與裝置相關聯之硬體的描述。</span><span class="sxs-lookup"><span data-stu-id="788d4-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="788d4-125">裝置應該提供識別驅動程式和所使用硬體的描述。</span><span class="sxs-lookup"><span data-stu-id="788d4-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-126">下列其他旗標適用于 **cdaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="788d4-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI \_ 資訊 \_ 媒體身分 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="788d4-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="788d4-128">針對目前已在正在進行查詢的播放程式中載入的音訊 CD 產生唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="788d4-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="788d4-129">此旗標會傳回16個十六進位數位的字串。</span><span class="sxs-lookup"><span data-stu-id="788d4-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ 資訊 \_ 媒體 \_ UPC</span><span class="sxs-lookup"><span data-stu-id="788d4-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="788d4-131">產生在音訊 CD 上編碼 (UPC) 的通用產品程式碼。</span><span class="sxs-lookup"><span data-stu-id="788d4-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="788d4-132">UPC 是數位的字串。</span><span class="sxs-lookup"><span data-stu-id="788d4-132">The UPC is a string of digits.</span></span> <span data-ttu-id="788d4-133">它可能不適用於所有 Cd。</span><span class="sxs-lookup"><span data-stu-id="788d4-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-134">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="788d4-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI \_ DGV \_ 資訊 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="788d4-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="788d4-136">常數，表示所需的資訊會包含在 *lpInfo* 所識別之結構的 **dwItem** 成員中。</span><span class="sxs-lookup"><span data-stu-id="788d4-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="788d4-137">下列常數是針對數位視訊裝置所定義：</span><span class="sxs-lookup"><span data-stu-id="788d4-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="788d4-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ 資訊 \_ 音訊 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="788d4-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="788d4-139">傳回目前音訊壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ 資訊 \_ 音訊 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="788d4-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="788d4-141">傳回目前音訊品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI \_ DGV \_ 資訊 \_ 還是 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="788d4-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="788d4-143">傳回目前靜止影像壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI \_ DGV \_ 資訊 \_ 仍為 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="788d4-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="788d4-145">傳回目前靜止影像品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI \_ DGV \_ 資訊 \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="788d4-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="788d4-147">傳回字串，描述可能由視覺效果的擁有者或工作區中的資料所造成的使用限制。</span><span class="sxs-lookup"><span data-stu-id="788d4-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ 資訊 \_ 影片 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="788d4-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="788d4-149">傳回目前視訊壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI \_ DGV \_ 資訊 \_ 影片 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="788d4-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="788d4-151">傳回目前影片品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI \_ 資訊 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="788d4-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="788d4-153">傳回設備磁碟機和硬體的版本層級。</span><span class="sxs-lookup"><span data-stu-id="788d4-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="788d4-154">設備磁碟機開發人員必須記錄所傳回字串的語法。</span><span class="sxs-lookup"><span data-stu-id="788d4-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI \_ DGV \_ 資訊 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="788d4-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-156">取得視窗標題。</span><span class="sxs-lookup"><span data-stu-id="788d4-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="788d4-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="788d4-158">取得以 [MCI \_ OPEN](mci-open.md) 或 [mci \_ LOAD](mci-load.md) 命令指定之最後一個檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="788d4-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="788d4-159">如果未指定檔案，裝置會傳回以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="788d4-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="788d4-160">只有傳回 **TRUE** 給 mci \_ GETDEVCAPS \_ 使用 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令的 [檔案] 旗標的裝置才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="788d4-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-161">針對數位影片裝置， *lpInfo* 會指向 [**MCI \_ DGV \_ INFO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="788d4-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="788d4-162">下列其他旗標適用于 **sequencer** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="788d4-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI \_ 資訊 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="788d4-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-164">從著作權中繼活動取得 MIDI 檔案的著作權注意事項。</span><span class="sxs-lookup"><span data-stu-id="788d4-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="788d4-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="788d4-166">取得目前檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="788d4-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="788d4-167">只有 **當您** 使用 mci GETDEVCAPS [使用檔案] 旗標呼叫 [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令時，裝置才會支援此旗標 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="788d4-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI \_ 資訊 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="788d4-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="788d4-169">從 sequence/track name 中繼事件取得序列名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-170">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="788d4-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI \_ VCR \_ 資訊 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="788d4-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="788d4-172">設定 [**MCI \_ INFO \_ PARMS**](mci-info-parms.md)結構的 **lpstrReturn** 成員，以指向版本號碼。</span><span class="sxs-lookup"><span data-stu-id="788d4-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="788d4-173">也會將 **dwRetSize** 成員設定為等於指向之字串的長度。</span><span class="sxs-lookup"><span data-stu-id="788d4-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-174">下列其他旗標 **適用于重迭裝置類型** ：</span><span class="sxs-lookup"><span data-stu-id="788d4-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="788d4-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="788d4-176">取得目前檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="788d4-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="788d4-177">只有傳回 **TRUE** 給 mci \_ GETDEVCAPS \_ 使用 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令的 [檔案] 旗標的裝置才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="788d4-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI \_ OVLY \_ 資訊 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="788d4-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-179">取得與影片重迭裝置相關聯之視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="788d4-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="788d4-180">下列其他旗標適用于 **waveaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="788d4-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="788d4-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="788d4-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="788d4-182">取得目前檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="788d4-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="788d4-183">**當您** 使用 mci GETDEVCAPS [使用檔案] 旗標呼叫 [mci \_ GETDEVCAPS](mci-getdevcaps.md)命令時，裝置會支援此旗標 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="788d4-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="788d4-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-185">取得目前輸入的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="788d4-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="788d4-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="788d4-187">取得目前輸出的產品名稱，且其值為裝置特定。</span><span class="sxs-lookup"><span data-stu-id="788d4-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="788d4-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="788d4-188">Requirements</span></span>



| <span data-ttu-id="788d4-189">需求</span><span class="sxs-lookup"><span data-stu-id="788d4-189">Requirement</span></span> | <span data-ttu-id="788d4-190">值</span><span class="sxs-lookup"><span data-stu-id="788d4-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="788d4-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="788d4-191">Minimum supported client</span></span><br/> | <span data-ttu-id="788d4-192">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="788d4-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="788d4-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="788d4-193">Minimum supported server</span></span><br/> | <span data-ttu-id="788d4-194">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="788d4-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="788d4-195">標頭</span><span class="sxs-lookup"><span data-stu-id="788d4-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="788d4-196"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="788d4-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788d4-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="788d4-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788d4-198">Mci</span><span class="sxs-lookup"><span data-stu-id="788d4-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="788d4-199">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="788d4-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

