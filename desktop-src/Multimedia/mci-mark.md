---
title: 'MCI_MARK 命令 (Mmsystem .h) '
description: MCI \_ MARK 命令會記錄或清除可與 MCI \_ 搜尋命令搭配使用以進行高速搜尋的標記。 VCR 裝置會辨識此命令。
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024787"
---
# <a name="mci_mark-command"></a><span data-ttu-id="b8184-105">MCI \_ MARK 命令</span><span class="sxs-lookup"><span data-stu-id="b8184-105">MCI\_MARK command</span></span>

<span data-ttu-id="b8184-106">MCI \_ MARK 命令會記錄或清除可與 [MCI \_ 搜尋](mci-seek.md) 命令搭配使用以進行高速搜尋的標記。</span><span class="sxs-lookup"><span data-stu-id="b8184-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="b8184-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="b8184-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="b8184-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="b8184-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="b8184-109">參數</span><span class="sxs-lookup"><span data-stu-id="b8184-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8184-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b8184-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b8184-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8184-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b8184-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b8184-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b8184-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="b8184-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="b8184-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="b8184-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8184-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span><span class="sxs-lookup"><span data-stu-id="b8184-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="b8184-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b8184-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b8184-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="b8184-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8184-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8184-118">Return Value</span></span>

<span data-ttu-id="b8184-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8184-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8184-120">備註</span><span class="sxs-lookup"><span data-stu-id="b8184-120">Remarks</span></span>

<span data-ttu-id="b8184-121">下列其他旗標適用于 VCR 裝置：</span><span class="sxs-lookup"><span data-stu-id="b8184-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="b8184-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI \_ VCR \_ 標示 \_ 清除</span><span class="sxs-lookup"><span data-stu-id="b8184-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="b8184-123">清除目前位置的標記（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b8184-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="b8184-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI \_ VCR \_ 標示 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="b8184-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="b8184-125">在目前位置寫入標記。</span><span class="sxs-lookup"><span data-stu-id="b8184-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8184-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8184-126">Requirements</span></span>



| <span data-ttu-id="b8184-127">需求</span><span class="sxs-lookup"><span data-stu-id="b8184-127">Requirement</span></span> | <span data-ttu-id="b8184-128">值</span><span class="sxs-lookup"><span data-stu-id="b8184-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8184-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8184-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b8184-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8184-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8184-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8184-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b8184-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8184-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8184-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b8184-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8184-134"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b8184-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8184-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8184-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8184-136">Mci</span><span class="sxs-lookup"><span data-stu-id="b8184-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b8184-137">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="b8184-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

