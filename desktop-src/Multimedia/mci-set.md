---
title: 'MCI_SET 命令 (Mmsystem .h) '
description: MCI \_ SET 命令會設定裝置資訊。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "106997290"
---
# <a name="mci_set-command"></a><span data-ttu-id="44508-105">MCI \_ SET 命令</span><span class="sxs-lookup"><span data-stu-id="44508-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="44508-106">無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。</span><span class="sxs-lookup"><span data-stu-id="44508-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="44508-107">本檔中有 ' 從屬 ' 這個字的參考。</span><span class="sxs-lookup"><span data-stu-id="44508-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="44508-108">Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。</span><span class="sxs-lookup"><span data-stu-id="44508-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="44508-109">這種用語是用來做為命令內所使用的用語。</span><span class="sxs-lookup"><span data-stu-id="44508-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="44508-110">為求一致，本檔包含此字。</span><span class="sxs-lookup"><span data-stu-id="44508-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="44508-111">當您在命令中更改這個字時，我們會將此檔修正為一致。</span><span class="sxs-lookup"><span data-stu-id="44508-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="44508-112">MCI \_ SET 命令會設定裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="44508-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="44508-113">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="44508-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="44508-114">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="44508-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="44508-115">參數</span><span class="sxs-lookup"><span data-stu-id="44508-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44508-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="44508-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="44508-117">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="44508-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="44508-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="44508-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="44508-119">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44508-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="44508-120">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="44508-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="44508-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span><span class="sxs-lookup"><span data-stu-id="44508-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="44508-122">[**MCI \_ 設定 \_ PARMS**](mci-set-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="44508-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="44508-123">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="44508-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44508-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="44508-124">Return Value</span></span>

<span data-ttu-id="44508-125">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="44508-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44508-126">備註</span><span class="sxs-lookup"><span data-stu-id="44508-126">Remarks</span></span>

<span data-ttu-id="44508-127">下列其他旗標適用于所有支援 MCI 設定的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="44508-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="44508-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ 組 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="44508-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="44508-129">音訊頻道號碼會包含在由 *lpSet* 所識別之結構的 dwAudio 成員中。</span><span class="sxs-lookup"><span data-stu-id="44508-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-130">此旗標必須與設定為 \_ \_ ON 或 mci \_ OFF 的 mci 一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44508-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="44508-131">使用下列其中一個常數來表示通道號碼：</span><span class="sxs-lookup"><span data-stu-id="44508-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="44508-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ 設定 \_ 音訊 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="44508-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="44508-133">所有音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="44508-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="44508-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>剩餘的 MCI \_ 組 \_ 音訊 \_</span><span class="sxs-lookup"><span data-stu-id="44508-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="44508-135">左聲道。</span><span class="sxs-lookup"><span data-stu-id="44508-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="44508-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ 設定 \_ 音訊 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="44508-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="44508-137">右聲道。</span><span class="sxs-lookup"><span data-stu-id="44508-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="44508-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI \_ 設定 \_ 門 \_ 已關閉</span><span class="sxs-lookup"><span data-stu-id="44508-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="44508-139">關閉媒體蓋 (是否有任何) 。</span><span class="sxs-lookup"><span data-stu-id="44508-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="44508-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI \_ 設定 \_ 門 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="44508-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="44508-141">開啟媒體蓋 (（如果有任何) ）。</span><span class="sxs-lookup"><span data-stu-id="44508-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="44508-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44508-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="44508-143">停用指定的影片或音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="44508-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="44508-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="44508-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="44508-145">啟用指定的影片或音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="44508-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="44508-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI \_ 設定 \_ 時間 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="44508-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="44508-147">時間格式參數會包含在 *lpSet* 所識別之結構的 **dwTimeFormat** 成員中。</span><span class="sxs-lookup"><span data-stu-id="44508-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-148">下列旗標可搭配此旗標使用：</span><span class="sxs-lookup"><span data-stu-id="44508-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="44508-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI \_ 格式 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="44508-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="44508-150">在 PCM (脈衝程式碼調製) 資料格式，將時間成員描述變更為輸入或輸出的位元組。</span><span class="sxs-lookup"><span data-stu-id="44508-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="44508-151">由 **waveaudio** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="44508-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI \_ 格式 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="44508-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="44508-153">後續的命令將會使用框架。</span><span class="sxs-lookup"><span data-stu-id="44508-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="44508-154">由 **digitalvideo**、 **vcr** 和 **videodisc** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI \_ 格式 \_ HMS</span><span class="sxs-lookup"><span data-stu-id="44508-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="44508-156">將時間格式變更為小時、分鐘和秒。</span><span class="sxs-lookup"><span data-stu-id="44508-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="44508-157">由 **vcr** 和 **videodisc** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI \_ 格式 \_ 毫秒</span><span class="sxs-lookup"><span data-stu-id="44508-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="44508-159">將時間格式變更為毫秒。</span><span class="sxs-lookup"><span data-stu-id="44508-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="44508-160">所有裝置類型都能辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI \_ 格式 \_ MSF</span><span class="sxs-lookup"><span data-stu-id="44508-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="44508-162">將時間格式變更為分鐘、秒和框架。</span><span class="sxs-lookup"><span data-stu-id="44508-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="44508-163">**Cdaudio** 和 **vcr** 裝置類型的辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI \_ 格式 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="44508-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="44508-165">將時間格式變更為輸入或輸出的範例。</span><span class="sxs-lookup"><span data-stu-id="44508-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="44508-166">由 **waveaudio** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="44508-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ 格式 \_ \_ 的 SMPTE 24、 \_ MCI \_ 格式 \_ 的 smpte 25 以及 mci \_ 格式的 \_ smpte \_ 30</span><span class="sxs-lookup"><span data-stu-id="44508-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="44508-168">將時間格式設定為24、25和30個框架 SMPTE (社會的運動圖片和電視工程師分別) 。</span><span class="sxs-lookup"><span data-stu-id="44508-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="44508-169">由 **sequencer** 和 **vcr** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI \_ 格式的 \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="44508-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="44508-171">將時間格式設定為30個放置畫面的 SMPTE。</span><span class="sxs-lookup"><span data-stu-id="44508-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="44508-172">由 **sequencer** 和 **vcr** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI \_ 格式 \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="44508-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="44508-174">變更時間格式以追蹤、分、秒和框架。</span><span class="sxs-lookup"><span data-stu-id="44508-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="44508-175"> (MCI 使用連續的追蹤號碼。 ) 由 **cdaudio** 和 **vcr** 裝置類型辨識。</span><span class="sxs-lookup"><span data-stu-id="44508-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="44508-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI \_ 設定 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="44508-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="44508-177">設定開啟或關閉的視訊訊號。</span><span class="sxs-lookup"><span data-stu-id="44508-177">Sets the video signal on or off.</span></span> <span data-ttu-id="44508-178">此旗標必須與 \_ 設定為 \_ ON 或 mci OFF 的 \_ mci 一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44508-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="44508-179">沒有影片的裝置會傳回 MCIERR \_ 不支援 \_ 的功能。</span><span class="sxs-lookup"><span data-stu-id="44508-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="44508-180">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="44508-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44508-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ SET \_ >FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="44508-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="44508-182">檔案格式參數會包含在 *lpSet* 所識別之結構的 **dwFileFormat** 成員中。</span><span class="sxs-lookup"><span data-stu-id="44508-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-183">若為數位視訊裝置，則會使用檔案格式來儲存或捕捉命令。</span><span class="sxs-lookup"><span data-stu-id="44508-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="44508-184">如果省略此參數，則可能會預設為設備磁碟機定義的格式。</span><span class="sxs-lookup"><span data-stu-id="44508-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="44508-185">如果指定的檔案格式與目前選取的演算法和品質相衝突，則會將它們變更為檔案格式的預設值。</span><span class="sxs-lookup"><span data-stu-id="44508-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="44508-186">以下是定義的檔案格式常數：</span><span class="sxs-lookup"><span data-stu-id="44508-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="44508-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="44508-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="44508-188">AVI 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS</span><span class="sxs-lookup"><span data-stu-id="44508-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="44508-190">AVSS 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="44508-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="44508-192">DIB 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="44508-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="44508-194">JFIF 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="44508-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="44508-196">JPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="44508-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="44508-198">MPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB</span><span class="sxs-lookup"><span data-stu-id="44508-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="44508-200">RLE DIB 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG</span><span class="sxs-lookup"><span data-stu-id="44508-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="44508-202">RJPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="44508-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="44508-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ \_ \_ 精確地設定搜尋</span><span class="sxs-lookup"><span data-stu-id="44508-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="44508-204">設定用於定位的格式。</span><span class="sxs-lookup"><span data-stu-id="44508-204">Sets the format used for positioning.</span></span> <span data-ttu-id="44508-205">此旗標必須與設定為 \_ \_ ON 或 mci \_ OFF 的 mci 一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44508-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="44508-206">如果 \_ \_ 指定了 mci 設定，則播放或錄製會精確地從旗標存取以 mci 指定的框架 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44508-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="44508-207">如果要求的框架不是主要畫面格，這可能會增加一些額外的延遲。</span><span class="sxs-lookup"><span data-stu-id="44508-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="44508-208">如果 \_ \_ 指定了 MCI 設定，裝置將會搜尋在要求的框架之前的主要畫面格影像。</span><span class="sxs-lookup"><span data-stu-id="44508-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="44508-209">針對某些檔案和裝置，這可能是檔案的第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="44508-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="44508-210">此旗標的預設值是裝置相依的。</span><span class="sxs-lookup"><span data-stu-id="44508-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="44508-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI \_ DGV \_ 設定 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="44508-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="44508-212">速度參數會包含在由 *lpSet* 所識別之結構的 **dwSpeed** 成員中。</span><span class="sxs-lookup"><span data-stu-id="44508-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-213">速度會指定為名義畫面播放速率與所需畫面播放速率之間的比率，其中名義畫面播放速率會指定為1000。</span><span class="sxs-lookup"><span data-stu-id="44508-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="44508-214">半速度是500，而雙速度是2000。</span><span class="sxs-lookup"><span data-stu-id="44508-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="44508-215">允許的速度範圍也取決於裝置，也可能是檔案。</span><span class="sxs-lookup"><span data-stu-id="44508-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="44508-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_ \_ 尚未設定 MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="44508-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="44508-217">搭配 MCI \_ DGV \_ set >fileformat 使用時 \_ ，mci \_ 集會設定用於 capture 命令的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="44508-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="44508-218">針對數位影片裝置， *lpSet* 參數會指向 [**MCI \_ DGV \_ SET \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="44508-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="44508-219">下列其他旗標會搭配 **sequencer** 裝置類型使用：</span><span class="sxs-lookup"><span data-stu-id="44508-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44508-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ SEQ \_ 格式 \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="44508-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="44508-221">將時間格式設定為歌曲指標單位。</span><span class="sxs-lookup"><span data-stu-id="44508-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="44508-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ SEQ \_ SET \_ MASTER</span><span class="sxs-lookup"><span data-stu-id="44508-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="44508-223">將 sequencer 設定為同步處理資料的來源，並指出在 *lpSet* 所識別之結構的 **dwMaster** 成員中指定同步處理的類型。</span><span class="sxs-lookup"><span data-stu-id="44508-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-224">MCISEQ 傳回 MCIERR \_ 不支援 \_ 的函數。</span><span class="sxs-lookup"><span data-stu-id="44508-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="44508-225">以下是針對同步處理類型定義的常數：</span><span class="sxs-lookup"><span data-stu-id="44508-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="44508-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="44508-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="44508-227">Sequencer 會傳送 MIDI 格式同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="44508-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="44508-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="44508-229">Sequencer 會傳送 SMPTE 格式的同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="44508-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無</span><span class="sxs-lookup"><span data-stu-id="44508-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="44508-231">Sequencer 不會傳送同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="44508-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI \_ SEQ \_ SET \_ OFFSET</span><span class="sxs-lookup"><span data-stu-id="44508-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="44508-233">將序列的 SMPTE 位移變更為由 *lpSet* 所識別之結構的 **dwOffset** 成員所指定的。</span><span class="sxs-lookup"><span data-stu-id="44508-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-234">這只會影響具有 SMPTE 除法類型的序列。</span><span class="sxs-lookup"><span data-stu-id="44508-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="44508-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ SEQ \_ 設定 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="44508-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="44508-236">將序列的輸出 MIDI 埠設定為 *lpSet* 所識別結構之 **dwPort** 成員中的 MIDI 裝置識別碼所指定的。</span><span class="sxs-lookup"><span data-stu-id="44508-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-237">裝置會關閉先前的埠 (如果有任何) ，然後嘗試開啟並使用新的埠。</span><span class="sxs-lookup"><span data-stu-id="44508-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="44508-238">如果失敗，則會傳回錯誤，並重新開啟先前使用的埠 (如果有任何) 。</span><span class="sxs-lookup"><span data-stu-id="44508-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="44508-239">針對埠定義了下列常數：</span><span class="sxs-lookup"><span data-stu-id="44508-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="44508-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無</span><span class="sxs-lookup"><span data-stu-id="44508-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="44508-241">關閉先前使用的埠 (是否有任何) 。</span><span class="sxs-lookup"><span data-stu-id="44508-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="44508-242">如果埠已開啟，sequencer 的行為就會完全相同，但不會傳送任何 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="44508-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="44508-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI \_ 對應程式</span><span class="sxs-lookup"><span data-stu-id="44508-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="44508-244">將開啟的埠設定為 MIDI 對應程式。</span><span class="sxs-lookup"><span data-stu-id="44508-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="44508-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ SEQ \_ SET \_ 從屬</span><span class="sxs-lookup"><span data-stu-id="44508-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="44508-246">設定 sequencer 以接收同步處理資料，並指出同步處理的類型是在由 *lpSet* 所識別之結構的 **dwSlave** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="44508-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-247">MCISEQ 傳回 MCIERR \_ 不支援 \_ 的函數。</span><span class="sxs-lookup"><span data-stu-id="44508-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="44508-248">以下是針對同步處理類型定義的常數：</span><span class="sxs-lookup"><span data-stu-id="44508-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="44508-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI \_ SEQ \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="44508-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="44508-250">設定 sequencer 以接收包含在 MIDI 檔案中的同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="44508-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="44508-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="44508-252">設定 sequencer 以接收 MIDI 同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="44508-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無</span><span class="sxs-lookup"><span data-stu-id="44508-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="44508-254">將 sequencer 設定為忽略 MIDI 資料流程中的同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="44508-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="44508-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="44508-256">設定 sequencer 以接收 SMPTE 同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="44508-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="44508-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ SEQ \_ SET \_ 節奏</span><span class="sxs-lookup"><span data-stu-id="44508-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="44508-258">將 MIDI 序列的節奏變更為 *lpSet* 所指向之結構的 **dwTempo** 成員所指定的。</span><span class="sxs-lookup"><span data-stu-id="44508-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="44508-259">若為除法別為 PPQN 的序列，則會在每分鐘的節拍中指定節奏;針對具有範圍類型為 SMPTE 的序列，節奏是以每秒的畫面格來指定。</span><span class="sxs-lookup"><span data-stu-id="44508-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="44508-260">針對 sequencer 裝置， *lpSet* 參數會指向 [**MCI \_ SEQ \_ SET \_ PARMS**](mci-seq-set-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="44508-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="44508-261">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="44508-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44508-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI \_ VCR \_ 組 \_ 組合 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="44508-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="44508-263">將裝置設定為 [組合]、[插入] 和 [) ] 時， (組合或插入模式中記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="44508-264">使用下列其中一個旗標：</span><span class="sxs-lookup"><span data-stu-id="44508-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="44508-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="44508-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="44508-266">在上設定組合記錄，並關閉插入記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="44508-267">記錄所有的影片、音訊和時間碼追蹤。</span><span class="sxs-lookup"><span data-stu-id="44508-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="44508-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44508-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="44508-269">將組合記錄關閉，然後開啟插入記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="44508-270">當組合記錄關閉時，可以選取影片、音訊和時間碼的個別曲目來進行錄製。</span><span class="sxs-lookup"><span data-stu-id="44508-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="44508-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR \_ 設定 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="44508-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="44508-272">*LpSet* 所識別之結構的 **dwClock** 成員包含新的時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="44508-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="44508-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR \_ 組 \_ 計數器 \_ 估價</span><span class="sxs-lookup"><span data-stu-id="44508-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="44508-274">*LpSet* 所識別之結構的 **dwCounterFormat** 成員包含常數，指定狀態計數器要使用的新計數器時間格式。</span><span class="sxs-lookup"><span data-stu-id="44508-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="44508-275">如需有效的常數清單，請參閱 \_ \_ \_ 此命令的其他旗標清單中的 MCI 設定時間格式。</span><span class="sxs-lookup"><span data-stu-id="44508-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="44508-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI \_ VCR \_ 設定 \_ 計數器 \_ 值</span><span class="sxs-lookup"><span data-stu-id="44508-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="44508-277">*LpSet* 所識別之結構的 **dwCounterValue** 成員包含新的計數器值。</span><span class="sxs-lookup"><span data-stu-id="44508-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="44508-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI \_ VCR \_ 設定 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="44508-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="44508-279">*LpSet* 所識別之結構的 **dwIndex** 成員包含一個常數，表示螢幕上顯示的內容，而且必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="44508-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="44508-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI \_ VCR \_ 索引 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="44508-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="44508-281">顯示計數器。</span><span class="sxs-lookup"><span data-stu-id="44508-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="44508-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI \_ VCR \_ 索引 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="44508-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="44508-283">顯示日期。</span><span class="sxs-lookup"><span data-stu-id="44508-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="44508-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI \_ VCR \_ 索引 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="44508-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="44508-285">顯示時間。</span><span class="sxs-lookup"><span data-stu-id="44508-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="44508-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI \_ VCR \_ 索引時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="44508-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="44508-287">顯示時間碼。</span><span class="sxs-lookup"><span data-stu-id="44508-287">Displays timecode.</span></span>

<span data-ttu-id="44508-288">如需詳細資訊，請參閱 [MCI \_ INDEX](mci-index.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="44508-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="44508-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI \_ VCR \_ 設定 \_ 暫停 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="44508-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="44508-290">*LpSet* 所識別之結構的 **dwPauseTimeout** 成員包含 pause 命令的最長持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="44508-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="44508-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI \_ VCR \_ SET \_ POSTROLL \_ DURATION</span><span class="sxs-lookup"><span data-stu-id="44508-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="44508-292">*LpSet* 所識別之結構的 **dwPostrollDuration** 成員包含的磁帶長度（以目前的時間格式），在發出 stop 或 pause 命令時，需要用來煞車 VCR 傳輸。</span><span class="sxs-lookup"><span data-stu-id="44508-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="44508-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ 設定 \_ 電源</span><span class="sxs-lookup"><span data-stu-id="44508-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="44508-294">設定開啟或關閉電源。</span><span class="sxs-lookup"><span data-stu-id="44508-294">Sets the power on or off.</span></span> <span data-ttu-id="44508-295">必須搭配下列其中一個旗標使用：</span><span class="sxs-lookup"><span data-stu-id="44508-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="44508-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44508-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="44508-297">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="44508-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="44508-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="44508-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="44508-299">開啟電源。</span><span class="sxs-lookup"><span data-stu-id="44508-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="44508-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI \_ VCR \_ 設定預先進行 \_ \_ 持續時間</span><span class="sxs-lookup"><span data-stu-id="44508-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="44508-301">由 *lpSet* 所識別之結構的 **dwPrerollDuration** 成員包含以目前時間格式表示的磁帶長度，以穩定 VCR 輸出。</span><span class="sxs-lookup"><span data-stu-id="44508-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="44508-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI \_ VCR \_ 設定 \_ 記錄 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="44508-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="44508-303">*LpSet* 所識別之結構的 **dwRecordFormat** 成員包含描述記錄速度的常數，其必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="44508-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="44508-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR \_ 格式 \_ EP</span><span class="sxs-lookup"><span data-stu-id="44508-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="44508-305">速度較慢的記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="44508-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI \_ VCR \_ 格式 \_ LP</span><span class="sxs-lookup"><span data-stu-id="44508-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="44508-307">以中度慢的記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="44508-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR \_ 格式 \_ SP</span><span class="sxs-lookup"><span data-stu-id="44508-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="44508-309">標準速度的記錄。</span><span class="sxs-lookup"><span data-stu-id="44508-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="44508-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI \_ VCR \_ 設定 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="44508-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="44508-311">由 *lpSet* 所識別之結構的 **dwSpeed** 成員包含新的速度設定，其中1000是正常的速度、2000是雙速度，而500是半速度等等。</span><span class="sxs-lookup"><span data-stu-id="44508-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="44508-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ 設定 \_ 磁帶 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="44508-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="44508-313">*LpSet* 所識別之結構的 **dwTapeLength** 成員包含磁帶的新長度（前提是磁帶的長度無法偵測）。</span><span class="sxs-lookup"><span data-stu-id="44508-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="44508-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR \_ 設定 \_ 時間 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="44508-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="44508-315">*LpSet* 所識別之結構的 **dwTimeMode** 成員包含一個常數，表示新的位置時間模式。</span><span class="sxs-lookup"><span data-stu-id="44508-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="44508-316">以下是有效的常數：</span><span class="sxs-lookup"><span data-stu-id="44508-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="44508-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI \_ VCR \_ 時間 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="44508-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="44508-318">強制裝置以獨佔方式使用計數器。</span><span class="sxs-lookup"><span data-stu-id="44508-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="44508-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI \_ VCR \_ 時間 \_ 偵測</span><span class="sxs-lookup"><span data-stu-id="44508-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="44508-320">每次將新的磁帶插入裝置，或模式從尚未就緒變更為就緒時，裝置應該會嘗試判斷磁帶上是否有可用的時間碼。</span><span class="sxs-lookup"><span data-stu-id="44508-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="44508-321">如果有時間碼可用，請在所有指定位置的後續命令中使用時間碼。</span><span class="sxs-lookup"><span data-stu-id="44508-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="44508-322">否則，請使用計數器。</span><span class="sxs-lookup"><span data-stu-id="44508-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="44508-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ 時間時間 \_ 碼</span><span class="sxs-lookup"><span data-stu-id="44508-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="44508-324">強制裝置僅使用時間碼。</span><span class="sxs-lookup"><span data-stu-id="44508-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="44508-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI \_ VCR \_ 組 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="44508-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="44508-326">使用微調調整來微調 VCR 磁帶傳輸的速度，而且必須搭配下列其中一個旗標使用：</span><span class="sxs-lookup"><span data-stu-id="44508-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="44508-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ PLUS</span><span class="sxs-lookup"><span data-stu-id="44508-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="44508-328">增加磁帶傳送速率。</span><span class="sxs-lookup"><span data-stu-id="44508-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="44508-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ 減號</span><span class="sxs-lookup"><span data-stu-id="44508-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="44508-330">減少磁帶傳送速率。</span><span class="sxs-lookup"><span data-stu-id="44508-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="44508-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI \_ VCR \_ 重設</span><span class="sxs-lookup"><span data-stu-id="44508-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="44508-332">將追蹤調整傳回到零。</span><span class="sxs-lookup"><span data-stu-id="44508-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="44508-333">若為 VCR 裝置， *lpSet* 參數會指向 [**MCI \_ VCR \_ 組 \_ PARMS**](mci-vcr-set-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="44508-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="44508-334">下列其他旗標適用于 **videodisc** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="44508-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44508-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI \_ VD \_ 格式 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="44508-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="44508-336">變更追蹤的時間格式。</span><span class="sxs-lookup"><span data-stu-id="44508-336">Changes the time format to tracks.</span></span> <span data-ttu-id="44508-337">MCI 使用連續的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="44508-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="44508-338">下列其他旗標適用于 **waveaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="44508-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44508-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="44508-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="44508-340">將用於記錄的輸入設定為 *lpSet* 所識別之結構的 **wInput** 成員。</span><span class="sxs-lookup"><span data-stu-id="44508-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="44508-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="44508-342">設定用來播放 *lpSet* 所識別結構之 **wOutput** 成員的輸出。</span><span class="sxs-lookup"><span data-stu-id="44508-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI \_ WAVE \_ 設定 \_ ANYINPUT</span><span class="sxs-lookup"><span data-stu-id="44508-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="44508-344">任何與目前格式相容的 wave 輸入都可以用來錄製。</span><span class="sxs-lookup"><span data-stu-id="44508-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="44508-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI \_ WAVE \_ 設定 \_ ANYOUTPUT</span><span class="sxs-lookup"><span data-stu-id="44508-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="44508-346">任何與目前格式相容的 wave 輸出都可用於播放。</span><span class="sxs-lookup"><span data-stu-id="44508-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="44508-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI \_ WAVE \_ 設定 \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="44508-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="44508-348">設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nAvgBytesPerSec** 成員的每秒位元組數。</span><span class="sxs-lookup"><span data-stu-id="44508-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI \_ WAVE \_ 設定 \_ BITSPERSAMPLE</span><span class="sxs-lookup"><span data-stu-id="44508-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="44508-350">設定用來播放、錄製和儲存至 *lpSet* 所識別之 PCM 資料格式 **nBitsPerSample** 成員的每個樣本位數。</span><span class="sxs-lookup"><span data-stu-id="44508-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI \_ WAVE \_ 設定 \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="44508-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="44508-352">設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nBlockAlign** 成員的區塊對齊。</span><span class="sxs-lookup"><span data-stu-id="44508-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI \_ WAVE \_ 設定 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="44508-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="44508-354">通道的數目會以 *lpSet* 所識別之結構的 **nChannels** 成員表示。</span><span class="sxs-lookup"><span data-stu-id="44508-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="44508-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI \_ WAVE \_ 設定 \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="44508-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="44508-356">設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **wFormatTag** 成員的格式類型。</span><span class="sxs-lookup"><span data-stu-id="44508-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="44508-357">指定 WAVE \_ 格式 \_ PCM 會將格式變更為 pcm。</span><span class="sxs-lookup"><span data-stu-id="44508-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="44508-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI \_ WAVE \_ 設定 \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="44508-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="44508-359">設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nSamplesPerSec** 成員的每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="44508-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="44508-360">針對 wave 音訊裝置， *lpSet* 參數會指向 [**MCI \_ WAVE \_ 設定 \_ PARMS**](mci-wave-set-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="44508-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="44508-361">在儲存資料的檔案建立時，會定義多個波形音訊資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="44508-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="44508-362">這些屬性會描述如何在檔案中結構化資料，而且在錄製開始之後就無法變更。</span><span class="sxs-lookup"><span data-stu-id="44508-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="44508-363">下列旗標清單會識別這些屬性：</span><span class="sxs-lookup"><span data-stu-id="44508-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="44508-364">MCI \_ WAVE \_ 設定 \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="44508-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="44508-365">MCI \_ WAVE \_ 設定 \_ BITSPERSAMPLE</span><span class="sxs-lookup"><span data-stu-id="44508-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="44508-366">MCI \_ WAVE \_ 設定 \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="44508-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="44508-367">MCI \_ WAVE \_ 設定 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="44508-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="44508-368">MCI \_ WAVE \_ 設定 \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="44508-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="44508-369">MCI \_ WAVE \_ 設定 \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="44508-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="44508-370">規格需求</span><span class="sxs-lookup"><span data-stu-id="44508-370">Requirements</span></span>



| <span data-ttu-id="44508-371">需求</span><span class="sxs-lookup"><span data-stu-id="44508-371">Requirement</span></span> | <span data-ttu-id="44508-372">值</span><span class="sxs-lookup"><span data-stu-id="44508-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44508-373">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44508-373">Minimum supported client</span></span><br/> | <span data-ttu-id="44508-374">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44508-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="44508-375">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44508-375">Minimum supported server</span></span><br/> | <span data-ttu-id="44508-376">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44508-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="44508-377">標頭</span><span class="sxs-lookup"><span data-stu-id="44508-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="44508-378"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="44508-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44508-379">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44508-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44508-380">Mci</span><span class="sxs-lookup"><span data-stu-id="44508-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44508-381">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="44508-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

