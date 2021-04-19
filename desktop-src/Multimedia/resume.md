---
title: resume 命令
description: Resume 命令會在使用 pause 命令暫停的裝置上繼續播放或錄製。
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- 繼續命令 Windows 多媒體
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999598"
---
# <a name="resume-command"></a><span data-ttu-id="9e49f-104">resume 命令</span><span class="sxs-lookup"><span data-stu-id="9e49f-104">resume command</span></span>

<span data-ttu-id="9e49f-105">Resume 命令會在使用 [pause](pause.md) 命令暫停的裝置上繼續播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="9e49f-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="9e49f-106">數位-影片、VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="9e49f-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="9e49f-107">雖然 CD 音訊、MIDI sequencer 和 videodisc 裝置也會辨識此命令，但 MCICDA、MCISEQ 和 MCIPIONR 設備磁碟機並不支援。</span><span class="sxs-lookup"><span data-stu-id="9e49f-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="9e49f-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="9e49f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9e49f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9e49f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e49f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9e49f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9e49f-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e49f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9e49f-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="9e49f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9e49f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="9e49f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9e49f-114">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="9e49f-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="9e49f-115">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="9e49f-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="9e49f-116">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="9e49f-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e49f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e49f-117">Return Value</span></span>

<span data-ttu-id="9e49f-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e49f-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="9e49f-119">範例</span><span class="sxs-lookup"><span data-stu-id="9e49f-119">Examples</span></span>

<span data-ttu-id="9e49f-120">下列命令會繼續播放或錄製 "newsound" 裝置。</span><span class="sxs-lookup"><span data-stu-id="9e49f-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="9e49f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e49f-121">Requirements</span></span>



| <span data-ttu-id="9e49f-122">需求</span><span class="sxs-lookup"><span data-stu-id="9e49f-122">Requirement</span></span> | <span data-ttu-id="9e49f-123">值</span><span class="sxs-lookup"><span data-stu-id="9e49f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e49f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e49f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e49f-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e49f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9e49f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e49f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e49f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e49f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9e49f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e49f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e49f-129">Mci</span><span class="sxs-lookup"><span data-stu-id="9e49f-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9e49f-130">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="9e49f-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="9e49f-131">pause</span><span class="sxs-lookup"><span data-stu-id="9e49f-131">pause</span></span>](pause.md)
</dt> </dl>

 

