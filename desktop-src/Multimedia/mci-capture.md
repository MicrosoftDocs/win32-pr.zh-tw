---
title: 'MCI_CAPTURE 命令 (Mmsystem .h) '
description: MCI \_ CAPTURE 命令會捕獲框架緩衝區的內容，並將其儲存在指定的檔案中。 數位影片裝置辨識此命令。
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934687"
---
# <a name="mci_capture-command"></a><span data-ttu-id="bfc88-105">MCI \_ CAPTURE 命令</span><span class="sxs-lookup"><span data-stu-id="bfc88-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="bfc88-106">MCI \_ CAPTURE 命令會捕獲框架緩衝區的內容，並將其儲存在指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="bfc88-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="bfc88-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="bfc88-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="bfc88-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="bfc88-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="bfc88-109">參數</span><span class="sxs-lookup"><span data-stu-id="bfc88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc88-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bfc88-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bfc88-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bfc88-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bfc88-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bfc88-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bfc88-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="bfc88-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="bfc88-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="bfc88-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfc88-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span><span class="sxs-lookup"><span data-stu-id="bfc88-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="bfc88-116">[**MCI \_ DGV \_ CAPTURE \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bfc88-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc88-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfc88-117">Return Value</span></span>

<span data-ttu-id="bfc88-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bfc88-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc88-119">備註</span><span class="sxs-lookup"><span data-stu-id="bfc88-119">Remarks</span></span>

<span data-ttu-id="bfc88-120">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="bfc88-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="bfc88-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ CAPTURE \_ AS</span><span class="sxs-lookup"><span data-stu-id="bfc88-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="bfc88-122">*LpCapture* 所識別之結構的 **lpstrFileName** 成員包含指定目的地路徑和檔案名的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="bfc88-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="bfc88-123"> (此旗標為必要項。 ) </span><span class="sxs-lookup"><span data-stu-id="bfc88-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="bfc88-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV \_ CAPTURE \_ AT</span><span class="sxs-lookup"><span data-stu-id="bfc88-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="bfc88-125">*LpCapture* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="bfc88-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="bfc88-126">矩形會指定框架緩衝區內裁剪並儲存至磁片的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="bfc88-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="bfc88-127">如果省略，則裁剪的區域預設為先前的 [MCI \_ PUT](mci-put.md) 命令所指定或預設的矩形，此命令會指定設備磁碟機實例的來源區域。</span><span class="sxs-lookup"><span data-stu-id="bfc88-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfc88-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfc88-128">Requirements</span></span>



| <span data-ttu-id="bfc88-129">需求</span><span class="sxs-lookup"><span data-stu-id="bfc88-129">Requirement</span></span> | <span data-ttu-id="bfc88-130">值</span><span class="sxs-lookup"><span data-stu-id="bfc88-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc88-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfc88-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc88-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfc88-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bfc88-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfc88-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc88-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfc88-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bfc88-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bfc88-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc88-136"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bfc88-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfc88-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfc88-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc88-138">Mci</span><span class="sxs-lookup"><span data-stu-id="bfc88-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bfc88-139">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="bfc88-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

