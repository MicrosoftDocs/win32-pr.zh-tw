---
title: '關閉命令 (Corecrt- \_ .h) '
description: Close 命令會關閉裝置或檔案，以及任何相關聯的資源。 當裝置或所有檔案的所有實例都已關閉時，MCI 會卸載裝置。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- 關閉命令 Windows 多媒體
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934256"
---
# <a name="close-command"></a><span data-ttu-id="cedc7-106">關閉命令</span><span class="sxs-lookup"><span data-stu-id="cedc7-106">close command</span></span>

<span data-ttu-id="cedc7-107">Close 命令會關閉裝置或檔案，以及任何相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="cedc7-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="cedc7-108">當裝置或所有檔案的所有實例都已關閉時，MCI 會卸載裝置。</span><span class="sxs-lookup"><span data-stu-id="cedc7-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="cedc7-109">所有 MCI 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="cedc7-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="cedc7-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cedc7-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="cedc7-111">參數</span><span class="sxs-lookup"><span data-stu-id="cedc7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cedc7-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cedc7-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cedc7-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cedc7-113">Identifier of an MCI device.</span></span> <span data-ttu-id="cedc7-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="cedc7-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="cedc7-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="cedc7-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cedc7-116">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="cedc7-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="cedc7-117">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="cedc7-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cedc7-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cedc7-118">Return Value</span></span>

<span data-ttu-id="cedc7-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cedc7-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cedc7-120">備註</span><span class="sxs-lookup"><span data-stu-id="cedc7-120">Remarks</span></span>

<span data-ttu-id="cedc7-121">若要關閉應用程式所開啟的所有裝置，請為 *lpszDeviceID* 參數指定 "all" 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="cedc7-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="cedc7-122">關閉 **cdaudio** 裝置會停止播放音訊。</span><span class="sxs-lookup"><span data-stu-id="cedc7-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="cedc7-123">**Windows 2000/XP：** 如果 **cdaudio** 裝置現正播放，關閉 **cdaudio** 裝置並不會導致音訊停止播放。</span><span class="sxs-lookup"><span data-stu-id="cedc7-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="cedc7-124">先傳送 [停止](stop.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="cedc7-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="cedc7-125">範例</span><span class="sxs-lookup"><span data-stu-id="cedc7-125">Examples</span></span>

<span data-ttu-id="cedc7-126">下列命令會關閉 "mysound" 裝置。</span><span class="sxs-lookup"><span data-stu-id="cedc7-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="cedc7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cedc7-127">Requirements</span></span>



| <span data-ttu-id="cedc7-128">需求</span><span class="sxs-lookup"><span data-stu-id="cedc7-128">Requirement</span></span> | <span data-ttu-id="cedc7-129">值</span><span class="sxs-lookup"><span data-stu-id="cedc7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cedc7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cedc7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cedc7-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cedc7-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cedc7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cedc7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cedc7-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cedc7-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cedc7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="cedc7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cedc7-135"><dt>Corecrt \_ 的 io。h</dt></span><span class="sxs-lookup"><span data-stu-id="cedc7-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cedc7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cedc7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedc7-137">Mci</span><span class="sxs-lookup"><span data-stu-id="cedc7-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cedc7-138">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="cedc7-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

