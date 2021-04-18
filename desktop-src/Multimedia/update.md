---
title: update 命令
description: Update 命令會將目前的框架重新繪製到指定的裝置內容 (DC) 。 數位影片裝置辨識此命令。
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- 更新命令 Windows 多媒體
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509364"
---
# <a name="update-command"></a><span data-ttu-id="e7336-105">update 命令</span><span class="sxs-lookup"><span data-stu-id="e7336-105">update command</span></span>

<span data-ttu-id="e7336-106">Update 命令會將目前的框架重新繪製到指定的裝置內容 (DC) 。</span><span class="sxs-lookup"><span data-stu-id="e7336-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="e7336-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="e7336-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="e7336-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="e7336-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e7336-109">參數</span><span class="sxs-lookup"><span data-stu-id="e7336-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7336-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e7336-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e7336-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7336-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e7336-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="e7336-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e7336-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span><span class="sxs-lookup"><span data-stu-id="e7336-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="e7336-114">DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e7336-114">Handle of a DC.</span></span> <span data-ttu-id="e7336-115">下表列出可辨識 **update** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="e7336-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="e7336-116">值</span><span class="sxs-lookup"><span data-stu-id="e7336-116">Value</span></span>        | <span data-ttu-id="e7336-117">意義</span><span class="sxs-lookup"><span data-stu-id="e7336-117">Meaning</span></span>                       | <span data-ttu-id="e7336-118">意義</span><span class="sxs-lookup"><span data-stu-id="e7336-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="e7336-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="e7336-119">digitalvideo</span></span> | <span data-ttu-id="e7336-120">在 *rect* 的 hdc *hdc* hdc *hdc*</span><span class="sxs-lookup"><span data-stu-id="e7336-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="e7336-121">油漆 hdc *hdc*</span><span class="sxs-lookup"><span data-stu-id="e7336-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="e7336-122">下表列出可在 **lpszHDC** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="e7336-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="e7336-123">值</span><span class="sxs-lookup"><span data-stu-id="e7336-123">Value</span></span>               | <span data-ttu-id="e7336-124">意義</span><span class="sxs-lookup"><span data-stu-id="e7336-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7336-125">hdc *hdc*</span><span class="sxs-lookup"><span data-stu-id="e7336-125">hdc *hdc*</span></span>           | <span data-ttu-id="e7336-126">指定要繪製之 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e7336-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="e7336-127">*rect* 的 hdc *hdc*</span><span class="sxs-lookup"><span data-stu-id="e7336-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="e7336-128">指定相對於用戶端矩形的裁剪矩形。</span><span class="sxs-lookup"><span data-stu-id="e7336-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="e7336-129">油漆 hdc *hdc*</span><span class="sxs-lookup"><span data-stu-id="e7336-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="e7336-130">當應用程式收到適用于 DC 的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時繪製 dc。</span><span class="sxs-lookup"><span data-stu-id="e7336-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="e7336-131">若要指定 DC 的控制碼，請使用字串 "hdc"，後面接著控制碼的 ASCII 標記法。</span><span class="sxs-lookup"><span data-stu-id="e7336-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="e7336-132">矩形會指定為 **X1 Y1 X2 Y2**。</span><span class="sxs-lookup"><span data-stu-id="e7336-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="e7336-133">座標 **X1 Y1** 指定矩形的左上角，而座標 **X2 Y2** 指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="e7336-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="e7336-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e7336-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e7336-135">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="e7336-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e7336-136">若為數位視訊裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="e7336-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="e7336-137">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="e7336-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7336-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7336-138">Return Value</span></span>

<span data-ttu-id="e7336-139">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e7336-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="e7336-140">範例</span><span class="sxs-lookup"><span data-stu-id="e7336-140">Examples</span></span>

<span data-ttu-id="e7336-141">下列命令會更新「電影」裝置所使用的整個顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="e7336-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="e7336-142">數位203是從 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 函式取得之 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e7336-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="e7336-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7336-143">Requirements</span></span>



| <span data-ttu-id="e7336-144">需求</span><span class="sxs-lookup"><span data-stu-id="e7336-144">Requirement</span></span> | <span data-ttu-id="e7336-145">值</span><span class="sxs-lookup"><span data-stu-id="e7336-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e7336-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7336-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e7336-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7336-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e7336-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7336-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e7336-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7336-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e7336-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7336-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7336-151">Mci</span><span class="sxs-lookup"><span data-stu-id="e7336-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e7336-152">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="e7336-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

