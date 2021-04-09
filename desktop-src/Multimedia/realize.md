---
title: 實現命令
description: 「實現」命令會指示裝置在顯示的視窗中，選取並實現其調色板的顯示內容。 數位影片裝置辨識此命令。
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- 實現命令 Windows 多媒體
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934936"
---
# <a name="realize-command"></a><span data-ttu-id="6118e-105">實現命令</span><span class="sxs-lookup"><span data-stu-id="6118e-105">realize command</span></span>

<span data-ttu-id="6118e-106">「實現」命令會指示裝置在顯示的視窗中，選取並實現其調色板的顯示內容。</span><span class="sxs-lookup"><span data-stu-id="6118e-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="6118e-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6118e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6118e-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6118e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6118e-109">參數</span><span class="sxs-lookup"><span data-stu-id="6118e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6118e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6118e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6118e-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6118e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6118e-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="6118e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6118e-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span><span class="sxs-lookup"><span data-stu-id="6118e-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="6118e-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="6118e-114">One of the following flags.</span></span>



| <span data-ttu-id="6118e-115">值</span><span class="sxs-lookup"><span data-stu-id="6118e-115">Value</span></span>      | <span data-ttu-id="6118e-116">意義</span><span class="sxs-lookup"><span data-stu-id="6118e-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6118e-117">背景資訊</span><span class="sxs-lookup"><span data-stu-id="6118e-117">background</span></span> | <span data-ttu-id="6118e-118">將調色板視為背景調色板。</span><span class="sxs-lookup"><span data-stu-id="6118e-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="6118e-119">正常</span><span class="sxs-lookup"><span data-stu-id="6118e-119">normal</span></span>     | <span data-ttu-id="6118e-120">瞭解最上層視窗的調色板。</span><span class="sxs-lookup"><span data-stu-id="6118e-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="6118e-121">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="6118e-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6118e-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6118e-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6118e-123">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="6118e-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6118e-124">若為數位視訊裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="6118e-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="6118e-125">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6118e-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6118e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="6118e-126">Return Value</span></span>

<span data-ttu-id="6118e-127">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6118e-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6118e-128">備註</span><span class="sxs-lookup"><span data-stu-id="6118e-128">Remarks</span></span>

<span data-ttu-id="6118e-129">只有當您的應用程式使用視窗控制碼，並收到 **wm \_ QUERYNEWPALLETTE** 或 **WM \_ PALETTECHANGED** 訊息時，才能使用此命令。</span><span class="sxs-lookup"><span data-stu-id="6118e-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="6118e-130">範例</span><span class="sxs-lookup"><span data-stu-id="6118e-130">Examples</span></span>

<span data-ttu-id="6118e-131">下列命令會告知 "myvideo" 裝置，以實現其調色板。</span><span class="sxs-lookup"><span data-stu-id="6118e-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="6118e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6118e-132">Requirements</span></span>



| <span data-ttu-id="6118e-133">需求</span><span class="sxs-lookup"><span data-stu-id="6118e-133">Requirement</span></span> | <span data-ttu-id="6118e-134">值</span><span class="sxs-lookup"><span data-stu-id="6118e-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6118e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6118e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6118e-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6118e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6118e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6118e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6118e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6118e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6118e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6118e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6118e-140">Mci</span><span class="sxs-lookup"><span data-stu-id="6118e-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6118e-141">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="6118e-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

