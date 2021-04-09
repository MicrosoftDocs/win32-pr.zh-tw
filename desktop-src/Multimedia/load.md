---
title: 載入命令
description: Load 命令會以裝置特定的格式載入檔案。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- 載入命令 Windows 多媒體
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686156"
---
# <a name="load-command"></a><span data-ttu-id="c3d75-105">載入命令</span><span class="sxs-lookup"><span data-stu-id="c3d75-105">load command</span></span>

<span data-ttu-id="c3d75-106">Load 命令會以裝置特定的格式載入檔案。</span><span class="sxs-lookup"><span data-stu-id="c3d75-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="c3d75-107">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="c3d75-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c3d75-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c3d75-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c3d75-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3d75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d75-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c3d75-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c3d75-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3d75-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c3d75-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="c3d75-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c3d75-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span><span class="sxs-lookup"><span data-stu-id="c3d75-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="c3d75-114">要載入的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="c3d75-114">Path and filename to load.</span></span> <span data-ttu-id="c3d75-115">針對影片重迭裝置，這也可以包含資料的目標矩形。</span><span class="sxs-lookup"><span data-stu-id="c3d75-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="c3d75-116">若要指定目標矩形，請指定 "at"，後面接著 **X1 Y1 X2 Y2**，其中 **x1 y1** 指定矩形的左上角，而 **X2 Y2** 指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="c3d75-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="c3d75-117">矩形相對於影片緩衝區來源。</span><span class="sxs-lookup"><span data-stu-id="c3d75-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="c3d75-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c3d75-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c3d75-119">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="c3d75-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c3d75-120">若為數位視訊裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="c3d75-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c3d75-121">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="c3d75-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d75-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3d75-122">Return Value</span></span>

<span data-ttu-id="c3d75-123">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3d75-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d75-124">備註</span><span class="sxs-lookup"><span data-stu-id="c3d75-124">Remarks</span></span>

<span data-ttu-id="c3d75-125">當載入完成時，"vidboard" 裝置會傳送通知訊息。</span><span class="sxs-lookup"><span data-stu-id="c3d75-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="c3d75-126">範例</span><span class="sxs-lookup"><span data-stu-id="c3d75-126">Examples</span></span>

<span data-ttu-id="c3d75-127">下列命令會將檔案載入至 "vidboard" 裝置。</span><span class="sxs-lookup"><span data-stu-id="c3d75-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="c3d75-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3d75-128">Requirements</span></span>



| <span data-ttu-id="c3d75-129">需求</span><span class="sxs-lookup"><span data-stu-id="c3d75-129">Requirement</span></span> | <span data-ttu-id="c3d75-130">值</span><span class="sxs-lookup"><span data-stu-id="c3d75-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3d75-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3d75-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d75-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3d75-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3d75-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3d75-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d75-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3d75-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3d75-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3d75-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d75-136">Mci</span><span class="sxs-lookup"><span data-stu-id="c3d75-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c3d75-137">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="c3d75-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

