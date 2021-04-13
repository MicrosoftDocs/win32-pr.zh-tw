---
title: 'MCI_CONFIGURE 命令 (Mmsystem .h) '
description: '[MCI \_ 設定] 命令會顯示用來設定作業選項的對話方塊。 數位影片裝置辨識此命令。'
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- MCI_CONFIGURE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383982"
---
# <a name="mci_configure-command"></a><span data-ttu-id="b02df-105">MCI \_ 設定命令</span><span class="sxs-lookup"><span data-stu-id="b02df-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="b02df-106">[MCI \_ 設定] 命令會顯示用來設定作業選項的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b02df-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="b02df-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="b02df-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="b02df-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="b02df-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="b02df-109">參數</span><span class="sxs-lookup"><span data-stu-id="b02df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02df-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b02df-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b02df-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b02df-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b02df-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b02df-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b02df-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="b02df-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="b02df-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="b02df-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02df-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span><span class="sxs-lookup"><span data-stu-id="b02df-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="b02df-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b02df-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b02df-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="b02df-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02df-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b02df-118">Return Value</span></span>

<span data-ttu-id="b02df-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b02df-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02df-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b02df-120">Requirements</span></span>



| <span data-ttu-id="b02df-121">需求</span><span class="sxs-lookup"><span data-stu-id="b02df-121">Requirement</span></span> | <span data-ttu-id="b02df-122">值</span><span class="sxs-lookup"><span data-stu-id="b02df-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02df-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b02df-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b02df-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b02df-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b02df-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b02df-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b02df-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b02df-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b02df-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b02df-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02df-128"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b02df-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02df-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b02df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02df-130">Mci</span><span class="sxs-lookup"><span data-stu-id="b02df-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b02df-131">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="b02df-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

