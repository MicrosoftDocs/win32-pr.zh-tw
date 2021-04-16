---
title: 'MCI_QUALITY 命令 (Mmsystem .h) '
description: MCI \_ quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383854"
---
# <a name="mci_quality-command"></a><span data-ttu-id="6da1c-105">MCI \_ 品質命令</span><span class="sxs-lookup"><span data-stu-id="6da1c-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="6da1c-106">MCI \_ quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。</span><span class="sxs-lookup"><span data-stu-id="6da1c-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="6da1c-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6da1c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6da1c-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="6da1c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="6da1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="6da1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da1c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6da1c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6da1c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6da1c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="6da1c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6da1c-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6da1c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span><span class="sxs-lookup"><span data-stu-id="6da1c-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-116">[**MCI \_ DGV \_ QUALITY \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6da1c-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da1c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6da1c-117">Return Value</span></span>

<span data-ttu-id="6da1c-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da1c-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6da1c-119">備註</span><span class="sxs-lookup"><span data-stu-id="6da1c-119">Remarks</span></span>

<span data-ttu-id="6da1c-120">使用 [mci \_ SETAUDIO](mci-setaudio.md) 和 [mci \_ SETVIDEO](mci-setvideo.md) 命令設定音訊、影片或仍有品質時，可使用為此品質層級定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="6da1c-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="6da1c-121">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="6da1c-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="6da1c-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ 品質 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="6da1c-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-123">*LpQuality* 所識別之結構的 **lpstrAlgorithm** 成員包含包含演算法名稱的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="6da1c-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="6da1c-124">設備磁碟機必須支援此演算法，且必須與使用的音訊、仍然或影片描述項相容。</span><span class="sxs-lookup"><span data-stu-id="6da1c-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="6da1c-125">如果省略此旗標，則會使用目前的演算法。</span><span class="sxs-lookup"><span data-stu-id="6da1c-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI \_ 品質 \_ 對話方塊</span><span class="sxs-lookup"><span data-stu-id="6da1c-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-127">設備磁碟機應該會顯示用來指定品質層級的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6da1c-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="6da1c-128">此對話方塊包含設備磁碟機內部所使用的演算法特定欄位，以建立描述特定品質層級的結構。</span><span class="sxs-lookup"><span data-stu-id="6da1c-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI \_ 品質 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="6da1c-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-130">*LpQuality* 所識別之結構的 **dwHandle** 成員包含結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da1c-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="6da1c-131">結構包含描述特定品質層級的演算法特定資料。</span><span class="sxs-lookup"><span data-stu-id="6da1c-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="6da1c-132">演算法的結構格式取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="6da1c-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI \_ 品質 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="6da1c-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-134">常數，表示演算法的類型會包含在 *lpQuality* 所識別之結構的 **dwItem** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6da1c-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="6da1c-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI \_ 品質 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="6da1c-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="6da1c-136">*LpQuality* 所識別之結構的 **lpstrName** 成員包含包含品質描述項的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="6da1c-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6da1c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6da1c-137">Requirements</span></span>



| <span data-ttu-id="6da1c-138">需求</span><span class="sxs-lookup"><span data-stu-id="6da1c-138">Requirement</span></span> | <span data-ttu-id="6da1c-139">值</span><span class="sxs-lookup"><span data-stu-id="6da1c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da1c-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6da1c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6da1c-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da1c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6da1c-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6da1c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6da1c-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da1c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6da1c-144">標頭</span><span class="sxs-lookup"><span data-stu-id="6da1c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6da1c-145"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6da1c-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da1c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6da1c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da1c-147">Mci</span><span class="sxs-lookup"><span data-stu-id="6da1c-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6da1c-148">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="6da1c-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

