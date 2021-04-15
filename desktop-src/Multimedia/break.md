---
title: break 命令
description: Break 命令會指定要中止使用 \ 0034 叫用之命令的索引鍵; wait \ 0034;國旗。 此命令是 MCI 系統命令;它是由 MCI 直接解讀。
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- 中斷命令 Windows 多媒體
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466785"
---
# <a name="break-command"></a><span data-ttu-id="4f81f-105">break 命令</span><span class="sxs-lookup"><span data-stu-id="4f81f-105">break command</span></span>

<span data-ttu-id="4f81f-106">Break 命令會指定索引鍵，以中止使用 "wait" 旗標叫用的命令。</span><span class="sxs-lookup"><span data-stu-id="4f81f-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="4f81f-107">此命令是 MCI 系統命令;它是由 MCI 直接解讀。</span><span class="sxs-lookup"><span data-stu-id="4f81f-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="4f81f-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4f81f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4f81f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f81f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f81f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4f81f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4f81f-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f81f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4f81f-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="4f81f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4f81f-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span><span class="sxs-lookup"><span data-stu-id="4f81f-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="4f81f-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="4f81f-114">One of the following flags.</span></span>



| <span data-ttu-id="4f81f-115">值</span><span class="sxs-lookup"><span data-stu-id="4f81f-115">Value</span></span>                 | <span data-ttu-id="4f81f-116">意義</span><span class="sxs-lookup"><span data-stu-id="4f81f-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4f81f-117">on *virtual key 程式碼*</span><span class="sxs-lookup"><span data-stu-id="4f81f-117">on *virtual key code*</span></span> | <span data-ttu-id="4f81f-118">指定中止使用 "wait" 旗標啟動之命令的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4f81f-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="4f81f-119">關</span><span class="sxs-lookup"><span data-stu-id="4f81f-119">off</span></span>                   | <span data-ttu-id="4f81f-120">停用目前的 break 鍵。</span><span class="sxs-lookup"><span data-stu-id="4f81f-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="4f81f-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4f81f-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4f81f-122">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="4f81f-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4f81f-123">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="4f81f-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4f81f-124">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="4f81f-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f81f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f81f-125">Return Value</span></span>

<span data-ttu-id="4f81f-126">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f81f-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f81f-127">備註</span><span class="sxs-lookup"><span data-stu-id="4f81f-127">Remarks</span></span>

<span data-ttu-id="4f81f-128">當啟用 break 鍵，且使用者按下 *lpszVirtKey* 參數中指定的虛擬金鑰程式碼所識別的金鑰時，裝置會將控制權傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="4f81f-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="4f81f-129">可能的話，命令會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="4f81f-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="4f81f-130">範例</span><span class="sxs-lookup"><span data-stu-id="4f81f-130">Examples</span></span>

<span data-ttu-id="4f81f-131">下列命令會將 F2 設定為 "mysound" 裝置的 break 鍵。</span><span class="sxs-lookup"><span data-stu-id="4f81f-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="4f81f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f81f-132">Requirements</span></span>



| <span data-ttu-id="4f81f-133">需求</span><span class="sxs-lookup"><span data-stu-id="4f81f-133">Requirement</span></span> | <span data-ttu-id="4f81f-134">值</span><span class="sxs-lookup"><span data-stu-id="4f81f-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f81f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f81f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4f81f-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f81f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f81f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f81f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4f81f-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f81f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f81f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f81f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f81f-140">Mci</span><span class="sxs-lookup"><span data-stu-id="4f81f-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4f81f-141">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="4f81f-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

