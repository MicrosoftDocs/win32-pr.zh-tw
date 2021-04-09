---
title: 'MCI_RESTORE 命令 (Mmsystem .h) '
description: MCI \_ RESTORE 命令會將點陣圖從檔案複製到框架緩衝區。 數位影片裝置辨識此命令。 此命令會執行 MCI CAPTURE 命令的相反動作 \_ 。
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686235"
---
# <a name="mci_restore-command"></a><span data-ttu-id="78de5-106">MCI \_ 還原命令</span><span class="sxs-lookup"><span data-stu-id="78de5-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="78de5-107">MCI \_ RESTORE 命令會將點陣圖從檔案複製到框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="78de5-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="78de5-108">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="78de5-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="78de5-109">此命令會執行 [MCI \_ CAPTURE](mci-capture.md) 命令的相反動作。</span><span class="sxs-lookup"><span data-stu-id="78de5-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="78de5-110">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="78de5-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="78de5-111">參數</span><span class="sxs-lookup"><span data-stu-id="78de5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78de5-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="78de5-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="78de5-113">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="78de5-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="78de5-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="78de5-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78de5-115">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="78de5-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="78de5-116">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="78de5-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="78de5-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span><span class="sxs-lookup"><span data-stu-id="78de5-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="78de5-118">[**MCI \_ DGV \_ RESTORE \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="78de5-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78de5-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="78de5-119">Return Value</span></span>

<span data-ttu-id="78de5-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="78de5-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="78de5-121">備註</span><span class="sxs-lookup"><span data-stu-id="78de5-121">Remarks</span></span>

<span data-ttu-id="78de5-122">此執行可辨識各種不同的影像格式，但一律接受 Windows 裝置獨立點陣圖 (DIB) 。</span><span class="sxs-lookup"><span data-stu-id="78de5-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="78de5-123">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="78de5-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="78de5-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI \_ DGV \_ 還原 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="78de5-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="78de5-125">*LpRestore* 所識別之結構的 **lpstrFileName** 成員包含包含來原始檔案名的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="78de5-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="78de5-126">需要檔案名。</span><span class="sxs-lookup"><span data-stu-id="78de5-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="78de5-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI \_ DGV \_ RESTORE \_ AT</span><span class="sxs-lookup"><span data-stu-id="78de5-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="78de5-128">*LpRestore* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="78de5-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="78de5-129">矩形會指定框架緩衝區相對於其來源的區域。</span><span class="sxs-lookup"><span data-stu-id="78de5-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="78de5-130">第一對座標指定矩形的左上角;第二個配對指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="78de5-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="78de5-131">如果未指定此旗標，則會將影像複製到框架緩衝區的左上角。</span><span class="sxs-lookup"><span data-stu-id="78de5-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78de5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="78de5-132">Requirements</span></span>



| <span data-ttu-id="78de5-133">需求</span><span class="sxs-lookup"><span data-stu-id="78de5-133">Requirement</span></span> | <span data-ttu-id="78de5-134">值</span><span class="sxs-lookup"><span data-stu-id="78de5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78de5-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78de5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="78de5-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78de5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78de5-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78de5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="78de5-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78de5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78de5-139">標頭</span><span class="sxs-lookup"><span data-stu-id="78de5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="78de5-140"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="78de5-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78de5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78de5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78de5-142">Mci</span><span class="sxs-lookup"><span data-stu-id="78de5-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="78de5-143">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="78de5-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

