---
title: 'MCI_INDEX 命令 (Mmsystem .h) '
description: MCI \_ INDEX 命令會開啟或關閉螢幕上的顯示。 VCR 裝置會辨識此命令。
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- MCI_INDEX 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106205"
---
# <a name="mci_index-command"></a><span data-ttu-id="229ea-105">MCI \_ 索引命令</span><span class="sxs-lookup"><span data-stu-id="229ea-105">MCI\_INDEX command</span></span>

<span data-ttu-id="229ea-106">MCI \_ INDEX 命令會開啟或關閉螢幕上的顯示。</span><span class="sxs-lookup"><span data-stu-id="229ea-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="229ea-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="229ea-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="229ea-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="229ea-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="229ea-109">參數</span><span class="sxs-lookup"><span data-stu-id="229ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229ea-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="229ea-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="229ea-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="229ea-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="229ea-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="229ea-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="229ea-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="229ea-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="229ea-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="229ea-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="229ea-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span><span class="sxs-lookup"><span data-stu-id="229ea-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="229ea-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="229ea-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="229ea-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="229ea-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="229ea-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="229ea-118">Return Value</span></span>

<span data-ttu-id="229ea-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="229ea-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="229ea-120">備註</span><span class="sxs-lookup"><span data-stu-id="229ea-120">Remarks</span></span>

<span data-ttu-id="229ea-121">畫面上顯示的資訊是由 \_ \_ \_ [mci \_ set](mci-set.md) 命令中的 mci VCR set 索引旗標所控制。</span><span class="sxs-lookup"><span data-stu-id="229ea-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="229ea-122">下列其他旗標適用于 VCR 裝置：</span><span class="sxs-lookup"><span data-stu-id="229ea-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="229ea-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="229ea-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="229ea-124">開啟螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="229ea-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="229ea-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="229ea-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="229ea-126">開啟螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="229ea-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="229ea-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="229ea-127">Requirements</span></span>



| <span data-ttu-id="229ea-128">需求</span><span class="sxs-lookup"><span data-stu-id="229ea-128">Requirement</span></span> | <span data-ttu-id="229ea-129">值</span><span class="sxs-lookup"><span data-stu-id="229ea-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="229ea-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="229ea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="229ea-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="229ea-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="229ea-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="229ea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="229ea-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="229ea-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="229ea-134">標頭</span><span class="sxs-lookup"><span data-stu-id="229ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="229ea-135"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="229ea-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229ea-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="229ea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229ea-137">Mci</span><span class="sxs-lookup"><span data-stu-id="229ea-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="229ea-138">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="229ea-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

