---
title: 'MCIWNDM_GETTIMEFORMAT 訊息 (Vfw .h) '
description: MCIWNDM \_ GETTIMEFORMAT 訊息會以兩種形式，以數值和字串形式抓取 MCI 裝置目前的時間格式。 您可以使用 MCIWndGetTimeFormat 宏明確地傳送此訊息。
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685592"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="f4e90-105">MCIWNDM \_ GETTIMEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="f4e90-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="f4e90-106">**MCIWNDM \_ GETTIMEFORMAT** 訊息會以兩種形式抓取 MCI 裝置的目前時間格式：作為數值和字串。</span><span class="sxs-lookup"><span data-stu-id="f4e90-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="f4e90-107">您可以使用 [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f4e90-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="f4e90-108">參數</span><span class="sxs-lookup"><span data-stu-id="f4e90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e90-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="f4e90-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="f4e90-110">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4e90-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f4e90-111"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="f4e90-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="f4e90-112">緩衝區的指標，包含時間格式以 null 終止的字串格式。</span><span class="sxs-lookup"><span data-stu-id="f4e90-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e90-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4e90-113">Return Value</span></span>

<span data-ttu-id="f4e90-114">傳回對應于定義時間格式之 MCI 常數的整數。</span><span class="sxs-lookup"><span data-stu-id="f4e90-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e90-115">備註</span><span class="sxs-lookup"><span data-stu-id="f4e90-115">Remarks</span></span>

<span data-ttu-id="f4e90-116">如果時間格式字串的長度超過傳回緩衝區，MCIWnd 會截斷字串。</span><span class="sxs-lookup"><span data-stu-id="f4e90-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="f4e90-117">MCI 裝置可支援下列一或多個時間格式。</span><span class="sxs-lookup"><span data-stu-id="f4e90-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="f4e90-118">時間格式</span><span class="sxs-lookup"><span data-stu-id="f4e90-118">Time format</span></span>                      | <span data-ttu-id="f4e90-119">MCI 常數</span><span class="sxs-lookup"><span data-stu-id="f4e90-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="f4e90-120">位元組</span><span class="sxs-lookup"><span data-stu-id="f4e90-120">Bytes</span></span>                            | <span data-ttu-id="f4e90-121">MCI \_ 格式 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="f4e90-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="f4e90-122">框架</span><span class="sxs-lookup"><span data-stu-id="f4e90-122">Frames</span></span>                           | <span data-ttu-id="f4e90-123">MCI \_ 格式 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="f4e90-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="f4e90-124">小時、分鐘、秒</span><span class="sxs-lookup"><span data-stu-id="f4e90-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="f4e90-125">MCI \_ 格式 \_ HMS</span><span class="sxs-lookup"><span data-stu-id="f4e90-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="f4e90-126">毫秒</span><span class="sxs-lookup"><span data-stu-id="f4e90-126">Milliseconds</span></span>                     | <span data-ttu-id="f4e90-127">MCI \_ 格式 \_ 毫秒</span><span class="sxs-lookup"><span data-stu-id="f4e90-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="f4e90-128">分鐘、秒、框架</span><span class="sxs-lookup"><span data-stu-id="f4e90-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="f4e90-129">MCI \_ 格式 \_ MSF</span><span class="sxs-lookup"><span data-stu-id="f4e90-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="f4e90-130">範例</span><span class="sxs-lookup"><span data-stu-id="f4e90-130">Samples</span></span>                          | <span data-ttu-id="f4e90-131">MCI \_ 格式 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="f4e90-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="f4e90-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="f4e90-132">SMPTE 24</span></span>                         | <span data-ttu-id="f4e90-133">MCI \_ 格式的 \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="f4e90-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="f4e90-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="f4e90-134">SMPTE 25</span></span>                         | <span data-ttu-id="f4e90-135">MCI \_ 格式的 \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="f4e90-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="f4e90-136">SMPTE 30 下降</span><span class="sxs-lookup"><span data-stu-id="f4e90-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="f4e90-137">MCI \_ 格式的 \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="f4e90-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="f4e90-138">SMPTE 30 (非捨棄) </span><span class="sxs-lookup"><span data-stu-id="f4e90-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="f4e90-139">MCI \_ 格式 \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="f4e90-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="f4e90-140">曲目、分、秒、畫面格</span><span class="sxs-lookup"><span data-stu-id="f4e90-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="f4e90-141">MCI \_ 格式 \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="f4e90-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="f4e90-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4e90-142">Requirements</span></span>



| <span data-ttu-id="f4e90-143">需求</span><span class="sxs-lookup"><span data-stu-id="f4e90-143">Requirement</span></span> | <span data-ttu-id="f4e90-144">值</span><span class="sxs-lookup"><span data-stu-id="f4e90-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4e90-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4e90-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e90-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4e90-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f4e90-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e90-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e90-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4e90-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4e90-149">標頭</span><span class="sxs-lookup"><span data-stu-id="f4e90-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e90-150"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e90-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e90-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4e90-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e90-152">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f4e90-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





