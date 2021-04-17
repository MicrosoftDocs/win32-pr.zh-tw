---
title: 'MCI_SETVIDEO 命令 (Mmsystem .h) '
description: MCI \_ SETVIDEO 命令會設定與影片播放相關聯的值。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465417"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="390ad-105">MCI \_ SETVIDEO 命令</span><span class="sxs-lookup"><span data-stu-id="390ad-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="390ad-106">MCI \_ SETVIDEO 命令會設定與影片播放相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="390ad-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="390ad-107">數位影片和 VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="390ad-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="390ad-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="390ad-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="390ad-109">參數</span><span class="sxs-lookup"><span data-stu-id="390ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390ad-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="390ad-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="390ad-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="390ad-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="390ad-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="390ad-113">**MCI \_通知**、 **mci \_ 等候** 或 **MCI \_ 測試**。</span><span class="sxs-lookup"><span data-stu-id="390ad-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="390ad-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="390ad-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="390ad-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span><span class="sxs-lookup"><span data-stu-id="390ad-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="390ad-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="390ad-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="390ad-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="390ad-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390ad-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="390ad-118">Return Value</span></span>

<span data-ttu-id="390ad-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="390ad-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="390ad-120">備註</span><span class="sxs-lookup"><span data-stu-id="390ad-120">Remarks</span></span>

<span data-ttu-id="390ad-121">下列其他旗標會搭配 "digitalvideo" 裝置類型使用：</span><span class="sxs-lookup"><span data-stu-id="390ad-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="390ad-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG</span><span class="sxs-lookup"><span data-stu-id="390ad-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="390ad-123">*LpSetVideo* 所識別之結構的 **lpstrAlgorithm** 成員包含包含視訊壓縮演算法名稱的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="390ad-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="390ad-124">壓縮演算法會由後續的 [mci \_ 保留](mci-reserve.md) 或 [MCI \_ 記錄](mci-record.md) 命令使用。</span><span class="sxs-lookup"><span data-stu-id="390ad-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="390ad-125">可用的演算法取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="390ad-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="390ad-126">如果指定的演算法與目前的檔案格式不相容，則檔案格式會變更為演算法的預設格式。</span><span class="sxs-lookup"><span data-stu-id="390ad-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="390ad-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="390ad-128">搭配 **MCI \_ DGV \_ SETVIDEO \_** 使用時，表示指定時間（以毫秒為單位），且為絕對時間。</span><span class="sxs-lookup"><span data-stu-id="390ad-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="390ad-129"> (這次無法在工作區的播放中執行。 ) </span><span class="sxs-lookup"><span data-stu-id="390ad-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="390ad-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI \_ DGV \_ SETVIDEO \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="390ad-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="390ad-131">修改 **MCI \_ DGV \_ SETVIDEO \_ 亮度**、 **mci \_ DGV \_ SETVIDEO \_ COLOR**、 **mci \_ DGV \_ SETVIDEO \_ 對比度**、 **MCI \_ DGV \_ SETVIDEO \_ GAMMA**、 **mci \_ DGV \_ SETVIDEO \_ 銳利** 或 **mci DGV SETVIDEO \_ \_ \_ 淡色** ，使其影響輸入信號並修改記錄的內容。</span><span class="sxs-lookup"><span data-stu-id="390ad-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="390ad-132">可能的話，這是監視輸入時的預設值。</span><span class="sxs-lookup"><span data-stu-id="390ad-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI \_ DGV \_ SETVIDEO \_ 專案</span><span class="sxs-lookup"><span data-stu-id="390ad-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="390ad-134">影片常數是在 *lpSetVideo* 所識別之結構的 **dwItem** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-135">常數可識別正在設定的值。</span><span class="sxs-lookup"><span data-stu-id="390ad-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="390ad-136">您可以使用此旗標來指定下列常數：</span><span class="sxs-lookup"><span data-stu-id="390ad-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="390ad-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI \_ AVI \_ SETVIDEO \_ DRAW \_ 程式</span><span class="sxs-lookup"><span data-stu-id="390ad-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-138">在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定了新的繪圖程式位址。</span><span class="sxs-lookup"><span data-stu-id="390ad-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-139">只有在裝置閒置時，才可以指定新的繪圖程式。</span><span class="sxs-lookup"><span data-stu-id="390ad-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="390ad-140">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="390ad-141">字串命令介面中沒有此旗標的對等專案。</span><span class="sxs-lookup"><span data-stu-id="390ad-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ SETVIDEO \_ 調色板 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="390ad-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="390ad-143">在 *lpSetVideo* 所識別之結構的 **dwOver** 和 **dwValue** 成員中指定了新的調色板色彩。</span><span class="sxs-lookup"><span data-stu-id="390ad-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-144">**DwOver** 成員會指定要變更之色彩的調色板索引，而 **dwValue** 成員會以 RGB 值指定新的色彩。</span><span class="sxs-lookup"><span data-stu-id="390ad-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="390ad-145">當您使用此常數時，您也必須使用 **mci \_ DGV \_ SETVIDEO \_ 專案** 來指定 **mci \_ DGV \_ SETVIDEO \_ OVER** 和 **mci \_ DGV \_ SETVIDEO \_ 值** 旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="390ad-146">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ SETVIDEO \_ 調色板 \_ 半色調</span><span class="sxs-lookup"><span data-stu-id="390ad-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-148">指出應該使用半色調調色板，而不是預設的調色板。</span><span class="sxs-lookup"><span data-stu-id="390ad-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="390ad-149">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="390ad-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="390ad-151">依 *lpSetVideo* 所識別之結構的 **dwValue** 成員，指定每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="390ad-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-152">每圖元的位數會用來儲存已捕捉或已記錄的資料</span><span class="sxs-lookup"><span data-stu-id="390ad-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="390ad-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ SETVIDEO \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="390ad-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="390ad-154">影片亮度層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的因素。</span><span class="sxs-lookup"><span data-stu-id="390ad-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI \_ DGV \_ SETVIDEO \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="390ad-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="390ad-156">影片色彩飽和度層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的因素。</span><span class="sxs-lookup"><span data-stu-id="390ad-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI \_ DGV \_ SETVIDEO \_ 對比</span><span class="sxs-lookup"><span data-stu-id="390ad-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="390ad-158">影片對比層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。</span><span class="sxs-lookup"><span data-stu-id="390ad-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ SETVIDEO \_ 幀 \_ 速率</span><span class="sxs-lookup"><span data-stu-id="390ad-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-160">畫面播放速率是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-161">速率是以每秒的畫面格時間單位（1000）來指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="390ad-162">例如，每秒29.97 個畫面格會指定為29970。</span><span class="sxs-lookup"><span data-stu-id="390ad-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ GAMMA</span><span class="sxs-lookup"><span data-stu-id="390ad-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="390ad-164">Gamma 更正指數值是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-165">Gamma 修正會調整在展示來源中編碼的強度與顯示的亮度之間的對應。</span><span class="sxs-lookup"><span data-stu-id="390ad-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="390ad-166">值是指數乘以1000。</span><span class="sxs-lookup"><span data-stu-id="390ad-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="390ad-167">例如，2200表示2.2 的指數。</span><span class="sxs-lookup"><span data-stu-id="390ad-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="390ad-168">值為1000時，表示指數為1，不會套用 gamma 更正。</span><span class="sxs-lookup"><span data-stu-id="390ad-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ COLOR</span><span class="sxs-lookup"><span data-stu-id="390ad-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="390ad-170">索引鍵色彩是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-171">按鍵色彩是 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="390ad-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ INDEX</span><span class="sxs-lookup"><span data-stu-id="390ad-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="390ad-173">索引鍵索引值是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-174">Index 參數是實體的調色板索引。</span><span class="sxs-lookup"><span data-stu-id="390ad-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE</span><span class="sxs-lookup"><span data-stu-id="390ad-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-176">在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定了調色板控制碼。</span><span class="sxs-lookup"><span data-stu-id="390ad-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-177">調色板控制碼包含在低序位字組中。</span><span class="sxs-lookup"><span data-stu-id="390ad-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="390ad-178">數位影片裝置不應該釋出使用此命令傳遞的調色板。</span><span class="sxs-lookup"><span data-stu-id="390ad-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="390ad-179">應用程式應該在關閉裝置之後釋放。</span><span class="sxs-lookup"><span data-stu-id="390ad-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="390ad-180">只有使用調色板的裝置才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="390ad-181">如果這個指定的調色板控制碼為零，則會使用預設的調色板。</span><span class="sxs-lookup"><span data-stu-id="390ad-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ SETVIDEO \_ 清晰度</span><span class="sxs-lookup"><span data-stu-id="390ad-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="390ad-183">影片清晰度值會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。</span><span class="sxs-lookup"><span data-stu-id="390ad-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI \_ DGV \_ SETVIDEO \_ 來源</span><span class="sxs-lookup"><span data-stu-id="390ad-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-185">指定影片輸入來源的常數會指定于 *lpSetVideo* 所識別之結構的 **dwValue** 成員中。</span><span class="sxs-lookup"><span data-stu-id="390ad-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-186">以下是定義的常數：</span><span class="sxs-lookup"><span data-stu-id="390ad-186">The following constants are defined:</span></span>

-   <span data-ttu-id="390ad-187">**MCI \_DGV \_ SETVIDEO \_ SRC \_ NTSC**： ntsc 電視。</span><span class="sxs-lookup"><span data-stu-id="390ad-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="390ad-188">MCI \_ DGV \_ SETVIDEO \_ SRC \_ pal： pal 電視。</span><span class="sxs-lookup"><span data-stu-id="390ad-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="390ad-189">MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB： rgb video。</span><span class="sxs-lookup"><span data-stu-id="390ad-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="390ad-190">MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM： SECAM 電視。</span><span class="sxs-lookup"><span data-stu-id="390ad-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="390ad-191">MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO： S-Video。</span><span class="sxs-lookup"><span data-stu-id="390ad-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI \_ DGV \_ SETVIDEO \_ STREAM</span><span class="sxs-lookup"><span data-stu-id="390ad-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="390ad-193">影片資料流程是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-194">整數值指定從工作區播放的影片串流。</span><span class="sxs-lookup"><span data-stu-id="390ad-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="390ad-195">如果未指定資料流程，且檔案格式未定義預設資料流程，則會播放第一個實際交錯的影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="390ad-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ SETVIDEO \_ 淡色</span><span class="sxs-lookup"><span data-stu-id="390ad-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="390ad-197">影片色調值會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。</span><span class="sxs-lookup"><span data-stu-id="390ad-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-198">一般而言，這項調整會在許多彩色電視集的淡色控制項之後進行模型化，並將250定義為綠色、750定義為紅色，而 0 (或 1000) 定義為藍色。</span><span class="sxs-lookup"><span data-stu-id="390ad-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="390ad-199">名義值一律為500。</span><span class="sxs-lookup"><span data-stu-id="390ad-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI \_ DGV \_ SETVIDEO \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="390ad-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="390ad-201">**Mci \_ DGV \_ SETVIDEO \_ 亮度**、 **mci \_ DGV \_ SETVIDEO \_ COLOR**、 **mci \_ DGV \_ SETVIDEO \_ 對比**、 **MCI \_ DGV \_ SETVIDEO \_ GAMMA**、 **MCI \_ DGV \_ SETVIDEO \_ 銳利** 或 **mci DGV SETVIDEO \_ \_ \_ 淡色** 旗標會被修改，因此只會影響顯示的信號，而不會影響所錄製的信號。</span><span class="sxs-lookup"><span data-stu-id="390ad-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="390ad-202">可能的話，這是監視檔案時的預設值。</span><span class="sxs-lookup"><span data-stu-id="390ad-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="390ad-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="390ad-204">轉換長度參數會包含在由 *lpSetVideo* 所識別之結構的 **dwOver** 成員中。</span><span class="sxs-lookup"><span data-stu-id="390ad-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-205">轉換長度會指定以目前時間格式 (的時間長度，) 進行變更所需的時間。</span><span class="sxs-lookup"><span data-stu-id="390ad-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="390ad-206">如果未使用此旗標，則會立即進行變更。</span><span class="sxs-lookup"><span data-stu-id="390ad-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ SETVIDEO \_ 品質</span><span class="sxs-lookup"><span data-stu-id="390ad-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="390ad-208">*LpSetVideo* 所識別之結構的 **lpstrQuality** 成員包含描述影片品質的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="390ad-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="390ad-209">緩衝區中的文字字串會指定影片壓縮演算法的特性。</span><span class="sxs-lookup"><span data-stu-id="390ad-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="390ad-210">您可以使用 **MCI \_ DGV \_ SETVIDEO \_ ALG** 旗標來選取指定演算法的品質描述項。</span><span class="sxs-lookup"><span data-stu-id="390ad-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="390ad-211">如果省略此旗標，則會使用目前的演算法。</span><span class="sxs-lookup"><span data-stu-id="390ad-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="390ad-212">可用的演算法和描述項名稱取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="390ad-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="390ad-213">每個裝置都會提供可用演算法的相關檔，以及適用描述項名稱的描述。</span><span class="sxs-lookup"><span data-stu-id="390ad-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="390ad-214">[MCI \_ QUALITY](mci-quality.md)命令可以定義其他描述項名稱。</span><span class="sxs-lookup"><span data-stu-id="390ad-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="390ad-215">所有裝置都支援描述項「低」、「中」和「高」。</span><span class="sxs-lookup"><span data-stu-id="390ad-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="390ad-216">預設值為 [驅動程式特定]。</span><span class="sxs-lookup"><span data-stu-id="390ad-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI \_ DGV \_ SETVIDEO \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="390ad-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="390ad-218">指定錄製是否包含或排除影片資料。</span><span class="sxs-lookup"><span data-stu-id="390ad-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="390ad-219">當結合的 **MCI \_ 設定 \_** 為時，會記錄影片資料。</span><span class="sxs-lookup"><span data-stu-id="390ad-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="390ad-220">當您 **將 MCI \_ 設定為 \_ OFF** 時，就會排除影片資料。</span><span class="sxs-lookup"><span data-stu-id="390ad-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="390ad-221">預設值包括影片資料。</span><span class="sxs-lookup"><span data-stu-id="390ad-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ SRC \_ NUMBER</span><span class="sxs-lookup"><span data-stu-id="390ad-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="390ad-223">影片來源的數位是在 *lpSetVideo* 所識別之結構的 **dwSourceNumber** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-224">如果 **MCI \_ DGV \_ SETVIDEO \_ 值** 所指定的類型有一個以上的輸入，則值會選取輸入。</span><span class="sxs-lookup"><span data-stu-id="390ad-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="390ad-225">此旗標一律必須搭配 **MCI \_ DGV \_ SETVIDEO \_ 來源** 使用。</span><span class="sxs-lookup"><span data-stu-id="390ad-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="390ad-226">但是，如果已省略 **mci \_ DGV \_ SETVIDEO \_ 值** ，指定的來源編號就會指出要使用的絕對來源，如同 [mci \_ 清單](mci-list.md) 命令中所指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="390ad-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="390ad-228">指定的演算法名稱或品質值適用于靜止影像。</span><span class="sxs-lookup"><span data-stu-id="390ad-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="390ad-229">每個設備磁碟機都必須支援 "none" 演算法，這表示沒有壓縮。</span><span class="sxs-lookup"><span data-stu-id="390ad-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="390ad-230">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="390ad-230">This is the default.</span></span> <span data-ttu-id="390ad-231">在此情況下，數位影片裝置仍會將影像儲存為 RGB 裝置獨立點陣圖， (Dib) 。</span><span class="sxs-lookup"><span data-stu-id="390ad-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="390ad-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI \_ DGV \_ SETVIDEO \_ 值</span><span class="sxs-lookup"><span data-stu-id="390ad-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-233">值會包含在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中。</span><span class="sxs-lookup"><span data-stu-id="390ad-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="390ad-234">值的意義是由 **MCI \_ DGV \_ SETVIDEO \_ 專案** 旗標所指定。</span><span class="sxs-lookup"><span data-stu-id="390ad-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="390ad-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="390ad-236">停用影片輸出。</span><span class="sxs-lookup"><span data-stu-id="390ad-236">Disables video output.</span></span> <span data-ttu-id="390ad-237">針對數位視訊裝置，停用影片會設定 [MCI \_ PUT](mci-put.md) 命令所定義之目的矩形中的圖元 (或其預設值，目前視窗的用戶端區域) 為純色，但不會影響框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="390ad-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="390ad-238">如有需要，您可以使用 [MCI \_ 視窗](mci-window.md) 命令來隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="390ad-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="390ad-239">影片的來源（不論是工作區或外部輸入）可能會繼續將新影像儲存在框架緩衝區中，但在啟用影片之前，不會顯示它們。</span><span class="sxs-lookup"><span data-stu-id="390ad-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="390ad-240">雖然應用程式應該使用 MCI \_ SETVIDEO 命令來控制此功能，但數位視訊裝置仍然必須支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="390ad-241">開啟開啟之後的預設值。</span><span class="sxs-lookup"><span data-stu-id="390ad-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="390ad-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="390ad-243">啟用影片輸出。</span><span class="sxs-lookup"><span data-stu-id="390ad-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="390ad-244">針對數位影片裝置， *lpSetVideo* 參數會指向 [**MCI \_ DGV \_ SETVIDEO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="390ad-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="390ad-245">下列其他旗標會搭配 "vcr" 裝置類型使用：</span><span class="sxs-lookup"><span data-stu-id="390ad-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="390ad-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR \_ SETVIDEO \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="390ad-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="390ad-247">將影片錄製設定為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="390ad-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="390ad-248">搭配下列其中一個旗標使用：</span><span class="sxs-lookup"><span data-stu-id="390ad-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="390ad-249">**MCI \_設定為 \_ ON**。</span><span class="sxs-lookup"><span data-stu-id="390ad-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="390ad-250">錄製影片。</span><span class="sxs-lookup"><span data-stu-id="390ad-250">Video recording on.</span></span>
-   <span data-ttu-id="390ad-251">**MCI \_設定為 \_ OFF**。</span><span class="sxs-lookup"><span data-stu-id="390ad-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="390ad-252">錄製錄影。</span><span class="sxs-lookup"><span data-stu-id="390ad-252">Video recording off.</span></span> <span data-ttu-id="390ad-253">您可能必須先關閉組合錄製 (使用 [mci \_ set](mci-set.md) 命令，並將 [ **mci \_ VCR \_ 組 \_ 組合 \_ 記錄** ] 旗標設為 [關閉]) ，然後才能關閉影片錄製。</span><span class="sxs-lookup"><span data-stu-id="390ad-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ 曲目</span><span class="sxs-lookup"><span data-stu-id="390ad-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="390ad-255">*LpSetVideo* 所識別之結構的 **dwTrack** 成員會指定受命令影響的追蹤。</span><span class="sxs-lookup"><span data-stu-id="390ad-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR \_ SETVIDEO \_ 來源</span><span class="sxs-lookup"><span data-stu-id="390ad-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="390ad-257">設定影片來源，且必須與 **MCI VCR SETVIDEO 搭配使用 \_ \_ \_ 以進行** 旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR \_ SETVIDEO \_ 監視</span><span class="sxs-lookup"><span data-stu-id="390ad-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="390ad-259">設定影片來源監視器，而且必須與 MCI VCR SETVIDEO 搭配使用 \_ \_ \_ 以進行旗標。</span><span class="sxs-lookup"><span data-stu-id="390ad-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="390ad-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_ 至</span><span class="sxs-lookup"><span data-stu-id="390ad-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="390ad-261">*LpSetVideo* 所識別之結構的 **dwTo** 成員包含下列其中一個常數：</span><span class="sxs-lookup"><span data-stu-id="390ad-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="390ad-262">**MCI \_ VCR \_ SRC \_ 類型 \_ 調諧器**</span><span class="sxs-lookup"><span data-stu-id="390ad-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="390ad-263">**MCI \_ VCR \_ SRC \_ 類型 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="390ad-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="390ad-264">**MCI \_ VCR \_ SRC \_ 類型 \_ AUX**</span><span class="sxs-lookup"><span data-stu-id="390ad-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="390ad-265">**MCI \_ VCR \_ SRC \_ 類型 \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="390ad-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="390ad-266">**MCI \_ VCR \_ SRC \_ 類型 \_ 靜音**</span><span class="sxs-lookup"><span data-stu-id="390ad-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="390ad-267">**MCI \_ VCR \_ SRC \_ 類型 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="390ad-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="390ad-268">**MCI \_ VCR \_ SRC \_ 類型 \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="390ad-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="390ad-269">**MCI \_ VCR \_ SETVIDEO \_ 號碼**</span><span class="sxs-lookup"><span data-stu-id="390ad-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="390ad-270">*LpSetVideo* 所識別之結構的 **dwNumber** 成員包含要使用的 **dwTo** 成員) 中所指定類型的影片輸入 (。</span><span class="sxs-lookup"><span data-stu-id="390ad-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="390ad-271">若為 VCR 裝置， *lpSetVideo* 參數會指向 [**MCI \_ VCR \_ SETVIDEO \_ PARMS**](mci-vcr-setvideo-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="390ad-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="390ad-272">規格需求</span><span class="sxs-lookup"><span data-stu-id="390ad-272">Requirements</span></span>



| <span data-ttu-id="390ad-273">需求</span><span class="sxs-lookup"><span data-stu-id="390ad-273">Requirement</span></span> | <span data-ttu-id="390ad-274">值</span><span class="sxs-lookup"><span data-stu-id="390ad-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390ad-275">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="390ad-275">Minimum supported client</span></span><br/> | <span data-ttu-id="390ad-276">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="390ad-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="390ad-277">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="390ad-277">Minimum supported server</span></span><br/> | <span data-ttu-id="390ad-278">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="390ad-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="390ad-279">標頭</span><span class="sxs-lookup"><span data-stu-id="390ad-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="390ad-280"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="390ad-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="390ad-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="390ad-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390ad-282">Mci</span><span class="sxs-lookup"><span data-stu-id="390ad-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="390ad-283">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="390ad-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

