---
title: 'MCI_SETTIMECODE 命令 (Mmsystem .h) '
description: MCI \_ SETTIMECODE 命令會啟用或停用 VCR 的時間碼記錄。 VCR 裝置會辨識此命令。
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- MCI_SETTIMECODE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991313"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="3b654-105">MCI \_ SETTIMECODE 命令</span><span class="sxs-lookup"><span data-stu-id="3b654-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="3b654-106">MCI \_ SETTIMECODE 命令會啟用或停用 VCR 的時間碼記錄。</span><span class="sxs-lookup"><span data-stu-id="3b654-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="3b654-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="3b654-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="3b654-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="3b654-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="3b654-109">參數</span><span class="sxs-lookup"><span data-stu-id="3b654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b654-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3b654-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3b654-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b654-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3b654-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3b654-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3b654-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="3b654-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="3b654-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="3b654-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b654-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span><span class="sxs-lookup"><span data-stu-id="3b654-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="3b654-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3b654-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="3b654-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="3b654-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b654-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b654-118">Return Value</span></span>

<span data-ttu-id="3b654-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b654-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b654-120">備註</span><span class="sxs-lookup"><span data-stu-id="3b654-120">Remarks</span></span>

<span data-ttu-id="3b654-121">下列其他旗標適用于 VCR 裝置：</span><span class="sxs-lookup"><span data-stu-id="3b654-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="3b654-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI \_ VCR \_ SETTIMECODE \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="3b654-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="3b654-123">將時間碼播放軌錄製設定為 on 或 off。</span><span class="sxs-lookup"><span data-stu-id="3b654-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="3b654-124">此旗標會搭配下列其中一個其他旗標使用：</span><span class="sxs-lookup"><span data-stu-id="3b654-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="3b654-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="3b654-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="3b654-126">記錄時間碼記錄。</span><span class="sxs-lookup"><span data-stu-id="3b654-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="3b654-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="3b654-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="3b654-128">關閉時間碼記錄。</span><span class="sxs-lookup"><span data-stu-id="3b654-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b654-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b654-129">Requirements</span></span>



| <span data-ttu-id="3b654-130">需求</span><span class="sxs-lookup"><span data-stu-id="3b654-130">Requirement</span></span> | <span data-ttu-id="3b654-131">值</span><span class="sxs-lookup"><span data-stu-id="3b654-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b654-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b654-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3b654-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b654-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3b654-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b654-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3b654-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b654-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3b654-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3b654-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b654-137"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3b654-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b654-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b654-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b654-139">Mci</span><span class="sxs-lookup"><span data-stu-id="3b654-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3b654-140">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="3b654-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

