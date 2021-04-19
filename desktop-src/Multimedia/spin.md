---
title: 微調命令
description: 微調命令會開始旋轉光碟或停止光碟的旋轉。 Videodisc 裝置會辨識此命令。
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- 微調命令 Windows 多媒體
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966510"
---
# <a name="spin-command"></a><span data-ttu-id="90a1b-105">微調命令</span><span class="sxs-lookup"><span data-stu-id="90a1b-105">spin command</span></span>

<span data-ttu-id="90a1b-106">微調命令會開始旋轉光碟或停止光碟的旋轉。</span><span class="sxs-lookup"><span data-stu-id="90a1b-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="90a1b-107">Videodisc 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="90a1b-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="90a1b-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="90a1b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="90a1b-109">參數</span><span class="sxs-lookup"><span data-stu-id="90a1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a1b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="90a1b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="90a1b-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="90a1b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="90a1b-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="90a1b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="90a1b-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span><span class="sxs-lookup"><span data-stu-id="90a1b-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="90a1b-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="90a1b-114">One of the following flags.</span></span>



| <span data-ttu-id="90a1b-115">值</span><span class="sxs-lookup"><span data-stu-id="90a1b-115">Value</span></span> | <span data-ttu-id="90a1b-116">意義</span><span class="sxs-lookup"><span data-stu-id="90a1b-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="90a1b-117">機</span><span class="sxs-lookup"><span data-stu-id="90a1b-117">down</span></span>  | <span data-ttu-id="90a1b-118">停止光碟的旋轉。</span><span class="sxs-lookup"><span data-stu-id="90a1b-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="90a1b-119">啟動</span><span class="sxs-lookup"><span data-stu-id="90a1b-119">up</span></span>    | <span data-ttu-id="90a1b-120">開始旋轉光碟。</span><span class="sxs-lookup"><span data-stu-id="90a1b-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="90a1b-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="90a1b-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="90a1b-122">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="90a1b-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="90a1b-123">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="90a1b-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a1b-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="90a1b-124">Return Value</span></span>

<span data-ttu-id="90a1b-125">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="90a1b-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="90a1b-126">範例</span><span class="sxs-lookup"><span data-stu-id="90a1b-126">Examples</span></span>

<span data-ttu-id="90a1b-127">下列命令會開始旋轉 videodisc 裝置。</span><span class="sxs-lookup"><span data-stu-id="90a1b-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="90a1b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="90a1b-128">Requirements</span></span>



| <span data-ttu-id="90a1b-129">需求</span><span class="sxs-lookup"><span data-stu-id="90a1b-129">Requirement</span></span> | <span data-ttu-id="90a1b-130">值</span><span class="sxs-lookup"><span data-stu-id="90a1b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90a1b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90a1b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="90a1b-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a1b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90a1b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90a1b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="90a1b-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a1b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="90a1b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90a1b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a1b-136">Mci</span><span class="sxs-lookup"><span data-stu-id="90a1b-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="90a1b-137">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="90a1b-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

