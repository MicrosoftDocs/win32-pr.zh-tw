---
title: 'MCI_ESCAPE 命令 (Mmsystem .h) '
description: MCI \_ ESCAPE 命令會將字串直接傳送至裝置。 Videodisc 裝置會辨識此命令。
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- MCI_ESCAPE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968169"
---
# <a name="mci_escape-command"></a><span data-ttu-id="ff548-105">MCI \_ ESCAPE 命令</span><span class="sxs-lookup"><span data-stu-id="ff548-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="ff548-106">MCI \_ ESCAPE 命令會將字串直接傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="ff548-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="ff548-107">Videodisc 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="ff548-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="ff548-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="ff548-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="ff548-109">參數</span><span class="sxs-lookup"><span data-stu-id="ff548-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff548-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ff548-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ff548-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff548-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ff548-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ff548-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ff548-113">MCI \_ 通知或 mci \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="ff548-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="ff548-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ff548-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff548-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span><span class="sxs-lookup"><span data-stu-id="ff548-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="ff548-116">[**MCI \_ VD \_ ESCAPE \_ PARMS**](mci-vd-escape-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ff548-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff548-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff548-117">Return Value</span></span>

<span data-ttu-id="ff548-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff548-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff548-119">備註</span><span class="sxs-lookup"><span data-stu-id="ff548-119">Remarks</span></span>

<span data-ttu-id="ff548-120">使用 MCI ESCAPE 傳送的資料 \_ 會與裝置相依，而且通常會直接傳遞給與裝置相關聯的硬體。</span><span class="sxs-lookup"><span data-stu-id="ff548-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="ff548-121">下列其他旗標適用于 videodisc 裝置：</span><span class="sxs-lookup"><span data-stu-id="ff548-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="ff548-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI \_ VD \_ ESCAPE \_ 字串</span><span class="sxs-lookup"><span data-stu-id="ff548-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="ff548-123">命令字串是在 *lpEscape* 所識別之結構的 **lpstrCommand** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="ff548-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="ff548-124">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="ff548-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff548-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff548-125">Requirements</span></span>



| <span data-ttu-id="ff548-126">需求</span><span class="sxs-lookup"><span data-stu-id="ff548-126">Requirement</span></span> | <span data-ttu-id="ff548-127">值</span><span class="sxs-lookup"><span data-stu-id="ff548-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff548-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff548-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff548-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff548-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff548-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff548-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff548-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff548-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff548-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ff548-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff548-133"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ff548-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff548-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff548-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff548-135">Mci</span><span class="sxs-lookup"><span data-stu-id="ff548-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ff548-136">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="ff548-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

