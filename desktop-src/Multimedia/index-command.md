---
title: index 命令
description: Index 命令控制 VCR 的螢幕顯示。 VCR 裝置會辨識此命令。
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- index 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935144"
---
# <a name="index-command"></a><span data-ttu-id="055e5-105">index 命令</span><span class="sxs-lookup"><span data-stu-id="055e5-105">index command</span></span>

<span data-ttu-id="055e5-106">Index 命令控制 VCR 的螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="055e5-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="055e5-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="055e5-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="055e5-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="055e5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="055e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="055e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055e5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="055e5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="055e5-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="055e5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="055e5-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="055e5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="055e5-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span><span class="sxs-lookup"><span data-stu-id="055e5-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="055e5-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="055e5-114">One of the following flags.</span></span>



| <span data-ttu-id="055e5-115">值</span><span class="sxs-lookup"><span data-stu-id="055e5-115">Value</span></span> | <span data-ttu-id="055e5-116">意義</span><span class="sxs-lookup"><span data-stu-id="055e5-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="055e5-117">關</span><span class="sxs-lookup"><span data-stu-id="055e5-117">off</span></span>   | <span data-ttu-id="055e5-118">關閉螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="055e5-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="055e5-119">on</span><span class="sxs-lookup"><span data-stu-id="055e5-119">on</span></span>    | <span data-ttu-id="055e5-120">開啟螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="055e5-120">Turns on the on-screen display.</span></span> <span data-ttu-id="055e5-121">要顯示的專案是由 [set](set.md) 命令的「index」旗標所指定。</span><span class="sxs-lookup"><span data-stu-id="055e5-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="055e5-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="055e5-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="055e5-123">可以是「等候」、「通知」或「測試」。</span><span class="sxs-lookup"><span data-stu-id="055e5-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="055e5-124">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="055e5-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055e5-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="055e5-125">Return Value</span></span>

<span data-ttu-id="055e5-126">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="055e5-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="055e5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="055e5-127">Requirements</span></span>



| <span data-ttu-id="055e5-128">需求</span><span class="sxs-lookup"><span data-stu-id="055e5-128">Requirement</span></span> | <span data-ttu-id="055e5-129">值</span><span class="sxs-lookup"><span data-stu-id="055e5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="055e5-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="055e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="055e5-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="055e5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="055e5-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="055e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="055e5-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="055e5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="055e5-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="055e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055e5-135">Mci</span><span class="sxs-lookup"><span data-stu-id="055e5-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="055e5-136">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="055e5-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="055e5-137">set</span><span class="sxs-lookup"><span data-stu-id="055e5-137">set</span></span>](set.md)
</dt> </dl>

 

