---
title: step 命令
description: 步驟命令會逐步執行一或多個畫面的向前或反向播放。 預設動作是向前前進一個畫面格。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- 步驟命令 Windows 多媒體
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465220"
---
# <a name="step-command"></a><span data-ttu-id="6cafd-106">step 命令</span><span class="sxs-lookup"><span data-stu-id="6cafd-106">step command</span></span>

<span data-ttu-id="6cafd-107">步驟命令會逐步執行一或多個畫面的向前或反向播放。</span><span class="sxs-lookup"><span data-stu-id="6cafd-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="6cafd-108">預設動作是向前前進一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6cafd-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="6cafd-109">數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6cafd-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="6cafd-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6cafd-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6cafd-111">參數</span><span class="sxs-lookup"><span data-stu-id="6cafd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cafd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6cafd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6cafd-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cafd-113">Identifier of an MCI device.</span></span> <span data-ttu-id="6cafd-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="6cafd-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6cafd-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span><span class="sxs-lookup"><span data-stu-id="6cafd-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6cafd-116">下列其中一個或兩個旗標。</span><span class="sxs-lookup"><span data-stu-id="6cafd-116">One or both of the following flags.</span></span>



| <span data-ttu-id="6cafd-117">值</span><span class="sxs-lookup"><span data-stu-id="6cafd-117">Value</span></span>       | <span data-ttu-id="6cafd-118">意義</span><span class="sxs-lookup"><span data-stu-id="6cafd-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cafd-119">依 *畫面* 格</span><span class="sxs-lookup"><span data-stu-id="6cafd-119">by *frames*</span></span> | <span data-ttu-id="6cafd-120">指出要逐步執行的框架數目。</span><span class="sxs-lookup"><span data-stu-id="6cafd-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="6cafd-121">如果您指定了負值的 *框架* 值，就不能指定「反轉」旗標。</span><span class="sxs-lookup"><span data-stu-id="6cafd-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="6cafd-122">reverse</span><span class="sxs-lookup"><span data-stu-id="6cafd-122">reverse</span></span>     | <span data-ttu-id="6cafd-123">反向步驟畫面格。</span><span class="sxs-lookup"><span data-stu-id="6cafd-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="6cafd-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6cafd-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6cafd-125">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="6cafd-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6cafd-126">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="6cafd-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="6cafd-127">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6cafd-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cafd-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cafd-128">Return Value</span></span>

<span data-ttu-id="6cafd-129">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6cafd-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cafd-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cafd-130">Requirements</span></span>



| <span data-ttu-id="6cafd-131">需求</span><span class="sxs-lookup"><span data-stu-id="6cafd-131">Requirement</span></span> | <span data-ttu-id="6cafd-132">值</span><span class="sxs-lookup"><span data-stu-id="6cafd-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6cafd-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cafd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6cafd-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cafd-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6cafd-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cafd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6cafd-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cafd-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6cafd-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cafd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cafd-138">Mci</span><span class="sxs-lookup"><span data-stu-id="6cafd-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6cafd-139">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="6cafd-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

