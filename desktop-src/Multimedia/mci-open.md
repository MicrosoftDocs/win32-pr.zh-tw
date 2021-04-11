---
title: 'MCI_OPEN 命令 (Mmsystem .h) '
description: MCI \_ OPEN 命令會初始化裝置或檔案。 所有裝置都會辨識此命令。
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843044"
---
# <a name="mci_open-command"></a><span data-ttu-id="5584c-105">MCI \_ 開啟命令</span><span class="sxs-lookup"><span data-stu-id="5584c-105">MCI\_OPEN command</span></span>

<span data-ttu-id="5584c-106">MCI \_ OPEN 命令會初始化裝置或檔案。</span><span class="sxs-lookup"><span data-stu-id="5584c-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="5584c-107">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="5584c-107">All devices recognize this command.</span></span>

<span data-ttu-id="5584c-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="5584c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="5584c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5584c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5584c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5584c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5584c-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5584c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5584c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5584c-113">MCI \_ 通知或 mci \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="5584c-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="5584c-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="5584c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5584c-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span><span class="sxs-lookup"><span data-stu-id="5584c-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="5584c-116">[**MCI \_ 開啟 \_ PARMS**](mci-open-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5584c-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="5584c-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="5584c-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5584c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5584c-118">Return Value</span></span>

<span data-ttu-id="5584c-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5584c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5584c-120">備註</span><span class="sxs-lookup"><span data-stu-id="5584c-120">Remarks</span></span>

<span data-ttu-id="5584c-121">\_ \_ 只要在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函式中指定了裝置，就必須使用 MCI 開啟類型旗標。</span><span class="sxs-lookup"><span data-stu-id="5584c-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="5584c-122">如果您指定裝置類型常數來開啟裝置， \_ \_ \_ 除了 mci \_ 開啟 \_ 類型之外，您還必須指定 mci 開啟類型識別碼旗標。</span><span class="sxs-lookup"><span data-stu-id="5584c-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="5584c-123">如需裝置類型常數的清單，請參閱 [MCI 裝置類型](mci-device-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5584c-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="5584c-124">如果在 \_ \_ 一開始開啟裝置或檔案時未指定 mci open 可共用旗標，則所有後續 \_ 的 mci 會開啟裝置或檔案的命令將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5584c-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="5584c-125">如果裝置或檔案已經開啟，而且未指定此旗標，即使第一個開啟的命令指定的 MCI 開啟可共用，呼叫也會失敗 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5584c-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="5584c-126">針對 MCISEQ 開啟的檔案。WINSPOOL.DRV 和 MCIWAVE。WINSPOOL.DRV 裝置為 nonsharable。</span><span class="sxs-lookup"><span data-stu-id="5584c-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="5584c-127">裝置名稱中會忽略大小寫，但不能有開頭或尾端空白。</span><span class="sxs-lookup"><span data-stu-id="5584c-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="5584c-128">若要透過登錄) 中的專案來使用自動類型選取 (，請將檔案名和副檔名指派給 *lpOpen* 所識別之結構的 **lpstrElementName** 成員、將 **lpstrDeviceType** 成員設為 **Null**，並設定 MCI \_ OPEN \_ 元素旗標。</span><span class="sxs-lookup"><span data-stu-id="5584c-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="5584c-129">下列其他旗標適用于所有支援開啟 MCI 的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="5584c-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="5584c-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ 開啟 \_ 別名</span><span class="sxs-lookup"><span data-stu-id="5584c-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="5584c-131">別名會包含在 *lpOpen* 所識別之結構的 **lpstrAlias** 成員中。</span><span class="sxs-lookup"><span data-stu-id="5584c-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_開啟 \_ 共用的 MCI</span><span class="sxs-lookup"><span data-stu-id="5584c-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="5584c-133">裝置或檔案應開啟為可共用。</span><span class="sxs-lookup"><span data-stu-id="5584c-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ 開啟 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="5584c-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="5584c-135">裝置類型名稱或常數會包含在由 *lpOpen* 所識別之結構的 **lpstrDeviceType** 成員中。</span><span class="sxs-lookup"><span data-stu-id="5584c-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI \_ 開啟 \_ 類型 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="5584c-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="5584c-137">由 *lpOpen* 所識別之結構的 **lpstrDeviceType** 成員的低序位文字包含標準的 MCI 裝置類型識別碼，而高序位字則選擇性地包含裝置的序數索引。</span><span class="sxs-lookup"><span data-stu-id="5584c-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="5584c-138">使用此旗標搭配 MCI \_ 開啟 \_ 類型旗標。</span><span class="sxs-lookup"><span data-stu-id="5584c-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="5584c-139">下列其他旗標適用于複合裝置：</span><span class="sxs-lookup"><span data-stu-id="5584c-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="5584c-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ OPEN \_ 元素</span><span class="sxs-lookup"><span data-stu-id="5584c-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="5584c-141">檔案名會包含在 *lpOpen* 所識別之結構的 **lpstrElementName** 成員中。</span><span class="sxs-lookup"><span data-stu-id="5584c-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI \_ 開啟 \_ 元素 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="5584c-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="5584c-143">*LpOpen* 所識別之結構的 **lpstrElementName** 成員會被解釋為 **DWORD** 值，而且具有裝置內部的意義。</span><span class="sxs-lookup"><span data-stu-id="5584c-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="5584c-144">使用此旗標搭配 MCI \_ OPEN \_ 元素旗標。</span><span class="sxs-lookup"><span data-stu-id="5584c-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="5584c-145">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="5584c-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5584c-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC</span><span class="sxs-lookup"><span data-stu-id="5584c-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="5584c-147">裝置應該減少在調色板中的靜態 (系統) 色彩數目。</span><span class="sxs-lookup"><span data-stu-id="5584c-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="5584c-148">這會增加可用於轉譯影片資料流程的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="5584c-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="5584c-149">此旗標只適用于與 Windows 共用調色板的裝置。</span><span class="sxs-lookup"><span data-stu-id="5584c-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ 開啟 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="5584c-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="5584c-151">父視窗控制碼是在 *lpOpen* 所識別之結構的 **hWndParent** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="5584c-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ 開啟 \_ WS</span><span class="sxs-lookup"><span data-stu-id="5584c-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="5584c-153">視窗樣式是在 *lpOpen* 所識別之結構的 **dwStyle** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="5584c-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT</span><span class="sxs-lookup"><span data-stu-id="5584c-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="5584c-155">指出16位 MCI 裝置支援的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="5584c-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ 開啟 \_ 32 位</span><span class="sxs-lookup"><span data-stu-id="5584c-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="5584c-157">指出32位 MCI 裝置支援的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="5584c-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="5584c-158">針對數位影片裝置， *lpOpen* 參數會指向 [**MCI \_ DGV \_ OPEN \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="5584c-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="5584c-159">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="5584c-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5584c-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ 開啟 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="5584c-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="5584c-161">父視窗控制碼是在 *lpOpen* 所識別之結構的 **hWndParent** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="5584c-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="5584c-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ 開啟 \_ WS</span><span class="sxs-lookup"><span data-stu-id="5584c-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="5584c-163">視窗樣式是在 *lpOpen* 所識別之結構的 **dwStyle** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="5584c-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="5584c-164">**DwStyle** 值會指定驅動程式將建立之視窗的樣式，並在應用程式未提供時加以顯示。</span><span class="sxs-lookup"><span data-stu-id="5584c-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="5584c-165">Style 參數會採用定義視窗樣式的整數。</span><span class="sxs-lookup"><span data-stu-id="5584c-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="5584c-166">這些常數與標準視窗樣式相同 (例如 WS \_ CHILD、ws \_ OVERLAPPEDWINDOW 或 ws \_ POPUP) 。</span><span class="sxs-lookup"><span data-stu-id="5584c-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="5584c-167">針對影片重迭裝置， *lpOpen* 參數會指向 [**MCI \_ OVLY \_ OPEN \_ PARMS**](mci-ovly-open-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5584c-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="5584c-168">下列其他旗標適用于 **waveaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="5584c-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5584c-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI \_ WAVE \_ 開啟 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="5584c-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="5584c-170">緩衝區長度是在 *lpOpen* 所識別之結構的 **dwBufferSeconds** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="5584c-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="5584c-171">針對波形音訊裝置， *lpOpen* 參數會指向 [**MCI \_ WAVE \_ 開啟 \_ PARMS**](mci-wave-open-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5584c-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="5584c-172">MCIWAVE 驅動程式需要非同步波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="5584c-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="5584c-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="5584c-173">Requirements</span></span>



| <span data-ttu-id="5584c-174">需求</span><span class="sxs-lookup"><span data-stu-id="5584c-174">Requirement</span></span> | <span data-ttu-id="5584c-175">值</span><span class="sxs-lookup"><span data-stu-id="5584c-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5584c-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5584c-176">Minimum supported client</span></span><br/> | <span data-ttu-id="5584c-177">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5584c-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5584c-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5584c-178">Minimum supported server</span></span><br/> | <span data-ttu-id="5584c-179">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5584c-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5584c-180">標頭</span><span class="sxs-lookup"><span data-stu-id="5584c-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="5584c-181"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5584c-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5584c-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5584c-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5584c-183">Mci</span><span class="sxs-lookup"><span data-stu-id="5584c-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5584c-184">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="5584c-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

