---
title: settimecode 命令
description: Settimecode 命令會啟用或停用 VCR 的時間碼記錄。 VCR 裝置會辨識此命令。
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- settimecode 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686628"
---
# <a name="settimecode-command"></a><span data-ttu-id="c7604-105">settimecode 命令</span><span class="sxs-lookup"><span data-stu-id="c7604-105">settimecode command</span></span>

<span data-ttu-id="c7604-106">Settimecode 命令會啟用或停用 VCR 的時間碼記錄。</span><span class="sxs-lookup"><span data-stu-id="c7604-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="c7604-107">VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="c7604-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="c7604-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c7604-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c7604-109">參數</span><span class="sxs-lookup"><span data-stu-id="c7604-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7604-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c7604-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c7604-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7604-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c7604-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="c7604-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c7604-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span><span class="sxs-lookup"><span data-stu-id="c7604-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="c7604-114">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="c7604-114">One of the following flags.</span></span>



| <span data-ttu-id="c7604-115">值</span><span class="sxs-lookup"><span data-stu-id="c7604-115">Value</span></span>      | <span data-ttu-id="c7604-116">意義</span><span class="sxs-lookup"><span data-stu-id="c7604-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="c7604-117">記錄于</span><span class="sxs-lookup"><span data-stu-id="c7604-117">record on</span></span>  | <span data-ttu-id="c7604-118">設定 VCR 來記錄時間碼。</span><span class="sxs-lookup"><span data-stu-id="c7604-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="c7604-119">關閉記錄</span><span class="sxs-lookup"><span data-stu-id="c7604-119">record off</span></span> | <span data-ttu-id="c7604-120">停用時間碼記錄。</span><span class="sxs-lookup"><span data-stu-id="c7604-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="c7604-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c7604-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c7604-122">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="c7604-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="c7604-123">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="c7604-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7604-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7604-124">Return Value</span></span>

<span data-ttu-id="c7604-125">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7604-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7604-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7604-126">Requirements</span></span>



| <span data-ttu-id="c7604-127">需求</span><span class="sxs-lookup"><span data-stu-id="c7604-127">Requirement</span></span> | <span data-ttu-id="c7604-128">值</span><span class="sxs-lookup"><span data-stu-id="c7604-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c7604-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7604-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c7604-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7604-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c7604-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7604-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c7604-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7604-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c7604-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7604-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7604-134">Mci</span><span class="sxs-lookup"><span data-stu-id="c7604-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c7604-135">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="c7604-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

