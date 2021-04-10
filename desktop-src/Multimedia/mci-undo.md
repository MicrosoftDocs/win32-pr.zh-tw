---
title: 'MCI_UNDO 命令 (Mmsystem .h) '
description: MCI \_ 復原命令會反轉最新成功的 mci \_ 剪下、mci \_ 複製、MCI \_ 刪除或 MCI \_ 貼上命令。 數位影片裝置辨識此命令。
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- MCI_UNDO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024709"
---
# <a name="mci_undo-command"></a><span data-ttu-id="d27c8-105">MCI \_ 復原命令</span><span class="sxs-lookup"><span data-stu-id="d27c8-105">MCI\_UNDO command</span></span>

<span data-ttu-id="d27c8-106">MCI \_ 復原命令會反轉最新成功的 [mci \_ 剪](mci-cut.md)下 [、mci \_ 複製](mci-copy.md)、 [mci \_ 刪除](mci-delete.md)或 [MCI \_ 貼](mci-paste.md) 上命令。</span><span class="sxs-lookup"><span data-stu-id="d27c8-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="d27c8-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="d27c8-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d27c8-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="d27c8-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="d27c8-109">參數</span><span class="sxs-lookup"><span data-stu-id="d27c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27c8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d27c8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d27c8-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d27c8-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d27c8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d27c8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d27c8-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="d27c8-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d27c8-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="d27c8-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d27c8-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span><span class="sxs-lookup"><span data-stu-id="d27c8-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="d27c8-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d27c8-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="d27c8-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="d27c8-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27c8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d27c8-118">Return Value</span></span>

<span data-ttu-id="d27c8-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d27c8-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27c8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d27c8-120">Requirements</span></span>



| <span data-ttu-id="d27c8-121">需求</span><span class="sxs-lookup"><span data-stu-id="d27c8-121">Requirement</span></span> | <span data-ttu-id="d27c8-122">值</span><span class="sxs-lookup"><span data-stu-id="d27c8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27c8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d27c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d27c8-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d27c8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d27c8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d27c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d27c8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d27c8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d27c8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d27c8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d27c8-128"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d27c8-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27c8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d27c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27c8-130">Mci</span><span class="sxs-lookup"><span data-stu-id="d27c8-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d27c8-131">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="d27c8-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

