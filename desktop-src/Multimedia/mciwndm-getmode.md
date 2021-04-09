---
title: 'MCIWNDM_GETMODE 訊息 (Vfw .h) '
description: MCIWNDM \_ GETMODE 訊息會抓取 MCI 裝置目前的作業模式。 MCI 裝置有數個作業模式，由常數指定。 您可以使用 MCIWndGetMode 宏明確地傳送此訊息。
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093791"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="0caf7-106">MCIWNDM \_ GETMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="0caf7-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="0caf7-107">**MCIWNDM \_ GETMODE** 訊息會抓取 MCI 裝置目前的作業模式。</span><span class="sxs-lookup"><span data-stu-id="0caf7-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="0caf7-108">MCI 裝置有數個作業模式，由常數指定。</span><span class="sxs-lookup"><span data-stu-id="0caf7-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="0caf7-109">您可以使用 [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0caf7-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="0caf7-110">參數</span><span class="sxs-lookup"><span data-stu-id="0caf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0caf7-111"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="0caf7-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="0caf7-112">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0caf7-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0caf7-113"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="0caf7-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="0caf7-114">用來傳回模式的應用程式定義緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="0caf7-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0caf7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0caf7-115">Return Value</span></span>

<span data-ttu-id="0caf7-116">傳回對應于定義模式之 MCI 常數的整數。</span><span class="sxs-lookup"><span data-stu-id="0caf7-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="0caf7-117">備註</span><span class="sxs-lookup"><span data-stu-id="0caf7-117">Remarks</span></span>

<span data-ttu-id="0caf7-118">如果描述模式的以 null 終止的字串比緩衝區長，則會被截斷。</span><span class="sxs-lookup"><span data-stu-id="0caf7-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="0caf7-119">並非所有裝置都可以在每種模式下運作。</span><span class="sxs-lookup"><span data-stu-id="0caf7-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="0caf7-120">例如，MCIAVI 裝置是播放裝置;它不支援錄製模式。</span><span class="sxs-lookup"><span data-stu-id="0caf7-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="0caf7-121">您可以使用 **MCIWNDM \_ GETMODE** 來取出下列模式。</span><span class="sxs-lookup"><span data-stu-id="0caf7-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="0caf7-122">作業模式</span><span class="sxs-lookup"><span data-stu-id="0caf7-122">Operating mode</span></span> | <span data-ttu-id="0caf7-123">MCI 常數</span><span class="sxs-lookup"><span data-stu-id="0caf7-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="0caf7-124">未就緒</span><span class="sxs-lookup"><span data-stu-id="0caf7-124">not ready</span></span>      | <span data-ttu-id="0caf7-125">MCI \_ 模式 \_ 未 \_ 就緒</span><span class="sxs-lookup"><span data-stu-id="0caf7-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="0caf7-126">開啟</span><span class="sxs-lookup"><span data-stu-id="0caf7-126">open</span></span>           | <span data-ttu-id="0caf7-127">\_開啟 MCI 模式 \_</span><span class="sxs-lookup"><span data-stu-id="0caf7-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="0caf7-128">暫停 (paused)</span><span class="sxs-lookup"><span data-stu-id="0caf7-128">paused</span></span>         | <span data-ttu-id="0caf7-129">MCI \_ 模式 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="0caf7-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="0caf7-130">正在播放 (playing)</span><span class="sxs-lookup"><span data-stu-id="0caf7-130">playing</span></span>        | <span data-ttu-id="0caf7-131">MCI \_ 模式 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="0caf7-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="0caf7-132">記錄</span><span class="sxs-lookup"><span data-stu-id="0caf7-132">recording</span></span>      | <span data-ttu-id="0caf7-133">MCI \_ 模式 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="0caf7-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="0caf7-134">搜尋</span><span class="sxs-lookup"><span data-stu-id="0caf7-134">seeking</span></span>        | <span data-ttu-id="0caf7-135">MCI \_ 模式 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="0caf7-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="0caf7-136">停止</span><span class="sxs-lookup"><span data-stu-id="0caf7-136">stopped</span></span>        | <span data-ttu-id="0caf7-137">MCI \_ 模式 \_ 停止</span><span class="sxs-lookup"><span data-stu-id="0caf7-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="0caf7-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="0caf7-138">Requirements</span></span>



| <span data-ttu-id="0caf7-139">需求</span><span class="sxs-lookup"><span data-stu-id="0caf7-139">Requirement</span></span> | <span data-ttu-id="0caf7-140">值</span><span class="sxs-lookup"><span data-stu-id="0caf7-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0caf7-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0caf7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0caf7-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0caf7-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0caf7-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0caf7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0caf7-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0caf7-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0caf7-145">標頭</span><span class="sxs-lookup"><span data-stu-id="0caf7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0caf7-146"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="0caf7-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0caf7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0caf7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0caf7-148">**MCIWndGetMode**</span><span class="sxs-lookup"><span data-stu-id="0caf7-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





