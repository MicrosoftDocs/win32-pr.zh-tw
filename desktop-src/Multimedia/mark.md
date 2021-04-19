---
title: mark 命令
description: Mark 命令控制錄影帶上的標記錄製和清除。 VCR 裝置會辨識此命令。
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- 標示命令 Windows 多媒體
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991304"
---
# <a name="mark-command"></a><span data-ttu-id="c67b7-105">mark 命令</span><span class="sxs-lookup"><span data-stu-id="c67b7-105">mark command</span></span>

<span data-ttu-id="c67b7-106">Mark 命令控制錄影帶上的標記錄製和清除。</span><span class="sxs-lookup"><span data-stu-id="c67b7-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="c67b7-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="c67b7-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="c67b7-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c67b7-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c67b7-109">參數</span><span class="sxs-lookup"><span data-stu-id="c67b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67b7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c67b7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c67b7-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c67b7-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c67b7-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="c67b7-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c67b7-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span><span class="sxs-lookup"><span data-stu-id="c67b7-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="c67b7-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="c67b7-114">One of the following flags.</span></span>



| <span data-ttu-id="c67b7-115">值</span><span class="sxs-lookup"><span data-stu-id="c67b7-115">Value</span></span> | <span data-ttu-id="c67b7-116">意義</span><span class="sxs-lookup"><span data-stu-id="c67b7-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c67b7-117">erase</span><span class="sxs-lookup"><span data-stu-id="c67b7-117">erase</span></span> | <span data-ttu-id="c67b7-118">清除目前位置的標記（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c67b7-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="c67b7-119">若要清除標記，請先搜尋標記，然後發出 mark "erase" 命令。</span><span class="sxs-lookup"><span data-stu-id="c67b7-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="c67b7-120">寫入</span><span class="sxs-lookup"><span data-stu-id="c67b7-120">write</span></span> | <span data-ttu-id="c67b7-121">在目前位置寫入標記。</span><span class="sxs-lookup"><span data-stu-id="c67b7-121">Writes a mark at the current position.</span></span> <span data-ttu-id="c67b7-122">VCR 可能必須處於「播放」或「錄製」模式，此命令才會成功。</span><span class="sxs-lookup"><span data-stu-id="c67b7-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="c67b7-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c67b7-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c67b7-124">可以是「等候」、「通知」或「測試」。</span><span class="sxs-lookup"><span data-stu-id="c67b7-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="c67b7-125">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="c67b7-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67b7-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="c67b7-126">Return Value</span></span>

<span data-ttu-id="c67b7-127">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c67b7-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c67b7-128">備註</span><span class="sxs-lookup"><span data-stu-id="c67b7-128">Remarks</span></span>

<span data-ttu-id="c67b7-129">標記是寫入內容的特殊信號，可由 VCR 在高速搜尋期間偵測到。</span><span class="sxs-lookup"><span data-stu-id="c67b7-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="c67b7-130">標記是 VCR 特定的。</span><span class="sxs-lookup"><span data-stu-id="c67b7-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67b7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c67b7-131">Requirements</span></span>



| <span data-ttu-id="c67b7-132">需求</span><span class="sxs-lookup"><span data-stu-id="c67b7-132">Requirement</span></span> | <span data-ttu-id="c67b7-133">值</span><span class="sxs-lookup"><span data-stu-id="c67b7-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c67b7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c67b7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c67b7-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c67b7-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c67b7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c67b7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c67b7-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c67b7-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c67b7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c67b7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67b7-139">Mci</span><span class="sxs-lookup"><span data-stu-id="c67b7-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c67b7-140">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="c67b7-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

